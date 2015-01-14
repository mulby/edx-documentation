.. include:: ../links.rst

.. _Installing edX Insights:

#######################
Installing edX Insights
#######################

This chapter is intended for those who are interested in running edX Insights
and its dependencies in a production environment.

See the following sections:

* `Overview`_

********
Overview
********

edX Insights provides Course Staff access to data gathered from courses that
are being used by students. edX Insights presents this information to the
Course Staff via charts, summary statistics, and data tables.

The LMS gathers data about student activity. This data is aggregated by the edX
Analytics Pipeline. The aggregated data is exposed by the edX Analytics Data
API. edX Insights reads the data from the edX Analytics Data API and presents
the data to Course Staff members.

============
Architecture
============

.. image:: /Images/Analytics_Pipeline.png

==========
Components
==========

edX Learning Management System
******************************

The Learning Management System records student actions in tracking log files.
These files are periodically compressed and copied into a filesystem that can be
read by the edX Analytics Pipeline. The Learning Management System also captures
a lot of information in a MySQL database. The edX Analytics Pipeline connects
directly to this database to extract information about students.

edX Analytics Pipeline
**********************

The edX Analytics Pipeline reads the MySQL database used by the LMS as well as
the tracking log files produced by the LMS. The data is processed and the
resulting summary data is published to the *Result Store*. The result store is a
MySQL database.

Requirements:

* Hadoop version 1.0.3 or higher
* Hive version 0.11.0.2 or higher
* Sqoop version 1.4.5
* Python 2.7
* Either Debian version 6.0 or higher, or Ubuntu version 12.04 or higher.
* A MySQL server version 5.6 or higher

Scheduler
*********

The Scheduler schedules the execution of data computation tasks. Data
computation tasks are run by the edX Analytics Pipeline. Data computation tasks
are used to update parts of the Result Store.

edX Analytics Data API
**********************

The edX Analytics Data API provides an HTTP interface for accessing data in the
Result Store. Typically, the data in the Result Store is updated periodically by
the edX Analytics Pipeline.

Requirements:

* Python 2.7

edX Insights
************

edX Insights uses the edX Analytics Data API to present data to users. Users
access the data using a supported web browser. edX Insights communicates
directly with the Learning Management System to authenticate users, authorize
users and read course structure information.

Requirements:

* Python 2.7

*************************************
What You Should Know Before You Start
*************************************

This guide assumes that you:

* Understand basic terminal usage.
* Understand how the Learning Management System has been deployed and
  configured.
* Understand basic computer network terminology.
* Understand the YAML file format.
* Understand Amazon Web Services terminology.


************************
Planning Your Deployment
************************

All edX Analytics services are designed to be relocatable. This means that they
do not require a particular configuration of virtual servers. You are free to
choose how the services should be distributed among the resources you have
available.

======
Hadoop
======

Most of the computation performed by the edX Analytics Pipeline is implemented
as Map Reduce jobs that currently must be executed by a Hadoop cluster. You can
scale your Hadoop cluster based on your current and projected data sizes. For
very small installations of Open edX, a single virtual server should be
sufficiently powerful to process your data.

Amazon's Elastic MapReduce service offers pre-configured Hadoop clusters. If you
are able to use Amazon Web Services, it is recommended you use this service.
Proper installation and configuration of Hadoop can be time consuming.

Additionally, vendors such as Cloudera and MapR offer simplified Hadoop
administration experiences.

Hadoop clusters can be scaled vertically and horizontally as your data grows.

Hadoop is a distributed system that consists of several different services. It
is worth noting that they are Java services and require a non-trivial amount of
memory to run. The high memory requirement may prevent you from running all
services on the same virtual server if it does not have enough memory available.

================
edX Applications
================

The edX Analytics Data API will be responding to a small number of requests
every time a page is loaded in edX Insights. Small installations can probably
host both services on the same virtual server. Larger installations will want to
consider hosting them on more than one virtual server. A load balancer is
recommended for each service that requires more than one virtual server.

============
Result Store
============

The results of computations performed by the edX Analytics Pipeline are stored
in a MySQL database. Even small installations are recommended to use a different
MySQL server than the one used by the Learning Management System. The query
patterns of the edX Analytics API are more I/O intensive than usual. Placing
both databases on the same server may degrade performance of the Learning
Management System.

=========
Scheduler
=========

Scheduling executions of the edX Analytics Pipeline can be accomplished in many
different ways. Any tool that can periodically execute shell commands should
work. The simplest tool that can perform this task is cron. Jenkins is also a
good candidate.

===================
Example Deployments
===================

Small Scale Using Elastic MapReduce
***********************************

A small deployment might consist of a single master node and a single core node.
The Scheduler is deployed to the master node and periodically executes the edX
Analytics Data Pipeline on this server. Additionally, the edX Analytics API, edX
Insights and Result Store are deployed to the master node. These services run
continuously.

Large Scale Using Elastic MapReduce
***********************************

A large scale deployment consists of a single master node, several core nodes,
and many task nodes deployed into a public subnet of a Virtual Private Cloud.
The edX Analytics API and edX Insights are each deployed into an auto-scaling
group behind an Elastic Load Balancer which terminates SSL connections and
distributes the load among the application servers. The application servers are
deployed into a private subnet of the Virtual Private Cloud. A single virtual
server is deployed into a private subnet to host the Scheduler. The Relational
Database Service is used to deploy a MySQL server into a private subnet. The
MySQL database will be used as the Result Store.

.. image:: /Images/Analytics_AWS_Deployment.png

Large Scale Without Using Elastic MapReduce
*******************************************

A large deployment that does not use Elastic MapReduce requires additional
configuration steps to establish a properly configured environment. A Hadoop
cluster is deployed. The master node is considered the node that is running the
Job Tracker service for Hadoop 1.X deployments or the Resource Manager service
for Hadoop 2.X deployments. Hive and Sqoop are deployed to the master node.
Several servers are deployed outside of the Hadoop cluster that host the
remainder of the infrastructure. The edX Analytics API and edX Insights services
are each deployed to at least one server. The Scheduler is deployed to another
server. A MySQL database is deployed to a server that is configured to host a
relational database.
