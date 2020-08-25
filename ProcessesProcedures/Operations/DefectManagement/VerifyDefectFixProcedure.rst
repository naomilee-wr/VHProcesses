:orphan:

|
|
|

===============================
Verify Defect Fix Procedure
===============================

|

Verify that the fix has been properly integrated into either the development tree or the targeted release.  If the product does not currently have release builds (i.e., still in development), it should be verified in the development tree.  If there are release builds, it must be verified in the release build.  Release builds incorporate prior fixes and their verifications, including those in the development tree, due to the iterative nature of the development process.  

Verify that the fix has resolved the defect.  Per the `Defect Fix Verification Policy <../DefectManagement/DefectFixVerificationPolicy.html>`__, verification applies to priority 1 and 2 and customer reported defects.   

The Defect Reporter, or Test Lead is responsible for this procedure.

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | -  Fix has been integrated           |
|                                      | -  For release builds, there is a    |
|                                      |    release build to test             |
|                                      | -  Defect is ready for verification  |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | -  Defect records are Integrated     |
|                                      |    indicating that fixes are ready   |
|                                      |    for verification                  |
|                                      | -  Updated defect record             |
|                                      | -  For release builds, there is a    |
|                                      |    release build to test             |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | -  The fix has been verified         |
|                                      | -  The fix has failed verification   |
|                                      |    and defect is reopened via the    |
|                                      |    *Restart* button.                 |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | -  Defect record is updated with     |
|                                      |    verification information          |
+--------------------------------------+--------------------------------------+

|

**Steps**
---------

#. **Determine what fixes to verify**
#. **Obtain the development tree or current release build to test**
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

-  ??

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1           | Martin Cote             | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.2           | Martin Cote             | Update to based on Rodger's feedback                                                                |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+