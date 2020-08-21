:orphan:

|
|
|

================================
Develop Defect Fix Procedure
================================

|

When the defect fixer has acknowledged the defect is valid, the defect fix development process begins. The objective of the process is to ensure that the developed fix is correctly tracked in the defect tracking system and checked-in to Configuration Management system.

The defect fixer is responsible for this procedure.

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | -  Defects are in "Open" *Status*    |
|                                      | -  Defect is assigned to defect      |
|                                      |    fixer                             |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | -  Defect records in the defect      |
|                                      |    tracking system                   |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | -  Modifications checked in to the   |
|                                      |    appropriate branch of the         |
|                                      |    Configuration Management system   |
|                                      | -  Defect fixer has tested the fix   |
|                                      | -  Defect is in *Status* "Open",     |
|                                      |    either Priority 1 or 2, and may   |
|                                      |    need to be released with the      |
|                                      |    product, or to be reviewed by     |
|                                      |    the Bug Board                     |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | -  Defect has been fixed with        |
|                                      |    *Status* set to "CHECKED IN",     |
|                                      |    and the details of the fix        |
|                                      |    recorded                          |
|                                      | -  The defect fix                    |
+--------------------------------------+--------------------------------------+

|

**Steps**
---------

#. **Understand the problem**

   -  Study the defect *Summary*, *Description*, *Internal Description* and *Steps to Reproduce* to understand both the expected and observed behavior.

   -  Identify and resolve any ambiguities and gaps in the recorded descriptions, contacting the submitter if necessary, then *Edit* and *Update* the defect to record changes made.

   -  Reproduce the problem and isolate the cause.

#. **Reject a defect**

   -  If the reported defect is a true defect but will not be fixed, set it to Won't Fix and enter a reason in the *Comment* field.

   -  To reject the defect, add justification for rejecting the defect and assign the defect back to the submitter.  Request the submitter to withdraw the defect

#. **Optionally, consider alternative solutions, select the appropriate one, and estimate the effort.**

   -  If the estimate is unexpectedly large, notify the Component Lead (Domain/Technical/Feature Lead) before moving the defect record to the "In Progress" state.

   -  Edit the defect and record your estimate in the *Estimated Effort* field

#. **Develop the fix**

   -  Move *Status* to "In Progress" by clicking the "Start Progress" button

   -  Correct the defect

   -  Unit test the fix

   -  Update any related specifications or data affected by the fix

   During development of the bug fix, the following change in status may be possible:

   -  A defect may be re-evaluated by the developer and Component Lead (Domain/Technical/Feature Lead) if they determine that the commitment to fix cannot be satisfied. In this case, the defect is returned to the Bug Board or defect originator for re-evaluation.

   -  If work on a defect has to be postponed, the defect is set to On Hold to notify Key Stakeholders of the temporary delay in developing the fix.  (For example, developer temporarily reassigned to higher priority defect)

#. **Review the defect fix according to the** `Code Review <../../CoreDev/CodingIntBuild/PeerReviewProcedure_CodeCollaborator.html>`__ **process**

#. **The** `Release Build <../../CoreDev/CodingIntBuild/ReleaseBuildProcess.html>`__ **process will automatically move fixed to the** *"checked in"* **state**

   -  Include any details regarding the fix.
   
|

**Variations**
--------------

**Fixing a defect in an external component**

-  If the defect is to be resolved in an external component, such as Open Source or other component that is not directly under our control, the defect status is set to "On-hold" -> "Waiting for Vendor"

-  The defect is then fixed in the external (non-product) location and made available to the team.

-  When that code is integrated, there is no automatic updates to the defect records.

-  When the defect filer/developer/tester identifies that the defect is no longer present, the defect record is manually moved to the "Fixed" resolution and a comment is added indicating why it was moved to fixed.

**Rerouting the defect to another Component**

-  If while working on the fix the defect fixer determines that the root of the defect is in another Component's code, the defect fixer or Component Lead should reroute the defect to the correct team.

   -  If the new component is in the same project, then the defect can be edited and the component and assignee changed.

   -  If the new component is in a different project, the defect must be "Moved" to the appropriate project:

      -  Select the defect to be moved

      -  Click on *More Actions -> Move*

      -  Select the new project and update any other fields as necessary

      -  Click on *Move*

|

**Next Activity in Process**
----------------------------

+---------------+--------------------------------------------------------------------+
| **Role**      | **Activity**                                                       |
+---------------+--------------------------------------------------------------------+
| Integrator    | `Integrate Defect Fix Procedure <./IntegrateFixProcedure.html>`__  |
+---------------+--------------------------------------------------------------------+

|

**Related Process Assets/Tools**
---------------------------------
- Defect Management system (e.g., Jira)
- `Defect Management Process <./DefectManagementProcess.html>`__
    
|

**References**
-----------------
- ??

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                  |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1           | Martin Cote             | Initial Draft                                                    |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
| 08/21/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Updated the links based on Shawn's feedback                      |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
|              |                         |               |                         |                                                                  |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
|              |                         |               |                         |                                                                  |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+

