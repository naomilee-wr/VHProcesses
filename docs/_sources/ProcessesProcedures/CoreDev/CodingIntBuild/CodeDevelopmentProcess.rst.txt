:orphan:

|
|
|

===========================
Code Development Process
===========================

|

This process describes how product code is developed. 

|

+--------------------------------------+-----------------------------------------+
| **Entry Criteria**                   | - Feature/Epic requirements ready for   | 
|                                      |   development - Stories are available   |
|                                      |   and ready for implementation          |
|                                      | - The design process has progressed     |
|                                      |   sufficiently for generation of code   |
|                                      |   using the appropriate coding standard.|
+--------------------------------------+-----------------------------------------+
| **Inputs**                           | - Requirements/Stories, HLDs, and Coding|
|                                      |   Standards                             |
+--------------------------------------+-----------------------------------------+
| **Exit Criteria**                    | - Code is checked in to the CM system   |
+--------------------------------------+-----------------------------------------+
| **Outputs**                          | - Committed code, associated test code  |
|                                      |   for the Feature(Epic), and passed test|
|                                      |   results                               |
|                                      | - Stories marked done and accepted in   |
|                                      |   the Requirments Management System     |
+--------------------------------------+-----------------------------------------+

|

**Stakeholders**
-----------------	
+------------------------+-------------------------------------------------------------------------------+
| **Role**               | **Responsibilities**                                                          |
+------------------------+-------------------------------------------------------------------------------+
| Scrum Team             | Scrum team includes Technical Feature Owner, Engineering Manager (Development |
|                        | & Test), Development Engineer, Test Engineer, Information Development         |
|                        | Engineer.                                                                     |
|                        |                                                                               |
|                        | Responsible for:                                                              |
|                        |                                                                               |
|                        | - reviewing the Requirements/Stories and HLDs, if available                   |
|                        | - writing code according to the coding standards and design from HLD, if      |
|                        |   available                                                                   |
|                        | - writing unit test code, and customer facing documentation                   |
+------------------------+-------------------------------------------------------------------------------+

|

**Activities**
--------------

|image0|

|

.. list-table::
   :widths: 10 30 120
   :header-rows: 1   
   
   * - Step #
     - Activity Name
     - Description
      
   * - 1
     - Develop Code
     - Using Stories and designs as inputs, Developers write code according to `coding standards <../../../ProcessDocuments/CoreDev/CodingIntBuild/WindRiverVxWorksCodingStandard.pdf>`__ and design according to the HLDs if available, run static code analysis(e.g., Coverity), and also address compiler warnings and fix defects. 
    
   * - 2
     - Develop unit tests
     - Developers write unit tests to generate code.  See `Development (Unit) Testing Process <./DevUnitTestingProcedure.html>`__.  

   * - 3
     - Test code
     - Developers perform the unit and any applicable regression tests and fix defects.   

   * - 4
     - Review code
     - Developers review code and ensures full traceability according to the `Peer Review Procedure using Code Collaborator <./PeerReviewProcedure_CodeCollaborator.html>`__.

       If the review finds code issues, Developer fixes issues found in the review, retest, and re-review the fixed code.

       If the review finds problems with existing design, Developers return to the `Design Process <../Design/DesignProcess.html>`__. 

       During the review, the Technical Feature Owner and Developer may determine a design (if one not already avaialble) is necessary to review the code. Technical Feature Owner or Developer creates a HLD according to the `Design Process <../Design/DesignProcess.html>`__.  
	   
   * - 5
     - Submit/Check in code
     - Developers submit/check in code according to the `Check-in Procedure <./CheckinProcedure.html>`__.    
	 
       The relevant Stories and Tasks are marked completed. 

|

**Related Process Assets/Tools**
--------------------------------

- `VxWorks Coding Standard <http://bitbucket.wrs.com/projects/VX7/repos/codingstandard/browse>`__
- `Coding Standards <../../../ProcessDocuments/CoreDev/CodingIntBuild/WindRiverVxWorksCodingStandard.pdf>`__     **Draft version updated but not reviewed/approved**

  - `Coding Style Guide <../../../ProcessDocuments/CoreDev/CodingIntBuild/WindRiverVxWorksCodingStyleGuide.pdf>`__
  - `Coding Rules Guide <../../../ProcessDocuments/CoreDev/CodingIntBuild/WindRiverVxWorksCodingRulesGuide.pdf>`__
  
- `Devlopment Unit Test Process <./DevUnitTestingProcedure.html>`__
- `Peer Review Procedure Using Code Collaborator <./PeerReviewProcedure_CodeCollaborator.html>`__
- `VxWorks: Submitting code into the Integration Branch <../../../SupplementaryGuidelines/Development/SubmitCodeIntegrationBranch_SG.html>`__
- `VxWorks: Submitting code into a Release Branch <../../../SupplementaryGuidelines/Development/SubmitCodeReleaseBranch_SG.html>`__
- `VxWorks: Submitting code into the SRO5XX Maintenance Branch <../../../SupplementaryGuidelines/Development/SubmitCodeMaintenanceBranch_SG.html>`__
- Engineering Requirements Management system (e.g., Jira Agile)
- Configuration Management system (e.g., Git)
- Peer Review system (e.g., Code Collaborator)
   
|

**References**
---------------

- `VxWorks Pull Request Submission Template <../../../ProcessDocuments/CoreDev/CodingIntBuild/PullRequestChecklistTemplate_v5.xlsx>`__

Note: For additional references, refer to `"Supplementary Guidelines" <../../SupplementaryGuidelinesIndex.html#development>`_ section. 
  
|

**Change Log**
--------------

+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**  | **Version**   | **Change By**           | **Description**                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 04/30/2020   | N/A                    | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                       |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 06/10/2020   | N/A                    | 0.2           | Shree Vidya Jayaraman   | Update based on Kitty's feedback                                                    |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 06/22/2020   | N/A                    | 0.3           | Shree Vidya Jayaraman   | Update based on Kitty's feedback                                                    |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 07/01/2020   | N/A                    | 0.4           | Shree Vidya Jayaraman   | Update based on Kitty's feedback                                                    |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 07/22/2020   | N/A                    | 0.5           | Shree Vidya Jayaraman   | Update based on Kitty's feedback                                                    |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+

.. |image0| image:: ../../../_static/CoreDev/CodingIntBuild/CodeProcess.jpg