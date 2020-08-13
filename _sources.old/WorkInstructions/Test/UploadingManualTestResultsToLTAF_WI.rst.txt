:orphan:

=======================================
Uploading Manual Test Results to LTAF
=======================================

**Purpose:** 
------------

Some code submissions may be very simple and do not require heavy testing.  The following procedures presents a simplified method for uploading test results in situations where developers opt to do quick manual tests.


**Procedure:**
---------------

This procedure is acceptable when the submission is:

- Benign
- Generally small in size
- Has very limited (or no) interactions with other parts of the system
- Can not effectively be tested without completing other parts of the Feature

1. Import the Jira Agile Story into LTAF

- In Jira Agile, set the "Testing Required" field for the Story being submitted to "Yes":

|image0|

- Log into `LTAF <http://pek-lpgtest3.wrs.com/ltaf/welcome.php>`__ using your UNIX credentials
- Set the release to the current one (in the top right corner):

|image1|

- Click on the "Requirements" link
- Import your US into LTAF using the combo box menu at the bottom of the page:

|image2|

- Once completed, you should see your US listed in the table along with its parent Feature

2. Upload Test Case Meta-data into LTAF

- Create a new test case meta-data file (i.e. test_case.conf)
- Fill-in the following template (with information appropriate for your manual test)

.. code-block:: rst
	
	[TEST_CONFIG]

    TEST_SUITE_NAME = <name of the test suite>

    COMPONENT= <component name, should match other test cases done by the team>

    TEST_CASE_TYPE = Functional

    FEATURE = <functional area, should match other test cases done by the team>

    AUTOMATION = no

    RCA = no

    DESCRIPTION = "<description of the test you performed>"

    TRACEABILITY =

    TEST_CASE_LIST = "<name of manual test #1> <name of manual test #2> <name of manual test #3>"

 
    GIT_LINK =

    CREATED_DATE =

    RELEASE_NAME =

- Upload the test case meta-data using the following command:

.. code-block:: rst
	
	curl -F testfile=@test_case.conf http://pek-lpgtest3.wrs.com/ltaf/upload_test.php

3. Upload Test Results into LTAF

- Create a new test run results file (i.e. tr_result.ini)
- Fill-in the following template (with information appropriate to your manual test)

.. code-block:: rst
	
	[LTAF]

	action = add_update

	release_name = <name of the release you are testing for, e.g. vx7-SR0510-features>

	test_component = <component name, should match what was put in test case meta-data>

	sprint = <name of the sprint, e.g. Sprint 24 - Ending 21 July 2017>

	week = <week in the sprint the testing occurred, e.g. week3>

	domain =  <team’s domain, should match previous test runs>

	log = <path to test logs if you have any>

	tester = <your user ID>

	build = <PASS or FAIL>

	requirements = <the User Story ID setup in step #1>

	function_pass = 1

	function_fail = 0

	test_suite = <test suite name used in step #2>

	test_name = <test case name used in step #2>

	status = <PASS or FAIL>

- Upload the test result using the following command:

.. code-block:: rst
	
	curl -F resultfile=@tr_result.ini  http://pek-lpgtest3.wrs.com/ltaf/upload_results.php
	
|

**Change Log**
--------------

+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/16/2020     | N/A            | 0.1            | Naomi Lee      | Transferred content from  Uploading   |
|                |                |                |                | Manual Test Results to LTAF Jive page |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/29/2020     | N/A            | 0.2            | Shree Vidya    | Updates based on Numan's feedback     |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+

.. |image0| image:: /_static/WorkInstructions/Test/UploadingManualTestResultsToLTAF_Image0.jpg
   :width: 100pt
   
.. |image1| image:: /_static/WorkInstructions/Test/UploadingManualTestResultsToLTAF_Image1.jpg
   :width: 200pt
   
.. |image2| image:: /_static/WorkInstructions/Test/UploadingManualTestResultsToLTAF_Image2.jpg
   :width: 200pt