:orphan:

|
|
|

====================================
Scrum Tester Responsibilities
====================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

**Purpose:**

(Source: https://jive.windriver.com/docs/DOC-74086)

**Grooming Phase**
------------------

- Study feature requirement in parallel with developer
- Study specifications if applicable (RFC, etc)
- Study new hardware overview pictures if applicable 
- Study new 3rdparty libraries and related CVE if applicable 
- Test strategy checklist

  - Hardware coverage
  - Conformance testing (ANVL, etc.)
  - Automation method (WASSP, VxTest, KONG, MEFA, etc.)
  - Dependencies
  - Performance
  - Kernel Space and user space coverage
  - Avoid use simulator as soon as possible (VxSIM and Simics)
 
- Build up a clear test criteria, or how to test/demo the US


**Planning Phase**
------------------

- Tester make commitment on sprint planning meeting base the feature testing estimation.

- If tester could not commit, the feature should not be committed.


**Development Phase**
---------------------
- Write Test Plan using template (note: Jive page/ppt has url to https://jive.windriver.com/docs/DOC-73974, but the link is returning an error)
- Test Plan review (PT, Developer as reviewer, Release prime as observer):  http://codereview.wrs.com/ui#review:id=55761
- Import User story to LTAF:  http://pek-lpgtest3.wrs.com/ltaf/requirement.php
- Update test meta data (note: Jive page/ppt this link https://jive.windriver.com/docs/DOC-48869, but the link is returning an error)
- Sync test cases to LTAF (http://pek-lpgtest3.wrs.com/ltaf/test_case.php)
- Execute test cases
- Update test case status in LTAF (http://pek-lpgtest3.wrs.com/ltaf/test_results.php)
- Update DoD with LTAF links (http://pek-lpgtest3.wrs.com/ltaf/erpt.php)
- Create defects

  - Labeling new feature ID and Steps to reproduce following publish guideline
  - Steps to reproduce - Isolate to simple steps, remove automation tools, framework related works which could be understood by customer

**Post Feature Complete**
--------------------------

- Regression test for new feature on release spin before CCB running.
- Defect Verification on release spin before CCB running.
- Deliver new feature automation test cases before GA (WASSP, VxTest, KONG, MEFA, etc
- Review the readme and knowledge libraries update for new feature before GA 

**Test Improvement**
---------------------
- TSR defect RCA and test coverage improvement
- Test GAP improvement

**Meetings and White Board**
-----------------------------
- Daily stand-up meeting
- Grooming meeting
- Sprint Planning meeting
- Sprint retrospective meeting
- User Stories DOR, DOD, Tasks - Update on time

.. image:: /_static/SupplementaryGuidelines/Test/ScrumTesterResponsibilities_Image0.jpg
   :width: 300pt