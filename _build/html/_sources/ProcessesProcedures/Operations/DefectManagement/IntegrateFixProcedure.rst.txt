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
| **Entry Criteria**                   | - Code modifications have been       |
|                                      |   completed and the developer has    |
|                                      |   tested the fix                     |
|                                      | - There is a CM branch (integration  |
|                                      |   or release branch) to merge to     |
|                                      | - Modifications checked in to the    |
|                                      |   appropriate branch of the version  |
|                                      |   control system                     |
|                                      | - The integration build has been     |
|                                      |   performed                          |
|                                      | - The integration tests for the fix  |
|                                      |   have passed                        |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | - The defect record is marked        |
|                                      |   "CHECKED IN"                       |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | - Integration test results are       |
|                                      |   captured in the defect record      |
|                                      | - Code is merged                     |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | - Defect record's *Status* is set    |
|                                      |   to "Status = RESOLVED", Resolution |
|                                      |   = "FIXED"                          |
+--------------------------------------+--------------------------------------+

|

**Steps**
---------

Once the defect has been included in a release build, the Developer will update state to "Resolved" and set the "Fix Version" to the release that was built-in.

Refer to `Release Build <../../CoreDev/CodingIntBuild/ReleaseBuildProcess.html>`_ process.

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

- Refer to `Supplementary Guidelines <../../../SupplementaryGuidelines/SupplementaryGuidelinesIndex.html#requirements>`_  

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                  |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1           | Martin Cote             | Initial Draft                                                    |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
| 08/21/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Fixed the link based on Shawn's feedback                         |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
| 08/25/2020   | N/A                     | 0.3           | Shree Vidya Jayaraman   | Fixed the link based on Rodger & Doina's feedback                |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
|              |                         |               |                         |                                                                  |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+
|              |                         |               |                         |                                                                  |
+--------------+-------------------------+---------------+-------------------------+------------------------------------------------------------------+

