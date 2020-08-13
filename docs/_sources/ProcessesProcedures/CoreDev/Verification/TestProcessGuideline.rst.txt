:orphan:
|
|
|

=====================================
Test Process Guideline
=====================================

|

This document provides guidelines for feature testing, release testing, nightly testing, weekly testing, sprint testing, EAR, CR testing, test coverage, test criteria and test defect related policy.

|

**Feature Testing**
-------------------
The new feature testing, mainly include what will be tested (feature test plan) and when the test should be finished according to the release schedule. Feature delivery/entry criteria follow release criteria.

**Feature Test Plan**
~~~~~~~~~~~~~~~~~~~~~

- Feature test plan is required for features which need create new TCs, for those features which could be covered by exist regression tests the test plan is optional

- Feature test plan must follow VxWorks feature test plan template

- Feature test plan must be reviewed with code collaborator; reviewer need involve Dev, Test, PM, EPM and other related stakeholders 

- Feature test plan must be finished and reviewed before feature merge into integration branch 

- Feature test plan document link should be added into Jira feature test plan field

**Feature Test Report**
~~~~~~~~~~~~~~~~~~~~~~~

- Feature test result must be imported into LTAF before the feature merged into integration branch

- New feature test result includes new feature test and regression test, both test results could be imported into LTAF and show out in ERPT

|image0|

**Feature Test Case Delivery**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Test case for new feature should be created according to test case user guidelines and add test case meta data according to meta data guideline

- New feature test case delivery will be tracked with LTAF test case report release by release

|

**Release Testing**
-------------------

The release testing, mainly include what will be tested (release test strategy) and when the test should be finished (release test plan in LTAF) according to the release schedule. Release test exit criteria refer to release GA criteria.

Release testing include regression testing, new feature integration testing and system testing (all testing are using features track in Jira) and the test covered Vx7, WB, Compiler, HV etc.

- Release testing will start after spin generated with all features included

- Release testing is fixed duration (currently 3 weeks test cycle)

- Release testing is tracked with Jira epics and LTAF report

- Release test plan will be created in LTAF before the release test start

- Release test status update report will be sent to “vx7-project” periodically

- Performance and footprint report will provide by the end of the second week of the release test cycle for PT and related stakeholders for review

- Release summary document will be created 1 week after GA and upload to VxWorks document as code website 

- CR and EAR release test report should be in LTAF and ERPT 


**Release Test Strategy**
~~~~~~~~~~~~~~~~~~~~~~~~~~

- Release test strategy is required for each SR release

- Release test strategy must follow VxWorks release test strategy template 

- Release test strategy must be ready for review 2 weeks before release testing started

- Release test strategy must be reviewed with code collaborator, involve Dev lead, Test lead, PM, EPM and related stakeholders 

- Release test strategy must be upload into Jive VxWorks test space


**Release Test Report**
~~~~~~~~~~~~~~~~~~~~~~~~

- Release test results need to be reviewed by the key stakeholders (e.g., Architects, Development and Test Leads)
- Release test result must be imported into LTAF and show out in ERPT
- For EAR/CR, test strategy and test plan are optional, test result need in LTAF and ERPT

|image1|

|


**Integration Testing**
------------------------

Integration testing includes:

- Nightly regression test
- Weekly regression test
- Sprint regression test

New test cases for new features will be added into nightly, weekly or sprint regression test

**Nightly Test**
~~~~~~~~~~~~~~~~~

Nightly Test Strategy
``````````````````````
- Full nightly test (include 5As and real target) on native spin

- 5As nightly test on both native and Helix spin

Nighty Test Report
```````````````````
- Submit “vx7-project” to receive the nightly report of VxWorks

|image2|

**Weekly Test** (Native only)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Weekly Test Strategy
``````````````````````
- Execute all automation regression tests every week


Weekly Test Report
```````````````````
- Weekly test report could be accessed from LTAF

|image3|


**Sprint Test** (Native only)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sprint Test Strategy
``````````````````````
- Execute all automation test and selected manual tests every sprint

- 1-day exploratory test for each sprint


Sprint Test Report
```````````````````
- Sprint test report could be accessed from LTAF and ERPT

|image4|

|

**Test case defect policy**
-----------------------------

- Test case issue will be reported with Jira defect and follow `Defect Management process <../../Operations/DefectManagement/DefectManagementProcess.html>`__

- Test case type defined in `test case meta data guideline <././TestCaseMetadatafileUsageGuideline.html>`__


**Test Coverage and Improvement**
-----------------------------------

- Test improvements are tracked with Jira epics and follow agile development process.

- Test case coverage and code coverage will be measured as below:

  - Test case coverage report will be generated in LTAF and tracked release by release

|image5|

  - Target coverage report will be generated in LTAF and tracked release by release (Native only)

|image6|

  - VxWorks code coverage data will be generated via Simics tool (Native only)
  
  http://pek-cc-pb08l.wrs.com/vxtest/vxtest1/LOG_VX7/Vx-7_CodeCoverage/report_SR06xx.html

|image7|

**Test Log Backup Policy** (Native only)
-----------------------------------------

- Test logs will follow company IT back up policy, all test logs will be backed up by IT. 
- VxWorks 7 new feature and release test logs location: http://pek-cc-pb08l/vxtest/vxtest1/LOG_VX7/
- VxWorks 7 Test Release and Feature test log backup policy: https://jive.windriver.com/docs/DOC-84463

|

References 
-----------------

- `VxWorks Test Case Meta Data File (test_case.conf) Usage Guideline (recovered version) <./TestCaseMetadatafileUsageGuideline.html>`__
- `VxWorks test document Jive location <https://jive.windriver.com/community/engineering/operation-system-common-platforms/teams/vxworks/vxworks-test>`__
- `VxWorks Release <http://pek-vx-doc.wrs.com/release/index.html>`__
- `VxWorks test suite users guide <https://docs.windriver.com/bundle/vxworks_7_regression_test_suite_users_guide_sr0640/page/age1452734308978.html>`__


**Change Log**
--------------

+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 05/20/2020     | N/A            | 0.1            | Shree Vidya    | Initial Draft                         |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 08/04/2020     | N/A            | 0.3            | Shree Vidya    | Updates based on kitty's feedback     |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+


.. |image0| image:: ../../../_static/CoreDev/Verification/LTAF_TestReport_Epic.jpg
.. |image1| image:: ../../../_static/CoreDev/Verification/LTAF_TestReport_Domain.jpg
.. |image2| image:: ../../../_static/CoreDev/Verification/LTAF_TestReport_Nightly.jpg
.. |image3| image:: ../../../_static/CoreDev/Verification/LTAF_TestReport_Weekly.jpg
.. |image4| image:: ../../../_static/CoreDev/Verification/LTAF_TestReport_Sprint.jpg
.. |image5| image:: ../../../_static/CoreDev/Verification/LTAF_TestReport_Coverage1.jpg
.. |image6| image:: ../../../_static/CoreDev/Verification/LTAF_TestReport_Coverage2.jpg
.. |image7| image:: ../../../_static/CoreDev/Verification/LTAF_TestReport_Coverage3.jpg