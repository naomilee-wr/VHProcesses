:orphan:
|
|
|

==================================
Defect Fix Verification Policy
==================================

|

The purpose of the fix verification policy is to ensure that important defects that are intended to be fixed in a release are fixed.

#. All priority 1 reported defect fixes must be verified on a release build before GA, without exceptions.
#. All priority 2 and customer reported defects should be verified on a release build before GA.  Any exceptions must be documented in the defect record and approved by the Bug Board.  An email notification of the exceptions shall be sent to the key stakeholders (e.g., Tech lead of the affected area, Product Architect, EPM, PLM, Senior Management, field representatives) prior to GA.
#. If a developer has reported a defect, they are expected to follow-up and verify the fix once it is available
#. Developers should monitor defects that are assigned to them and have the state "Resolved", this indicates that the fix is ready to be validated
#. Validation can occur using any form of the product (e.g. Git, internal spin, official release)
#. Refer to the JIRA record for information on where the fix can be accessed
#. If unclear, the developer should contact the original assignee
#. Once the developer has verified that the fix does address their reported issue, the defect should be moved to the "Closed" state
#. If the current defect is fixed but a new defect is observed during verification, the current defect should be closed and a new defect should be opened. 
#. During defect verification, if the current defect fix does not address the issue/defect, the Verifier should re-open the defect.

|

**Reporting**
-------------

The following information shall be published and available for review

#. Number of fixes requiring verification
#. Number of fixes verified

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 06/29/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Updates based on Numan's feedback                                                                   |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 07/24/2020   | N/A                     | 0.3           | Shree Vidya Jayaraman   | Updates based on Martin's feedback                                                                  |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+