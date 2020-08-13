:orphan:

============================================
Responding to Nightly Validation
============================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

**Purpose:**  Once code has been submitted into a release, it is verified on a nightly basis against a much broader set of criteria.  Developers are responsible for monitoring nightly reports and ensuring that their submissions have not caused any regression.  In the event of a regression, developers are expected to prioritize a fix.  The following document describes the types of nightly validation and how to monitor reports.

(Source: https://jive.windriver.com/docs/DOC-55939)

**Procedure:**
---------------

**Verifying Nightly Testing Report**
++++++++++++++++++++++++++++++++++++

The results from the Nightly Testing are emailed in a report to the vx7-project email alias (see example below)

- The email will be titled “VxWorks 7 Nightly Testing Report (<DATE>) - Complete”
- The report is usually followed by a second email that provides an analysis on the failures
- In cases where there was no code change (i.e. no churn), the Nightly Testing will not run.  This results in a "No SPIN Available for Nightly Testing <DATE>" email being sent in place of the report.
- Example of a "No SPIN" email:
  
|image0|
  

- The report will contain:

  - A summary of passed and failed test cases, along with a trend chart
  - A link to the original LTAF report (which will contain links to build and execution logs)
  - A breakdown of the report by domain
  - A list of who committed into the Spin (since the last Nightly Test)
  - A list of known regression defects

- In the event that the emailed analysis reveals a failure in your domain, your team is expected to prioritize a fix for the identified regression(s)

- If an analysis is not yet available, or fails to adequately explain all failures, you are expected to parse the Nightly Testing report by investigating logs available through LTAF

- Example:

|image1|
 

**Verifying Nightly Build & Manufacturing Report**
++++++++++++++++++++++++++++++++++++++++++++++++++++

The results from the Nightly Build & Manufacturing are emailed in a report to the vx7-project email alias (see example below)

- The email will be titled "VX7 Build Results: <RESULT>" where <RESULT> will either be SUCCESSFUL or FAILURE

- If you are not receiving the email, you can subscribe to the distribution list at: http://list-int.wrs.com/sympa/info/vx7-project

- The report will contain:

  - a link to the Build Summary
  - a link to the complete set of build logs
  - the name of the spin created
  - the list of individuals who have submitted code since the last round of nightly validation
  - the list of Git commits submitted by individuals

- In the event of a failure, developers who have contributed code are expected to parse build logs to fix the situation

- Example:

|image2|

**Verifying Nightly Coverity Report**
++++++++++++++++++++++++++++++++++++++++

The results from the Nightly Coverity are also provided by email

- The email will be titled "Coverity 871 Issue Report(<date>)"

- The report will contain:

  - Trend graphs on Coverity defects by priority and component
  - A break down of defects by domain
  - A list of remaining defects
  - Links to Excel and PDF Report
  - Link to the Coverity database with all the defects listed

- Example:

|image3|

.. |image0| image:: /_static/WorkInstructions/Development/RespondingToNightlyValidation_Image0.jpg
   :width: 500pt
   
.. |image1| image:: /_static/WorkInstructions/Development/RespondingToNightlyValidation_Image1.jpg
   :width: 500pt

.. |image2| image:: /_static/WorkInstructions/Development/RespondingToNightlyValidation_Image2.jpg
   :width: 300pt

.. |image3| image:: /_static/WorkInstructions/Development/RespondingToNightlyValidation_Image3.jpg
   :width: 450pt   