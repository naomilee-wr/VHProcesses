:orphan:

|
|
|

==================================================
Program Change Management Procedure Using Jira
==================================================

|

This procedures describes the tracking of Program Change Requests.

A Program Change Request item is written to track the impact assessment and approval of a change to the program commitment. (e.g. adding or removing features from the program, changing versions of a software component, changing the release date). The Engineering Program Manager (EPM) is responsible to see the procedure is followed.

The EPM is responsible for checking Change Requests are closed.

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | A Program Change Request exists that |
|                                      | needs to be tracked.                 |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | A Program Change Request             |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | A Program Change Request is tracked  |
|                                      | to completion.                       |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | A Program Change Request with Status |
|                                      | = Accepted, Rejected or Withdrawn.   |
+--------------------------------------+--------------------------------------+

|

**Steps**
---------

**1. File or re-open a Program Change Request**

A Program Change Request is a special type of action in the EPM tool.  Anyone may file a Program Change Request. The Tools and Templates section below describes the Change Request fields. The Change Type, Priority, Reporter, Summary, Justification, Description, Next Action and Next Action Due fields are mandatory. Descriptions of the Record fields are in the Tools and Templates section below. If the filer is not certain who to assign the action to, the action is assigned to the EPM. The status of a newly created record is Open.

A Change Request record may be returned to status = Open if the resolution was not satisfactory, or if more actions were required after the item was closed.

**2. Assign the Change Request**

The EPM assigns the Change Request, updating the record in the EPM tool.  The person assigned to Change Request performs the impact assessment.

**3. Resolve a Change Request**

The identified Key Stakeholders meet and review the impact assessment.  If the stakeholders agree that the change should proceed, then each stakeholder marks the sub-task status = Approved. Non-approvals are indicated by sub-task status = Rejected.  The results of the review are captured in the "Description" field. 

**4. Close a Change Request**

If the EPM verifies that the Change Request has been accepted by all stakeholders and all artifacts associated with the change have been updated, the EPM sets Status = Accepted.  Change Requests that are not approved are set to Status = Rejected.

|

**Tool & Template Instructions**
--------------------------------

**Jira - Program Change Request Record Template:**

.. list-table::
   :widths: 30 120
   :header-rows: 1   
   
   * - Field
     - Description
    
   * - Status
     - Status of the Change Request.  Open when created, Accepted/Rejected or Withdrawn when decision is made.
         
   * - Change Type (required)
     - Feature Add, Feature Change, Feature Remove, Schedule
         
   * - Priority (required)
     - The priority of the change.  Priority may be:
	 
       1.  Very High
	 
       2.  High
	 
       3.  Medium
	 
       4.  Low
	   
   * - Reporter (required)
     - The person entering the Change Request.
    
   * - Summary (required)
     - A brief description of the change requested.   
     
   * - Justification (required)
     - The justification for why the change is being requested.
     
   * - Description (required)
     - A more complete description of the Change Request.
     
   * - Assignee
     - The owner of the Change Request
     
   * - Next action/Next action due (required)
     - The next action item to close the Change Request and the due date.
     
   * - Sub-Tasks
     - Assign the sub-task to the stakeholder who should be the approver.

|

**Reference**
-------------
-  `Risk, Action and Issue Management <./RiskActionIssueProcedure_Jira.html>`__  

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/05/2020   | N/A                     | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 06/22/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Updates based on Doina's feedback                                                                   |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
