:orphan:
|
|
|

=============================
Defect Management Process
=============================

|

This process describes the steps in managing defect reports from submission through resolution. Defects are managed in the Defect Management System (e.g., Jira).  

The EPM is responsible for ensuring that this process is followed. 
The Bug Board is responsible for reviewing the defect record and deciding on the bug disposition.

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | - Defect has been found              |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | - Defect information                 |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | One of the following happens to the  |
|                                      | defect:                              |
|                                      |                                      |
|                                      | - The defect has been fixed and      |
|                                      |   Status is resolved and resolution  |
|                                      |   is fixed.                          |
|                                      | - The defect has been determined  not|
|                                      |   to be fixed and *Status* is set to |
|                                      |   "Resolved",                        |
|                                      |   *Resolution* is set to "Won't Fix" |
|                                      | - The defect has been determined     |
|                                      |   not to be a defect and *Status* is |
|                                      |   set to "Fixed"                     |
|                                      |   *Resolution* is set to "Rejected"  |
|                                      |   or "Withdrawn"                     |
|                                      | - The defect is determined to be a   |
|                                      |   requirement, is reclassified as    |
|                                      |   an "Enhancement Request" or "Epic" |
|                                      | - Safety Defect -- Roger Boden??     |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | -  Defect record has been updated    |
|                                      | -  The defect fix is implemented and |
|                                      |    verified                          |
+--------------------------------------+--------------------------------------+

|

**Activities**
--------------

|image0|

.. list-table::
   :widths: 10 30 120
   :header-rows: 1   
   
   * - Step #
     - Activity Name
     - Description
    
   * - 1
     - `Submit defect <./SubmitDefectProcedure.html>`__
     - Engineering or a Customer Support Engineer reports a product defect to the responsible engineering component team for resolution. 
    
   * - 2
     - `Triage defect <./TriageDefectProcedure.html>`__
     - Using minimal effort, the Domain/Technical Lead :
	 
       -  Ensures new defect records have been properly routed and adequately documented
	 
       -  Weeds out non-defects by marking the *Resolution* as "Won't Fix", "Rejected" or reclassifying the Issue Type as "Enhancement Request/Epic" 
	 
       -  Initiates timely action to address high priority defects, especially customer-reported defects. 
  
       **Note**: Anytime during the defect management process, a defect may be put "On Hold" status due to additional information required to move to the next state.

   * - 3
     - `Assign a defect to a defect assignee to be fixed <./AssignDefectFixProcedure.html>`__
     - The Engineering Manager/Technical Lead/Scrum team assigns defects to defect assignee (developer, tech writer, etc.). In the case of a customer reported defect, it may be necessary for the Domain/Technical Lead to assign the defect for resolution to ensure a timely response. 
	 
   * - 4
     - `Fix defect <./DevelopDefectFixProcedure.html>`__
     - The assigned defect assignee (developer, tech writer, etc.) creates, tests, and checks-in a fix for the defect.

   * - 5
     - `Integrate fix <./IntegrateFixProcedure.html>`__
     -  The checked-in fix is integrated and integration tests are performed. Release build includes the integrated fix.

   * - 6
     - `Verify fix <./VerifyDefectFixProcedure.html>`__
     - All fixes are verified on an "official" release build or other distribution image, according to the `Defect Fix Verification Policy <./DefectFixVerificationPolicy.html>`__. 
	 	    
   * - Parallel Activity  to 3
     - `Review defects <./BugBoardReviewProcedure.html>`__
     - The Bug Board reviews all open defects (both new and backlog) according to the `Bug Board Policy <./BugBoardPolicy.html>`__.  Once a defect has been resolved, it will not be reviewed.

   * - Parallel Activity to 2-6
     - `Evaluate/Prepare defect for publication <./PrepareDefectForPublicationProcedure.html>`__
     - Preparing a customer defect for publication is the responsibility of the defect assignee.   The decision to publish defects follows the `Defect Publication Policy <./DefectPublicationPolicy.html>`__. Development defects may optionally be published based on the recommendation of the team.
     
|

**Related Process Assets/Tools**
--------------------------------

- Defect Management system (e.g., Jira)
- `Defect Publication Policy <./DefectPublicationPolicy.html>`__
- `Submit defect <./SubmitDefectProcedure.html>`__
    
|

**References**
---------------

- `Worldwide Escalation Process <https://jive.windriver.com/docs/DOC-34980>`__
- `Customer Defects and Escalation Guidelines <https://jive.windriver.com/docs/DOC-63643>`__
   
|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1           | Martin Cote             | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 07/28/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Update based on Doina & Rodger's feedback                                                           |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+

.. |image0| image:: /_static/Operations/DefectManagement/DefectProcess.jpg 