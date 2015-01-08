.. _Creating the About Page:

#####################################
Creating the About Page
#####################################


*******************
Overview
*******************

The course About page, sometimes called the "course summary" page, provides
prospective students with important information about your course. The page
includes an overview of the course content as well as important dates and any
course prerequisites. The following image shows a typical About page. You
configure the contents of this page in Studio.

.. image:: ../Images/about_page.png
 :alt: An image of the course About page.

Students see the course About page before they enroll in the course. After a 
student enrolls in the course, some of the information from the About page 
appears on the Student Dashboard.

.. image:: ../Images/dashboard.png
 :alt: An image of the dashboard

For more information, see the following topics:

* :ref:`Provide a Written Overview`
* :ref:`Add a Course Image`
* :ref:`Add a Course Video`
* :ref:`Set Course Time Requirements`
* :ref:`Specify Prerequisite Courses`
* :ref:`Set Important Dates for Your Course`
* :ref:`A Template For Course Overview`

.. note:: For courses on Edge_, only students that you explicitly invite can see 
 the course About page.

.. _Provide a Written Overview:

*********************************
Provide a Written Overview
*********************************

The course overview provides important information for students who may be
interested in taking your course. It introduces the main idea of the course and
describes the topics or concepts that the course covers. The overview can also
provide information about the skills and knowledge your students need before
they enroll in your course, as well as course requirements and staff.

.. note:: If students must complete a specific course before they enroll in your
 course, you can specify a prerequisite course separately. For more information,
 see :ref:`Specify a Prerequisite Course`.

The course overview is circled in the following course About page:

.. image:: ../Images/about-page-course-description.png
 :alt: Image of a course About page with the overview circled

You enter the course overview in Studio by using HTML. A sample template appears
in Studio. We have also provided a boilerplate that you can use for guidance.
For more information, see :ref:`A Template For Your Course Overview`.

To enter the course overview:

#. From the **Settings** menu, select **Schedule & Details**.
#. Scroll down to the **Introducing Your Course** section, then locate the
   **Course Overview** field.

.. image:: ../Images/course_overview.png
  :alt: Image of the HTML course description.

3. Overwrite the existing content as needed for your course, following the
   directions in the boilerplate text. Do not edit HTML tags. For a template
   that includes placeholders, see :ref:`A Template For Your Course Overview`.

   .. note:: There is no save button. Studio automatically saves your changes.
 
4. Click **your course summary page** in the text beneath the field to test how
   the description will appear to students.

.. image:: ../Images/course_overview.png
  :alt: Image of the HTML Course Overview section in Studio

.. note:: For courses on edX.org_, you must communicate the course overview
 to your edX program manager, to ensure the content is accurate on the course
 About page.

.. _Add a Course Image:

************************
Add a Course Image
************************

The course image that you add in Studio appears on the student dashboard. 

On Edge_, the image also appears on the course About page.

In the following example, the course image that was added in Studio is circled
in the student dashboard:

.. image:: ../Images/dashboard-course-image.png
 :alt: Image of the course image in the student dashboard

On edX.org_, the course image you add in Studio does not appear on the course
About page automatically. You must work directly with your edX Program Manager
to set up the course About page.

The course image should be a minimum of 660 pixels in width by 240 pixels in
height, and in .JPG or .PNG format.

#. From the **Settings** menu, select **Schedule & Details**.
#. Scroll down to the **Course Image** section.
#. To select an image from your computer, click **Upload Course Image**, then
   follow the prompts to find and upload your image.
#. View your dashboard to test how the image will appear to students.

.. _Add a Course Video:

*********************************
Add a Course Introduction Video
*********************************

On Edge_, the course introduction video appears on the course About page that
students see.

.. note:: On edX.org_, you work directly with your Program Manager to set up the
 course video in the About page.

In the following example, the course video is circled in the course About
page:

.. image:: ../Images/about-page-course-video.png
 :alt: Image of the course video in the course About page.

The course video should excite and entice potential students to enroll, and
reveal some of the personality the instructors bring to the course.

The video should answer these key questions:

* Who is teaching the course?
* What university or college is the course affiliated with?
* What topics and concepts are covered in your course?
* Why should a learner enroll in your course?

