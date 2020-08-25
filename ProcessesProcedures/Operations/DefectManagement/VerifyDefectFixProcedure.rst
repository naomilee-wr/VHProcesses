:orphan:

|
|
|

===============================
Verify Defect Fix Procedure
===============================

|

Verify that the fix has been properly integrated into the integration or release branch.  The defects must be verified in the release builds.  

Verify that the fix has resolved the defect.  Per the `Defect Fix Verification Policy <../DefectManagement/DefectFixVerificationPolicy.html>`__, verification applies to priority 1 and 2 and customer reported defects.  

**<<Discuss the defect verification policy and this procedure with Dev SMEs>>**

The Defect Reporter, or Test Lead is responsible for this procedure.

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | -  Fix has been integrated           |
|                                      | -  There is a release build to test  |
|                                      | -  Defect is ready for verification  |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | -  Defect records are Integrated     |
|                                      |    indicating that fixes are ready   |
|                                      |    for verification                  |
|                                      | -  Updated defect record             |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | -  The fix has been verified         |
|                                      | -  Defect record is updated with     |
|                                      |    verification information          | 
+--------------------------------------+--------------------------------------+
|                                      | -  The fix has passed verification   |
|                                      |    and defect is closed via the      |
|                                      |    *Closed* button.                  |
| **Outputs**                          | -  The fix has failed verification   |
|                                      |    and defect is reopened via the    |
|                                      |    *Restart* button.                 |
+--------------------------------------+--------------------------------------+

|

**Steps**
---------

#. **Determine what fixes to verify**
#. **Obtain the current release build to test**
#. **Review the defect** *Description, Internal Description,* and *Steps to Reproduce*
#. **If there are duplicate defects,** review the *Description, Internal Description*, and *Steps to Reproduce* of each duplicate.
#. **Follow the** *Steps to Reproduce* **listed in the defect and any duplicate defects to test the fix.** Duplicate defects may list significantly different descriptions and ways to reproduce a defect.
#. **If verification fails,** reopen the record

   -  Click on *Restart* button
   -  Record any details about the test failure in the *Comment* field
   -  The defect fixer is notified of the failure.

#. **If verification passes,** close the defect record

|

**Related Process Assets/Tools**
---------------------------------

- Defect Management system (e.g., Jira)
- `Defect Management Process <./DefectManagementProcess.html>`__
- `Defect Fix Verification Policy <./DefectManagement/DefectFixVerificationPolicy.html>`__
    
|

**References**
--------------

- Refer to `Supplementary Guidelines <../../../SupplementaryGuidelines/SupplementaryGuidelinesIndex.html#requirements>`_ 

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1           | Martin Cote             | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 08/25/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Update to based on Rodger & Doina's feedback                                                        |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+