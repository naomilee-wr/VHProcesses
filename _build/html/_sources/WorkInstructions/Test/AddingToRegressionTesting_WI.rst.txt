:orphan:

====================================
Adding to Regression testing
====================================

**Purpose:** As teams develop new Features, they are also responsible for adding new test cases into the overall VxWorks 7 regression test suites.  The following document outlines the process for updating the VxWorks 7 regression test suite.


**Procedure**
--------------

- Each VxWorks 7 development team has approached regression testing slightly differently.  Over the years, the Test Team has aggregated the various test suites and now executes these on a Nightly basis.
  
  - Given the origins of the VxWorks 7 regression test suite, the procedure for adding new test cases can be slightly different from team to team.
  - Typically however, the process will involve teams adding new test cases and updating matrices in WASSP Git Repos

- It has traditionally been the Test Team's responsibility for adding new test cases to regression testing.  As of SR0520+, this responsibility now falls onto the separate Scrum Teams.
  
  - The Test Team had explicit Features/Epics in Jira Agile for each release to track this work (e.g. F9259?? for SR0510).  These features/epics will no longer be created.

- Ideally, as teams deliver code into the "vx7-integration" branch, they should also be adding to their regression testing suites
  
  - Scrum Teams should be creating their own Stories (or tasks) to track the integration
  - Teams should NOT be waiting until Feature Complete to do the integration, they must be doing it throughout feature development
  - There may be a small lag in delivering some of the test cases (Feature/Epic completion will not be gated on test integration)

- New Features which do not add new test cases into the VxWorks 7 Regression Test Suites will be scrutinized
 
  - A Feature/Epic cannot be providing new functionality and yet not have some new test case being created!
  

|

**Change Log**
--------------

+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/16/2020     | N/A            | 0.1            | Naomi Lee      | Transferred content from  Adding to   |
|                |                |                |                | Regression testing Jive page          |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/29/2020     | N/A            | 0.2            | Shree Vidya    | Updates based on Numan's feedback     |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+