:orphan:

|
|
|

==================================
Integrate Defect Fix Procedure
==================================

|

Once a checked-in fix is confirmed to be present on the integration branch, the defect record is updated. The procedure ensures that integration testing has passed before the defect can be marked "Resolved"/"Fixed".

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | -  Code modifications have been      |
|                                      |    completed and the developer has   |
|                                      |    tested the fix                    |
|                                      | -  There is an integration branch to |
|                                      |    merge to                          |
|                                      | -  Modifications checked in to the   |
|                                      |    appropriate branch of the version |
|                                      |    control system                    |
|                                      | -  The integration build has been    |
|                                      |    performed                         |
|                                      | -  The integration tests for the fix |
|                                      |    have passed                       |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | -  The defect record is marked       |
|                                      |    "CHECKED IN"                      |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | -  Integration test results are      |
|                                      |    captured in the defect record     |
|                                      | -  Code is merged                    |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | -  Defect record's *Status* is set   |
|                                      |    to "RESOLVED"/"FIXED"             |
+--------------------------------------+--------------------------------------+

|

**Steps**
---------

**The** `Release Build <../CodingIntBuild/ReleaseBuildProcess.html>`__ **process will automatically move fixed records to "Resolved"/"Fixed".  This will set the "Fix Version" to the one that was built.**

|

**Variations**
--------------

In cases where the system cannot automatically move the fixed record to integrated, the CM Engineer will identify which fix records have been integrated.  They will manually move the record to "Resolved"/"Fixed" and assigned a Fix Version.

|

**Next Activity in Process**
----------------------------

+------------+--------------------------------------------------------------------+
| **Role**   | **Activity**                                                       |
+------------+--------------------------------------------------------------------+
| Tester     | `Verify Defect Fix Procedure <./VerifyDefectFixProcedure.html>`__  |
+------------+--------------------------------------------------------------------+

|

**Related Process Assets/Tools**
--------------------------------

- Defect Management system (e.g., Jira)
- `Defect Management Process <./DefectManagementProcess.html>`__
    
|

**References**
-----------------

- ??

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1           | Martin Cote             | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+