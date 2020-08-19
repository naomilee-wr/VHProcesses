:orphan:
|
|
|

===========================
Submit Defect Procedure
===========================

|


This procedure describes how to submit a defect. The filer of the defect is responsible for executing all the steps of this procedure.

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | Defect is discovered.                |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | Defect information                   |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | A new defect has been entered.       |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | Defect record in the "Open"          |
|                                      | *Status* has been submitted          |
+--------------------------------------+--------------------------------------+

|

**Steps**
---------

|image0| 


#. When a defect has been found, before reporting it, search the defect database to see if a defect has been filed before for the same issue.
#. If an existing defect is found, update the record with any new information.

#. If a defect record doesn't exist, create a new defect record. The following fields are required when creating a new defect:

   -  *Project*
   -  *Issue Type* (set to "Bug")
   -  *Summary*
   -  *Priority*
   -  *Severity*
   -  *Components*
   -  *Found in Versions*
   -  *Where Found*
   -  *Reporter*				

   **These additional fields should also be filled in, if known:**

   -  *Description*
   -  *Steps to Reproduce*
   -  *Workaround*
   -  *Host OS*
   -  *Processor Architecture*
   -  *Processor*
   -  *Environment*

   
   Exception: For confidential security information, a placeholder defect record may be created. This record will contain minimal information, until the issue is no longer confidential. Once the information is no longer confidential, the fields will be filled out as noted above.

   **Note:**  For definitions for specific fields in Jira, click on the ? icon next to the field within Jira. 

   **Note:**  For Security related defects, fill out the fields in the Security Tab in Jira.

#. If a defect was reported by a customer, and the submitter is in customer support, attach the Customer Support Request record. If the defect is part of an escalation, attach the Escalation record.
#. Save the defect record.

|

**Next Activity in Process**
----------------------------

+----------------------------------------+-------------------------------------------------------------+
| **Role**                               | **Activity**                                                |
+----------------------------------------+-------------------------------------------------------------+
| Technical Feature Owner                | `Triage Defect Procedure <./TriageDefectProcedure.html>`__  |
+----------------------------------------+-------------------------------------------------------------+

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
| 08/13/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Update based on Doina's feedback                                                                    |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+

.. |image0| image:: /_static/Operations/DefectManagement/DefectSubmission.jpg 