The video should deliver your message as concisely as possible and have a run
time of less than 2 minutes.

Ensure your course introduction video follows the same :ref:`Compression
Specifications` and :ref:`Video Formats` guidelines as course content videos.

To add a course introduction video:


#. Upload the course video to YouTube. Make note of the code that appears
   between **watch?v =** and **&feature** in the URL. This code appears in the
   green box below.

  .. image:: ../Images/image127.png
    :alt: Image of a sample course video
    
2. From the **Settings** menu, select **Schedule & Details**.
#. Scroll down to the **Course Introduction Video** section.
#. In the field below the video box, enter the YouTube video ID (the code you
   copied in step 1). When you add the code, the video automatically loads in
   the video box. Studio automatically saves your changes.


.. _Set Course Time Requirements:

************************************
Set Course Time Requirements
************************************

The estimated effort per week appears at the bottom of the course About page.

#. From the **Settings** menu, select **Schedule & Details**.
#. Scroll down to the **Requirements** section.
#. In the **Hours of Effort per Week** field, enter the number of hours you
   expect students to work on this course each week.
#. View your course About page to test how the requirements will appear to
   students.

.. _Specify Prerequisite Courses:

************************************
Specify Prerequisite Courses
************************************

On the About page, you can specify that students must take a particular course
before they enroll in your course. If a student has not completed the
prerequisite course, he can enroll in your course, but he cannot see any course
content.

To specify a prerequisite course, you must have at least the Course Staff role
in both the current course and in the prerequisite course.

#. In Studio, open your course.
#. On the **Settings** menu, select **Schedule & Details**, and then scroll to
   the end of the **Schedule & Details** page.
#. In the **Requirements** section, under **Prerequisite Course**, select a
   course from the drop-down list.
#. At the bottom of the page, select **Save Changes**.

.. note:: Currently, you can specify only one prerequisite course.

.. _Set Important Dates for Your Course:

***********************************
Set Important Dates for Your Course
***********************************

You must set dates and times for enrollment and for the course.

In Studio, from the **Settings** menu, select **Schedule and Details**.  

.. image:: ../Images/schedule.png
  :alt: An image of the course schedule page.

Follow the on-screen text to enter the course and enrollment schedule.

.. note:: 
 The Time fields on this page, and the times that students see, use UTC
 (Universal Coordinated Time)

.. _The Course Start Date:

=======================
The Course Start Date
=======================


.. note:: The default course start date is set far into the future, to
 **01/01/2030**. This is to ensure that your course does not start before
 you intend it to. You must change the course start date to the date you want
 students to begin using the course.

Students see the course start date and time on their **Current Courses**
dashboards and on the course About page. Students can see some parts of the
course before the course start date. For example, students can see your **Course
Info** page and course-wide discussion topics as soon as they enroll in your
course. For more information about course-wide discussion topics, see
:ref:`Create CourseWide Discussion Topics`.

The following example shows the course start date and time on the course About
page:

.. image:: ../Images/about-page-course-start.png
 :alt: An image of the course About page, with the start date circled.

.. note:: 
 For courses on edX.org_, you must communicate the course start date and time
 to your edX program manager to ensure the date is accurate on the course
 About page.

In the dashboard, students see the start dates and times for each of their
courses, as in the following examples.

.. image:: ../Images/dashboard-course-to-start.png
 :width: 600
 :alt: An image of two courses in the student dashboard, with the start 
 dates and times circled.

.. note:: If you do not specify a start time for your course, students see
   the default start time, 00:00 Coordinated Universal Time (UTC).


.. _Set the Advertised Start Date:

======================================
Set the Advertised Start Date
======================================

You can set an advertised start date for your course that is different than the
course start date you set in the **Schedule and Details** page. You may want to
do this if there is uncertainty about the exact start date. For example, you
could advertise the start date as **Spring, 2014**.

To set an advertised start date:

#. From the **Settings** menu, select **Advanced Settings**.
#. Find the **Course Advertised Start Date** policy key. The default value is
   **null**.
#. Enter the value you want to display as the advertised start date. You can
   use any string, enclosed in double quotation marks. If you format the string
   as a date (for example, as 02/01/2014), the value is parsed and presented to
   students as a date.

  .. image:: ../Images/advertised_start.png
   :alt: Image of the advertised start date policy key with a value of "anytime, self-paced"

