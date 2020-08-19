:orphan:
|
|
|

=========================================
Creating Feature Test Plan Guideline
=========================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

**Purpose:**

For every Feature/Epic that a team will be releasing, a test plan must be authored, reviewed and accepted.  A test plan can cover more than one Feature/Epic.   

(Source: https://jive.windriver.com/docs/DOC-58077)
|

**Important References**
-------------------------

- `Test Process Guideline <../../ProcessesProcedures/CoreDev/Verification/TestProcessGuideline.html>`__
- `Feature Test Plan Template <../../ProcessDocuments/CoreDev/Verification/FeatureTestPlanTemplate.docx>`__

|
 
**Guidelines**
--------------

- All Feature Test Plans must take into account Multi-Version Testing

  - The general strategy and test process to be followed is outlined in: The specified item was not found.
  - If multi-version testing is not required (for example, if the team is delivering new RPMs) then it must be clearly and explicitly indicated in the Feature Test Plan
  
- Feature Test Plan must identify/include the following:
  
  - test environment
  - risks and dependencies
  - test cases that need to be created
  - existing test cases that should be rerun before code submission.
  - impact on other areas, e.g. performance, footprint, etc. to ensure these are checked.
  - test results location
  - defects related to the feature
  

- It's important to note that:

  - Feature Test Plans must be reviewed the Feature Architect (Product Architect) and the Lead Feature Developer (unless the Lead is the author.
  - Feature Test Plans must be uploaded before the Feature/Epic's merge date.
  - All automated feature/epic tests should be added into nightly regression Suite.
  
|

**Change Log**
--------------

+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/25/2020     | N/A            | 0.1            | Shree Vidya    | Transferrred content from Creating a  |
|                |                |                | Jayaraman      | Feature Test Plan Jive page           |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/29/2020     | N/A            | 0.2            | Shree Vidya    | Updates based on Numan's feedback     |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 08/04/2020     | N/A            | 0.3            | Shree Vidya    | Updates based on kitty's feedback     |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+