4. Click **Save Changes** at the bottom of the page.

The start date shown on the dashboard is now the value of the **Course
Advertised Start Date** policy key:

.. image:: ../Images/dashboard-course_adver_start.png
 :alt: An image of a course listing in the student dashboard, with the
     advertised start date circled.

If you do not change the default course start date (01/01/2030), and the
**Course Advertised Start Date** policy value is ``null``, then the student
dashboard does not list a start date for the course. Students just see that
the course has not yet started.

.. _The Course End Date:

=====================
The Course End Date
=====================

  The course end date is the date after which students can no longer earn credit
toward certificates. Students who have earned certificates can view them after
the course end date.

.. important::
 If you do not set a course end date, students will not be able to access
 earned certificates.

.. note:: 
 For courses on edX.org_, you must communicate the course end date to
 your edX Program Manager, to ensure the date is accurate on the course
 About page.

After grades and certificates are finalized, students see the course end date
on their personal **Current Courses** dashboards, as shown in the following
examples.

* If grades and certificates are not yet finalized, students can see the course
  end date and a message:

  .. image:: ../Images/dashboard-wrapping-course.png
   :alt: Image of a course on the student dashboard that has ended, but not
     been graded

* When grades and certificates are finalized, students who have not earned a
  certificate see their score and the score required to earn a certificate:
  
  .. image:: ../Images/dashboard-no-cert-course.png
   :alt: Image of a course on the student dashboard that has ended, but not
     been graded

* Students whose final score is equal to or higher than the required score can
  click **Download Certificate** to get their certificates as PDFs:

  .. image:: ../Images/dashboard-completed-course.png
   :alt: Image of a course on the student dashboard that has ended, but not
     been graded

.. _A Template For Your Course Overview:

************************************************
 A Template For Your Course Overview
************************************************

  
Replace the placeholders in the following template with your information.

.. code-block:: html

  <section class="about">
    <h2>About This Course</h2>
    <p>Include your long course description here. The long course description
      should contain 150-400 words.</p>
    <p>This is paragraph 2 of the long course description. Add more paragraphs
      as needed. Make sure to enclose them in paragraph tags.</p>
  <section>
  <section class="prerequisites">
    <h2>Requirements</h2>
    <p>Add information about skills and knowledge that students should have 
       before they enroll in your course here.</p>
  </section>
  <section class="course-staff">
    <h2>Course Staff</h2>
    <article class="teacher">
      <div class="teacher-image">
        <!-- Replace the path below with the path to your faculty image. -->
        <img src="/c4x/edX/edX101/asset/Placeholder_FacultyImage.jpg"
          align="left" style="margin:0 20 px 0"/>
      </div>
      <h3>Staff Member</h3>
      <p>Biography of instructor/staff member</p>
    </article>
  <article class="teacher">
      <div class="teacher-image">
        <img src="/c4x/edX/edX101/asset/Placeholder_FalcutyImage.jpg"/>
      </div>
      <h3>Staff Member Name</h3>
      <p>Biography of instructor/staff member</p>
    </article>
  </section>
  <section class="faq">
    <section class="responses">
      <h2>Frequently Asked Questions</h2>
      <article class="response">
        <h3>Do I need to buy a textbook?</h3>
        <p>No, a free online version of Chemistry: Principles, Patterns, and
          Applications, First Edition by Bruce Averill and Patricia Eldredge
          will be available, though you can purchase a printed version
          (published by FlatWorld Knowledge) if you'd like.</p>
      </article>
      <article class="response">
        <h3>Question 2?</h3>
        <p>Answer 2.</p>
      </article>
    </section>
  </section>

  <!--Paragraph: <p>CONTENT GOES IN HERE</p> -->
  <!--Line break: <br/> -->
  <!--Hyperlink: <a href="URL">LINK TEXT</a> -->
  <!--Email hyperlink: <a href="mailto:EMAIL@ADDRESS.COM">LINK TEXT</a> -->
  <!--Bold text: <b>TEXT</b> -->
  <!--Italic text: <i>TEXT</i> -->