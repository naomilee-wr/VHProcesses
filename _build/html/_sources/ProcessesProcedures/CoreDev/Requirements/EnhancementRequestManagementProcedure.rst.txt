:orphan:
|
|
|

==========================================
Enhancement Request Management Process
==========================================

|

The purpose of the Enhancement Request Management procedure is to evaluate Enhancement Requests (ER) in the Defect Management Tool (e.g., Jira) as possible requirements. ERs are regularly reviewed and evaluated at Enhancement Request review meetings.  The meeting’s purpose is to review ERs that are new in the system, as well as existing ones that are still under discussion.

The Customer Service Organization (CSO) is responsible for submitting the ER and holding review meetings.

+--------------------------------------+--------------------------------------------------+
| **Entry Criteria**                   | An ER has been found and is in *Status* “Open”   |
+--------------------------------------+--------------------------------------------------+
| **Inputs**                           | ER record in the Defect Tracking System          |
|                                      | (e.g., Jira)                                     |
+--------------------------------------+--------------------------------------------------+
| **Exit Criteria**                    | The Enhancement Request record *Type* changed to |
|                                      | "Epic" or "Defect"                               |  
+--------------------------------------+--------------------------------------------------+
| **Outputs**                          | Updated Enhancement Request record               |
|                                      |                                                  |
|                                      | - *Type* changed to "Defect"                     |
|                                      | - Marked Duplicate                               |
|                                      | - "Rejected" or "Withdrawn" with explanation     |
|                                      | - If accepted, Type changed to "Epic"            |
+--------------------------------------+--------------------------------------------------+

|

**Stakeholders** 
-----------------	

+-------------------------+-------------------------------------------------------------------------------+
| **Role**                | **Responsibilities**                                                          |
+-------------------------+-------------------------------------------------------------------------------+
| Customer Service        |  Responsible for Submitting the ER and holding review meetings                |
| Organization            |                                                                               |
+-------------------------+-------------------------------------------------------------------------------+
| Key Stakeholders        |  Key Stakeholders (Product Manager, Engineering Manager, Technical Feature    |
| / Scrum Team            |  Owner) and/or Scrum team are responsible for reviewing the ER.               |
+-------------------------+-------------------------------------------------------------------------------+

**Activities**
---------------

|image0|

.. list-table::
   :widths: 10 30 120
   :header-rows: 1   
   
   * - Step #
     - Activity Name
     - Description  
	 
   * - 1
     - Submit enhancement request(s)
     - When an ER is requested, before creating a new record, search the Tracking System (e.g., Jira) to see if an ER has been filed before for the same issue. 

       -  *Project*
       -  *Issue Type* (set to "Enhancement Request")
       -  *Summary*
       -  *Priority*
       -  *Severity*

       **These additional fields should also be filled in, if known:**

       -  *Description*
       -  *Workaround*
       -  *Components*
       -  *Found In Versions*
       -  *Salesforce Case Reference* (for customer requested ERs)

  
   * - 2
     - Review enhancment request(s) - Search enhancement request(s)
     - Identify new enhancement request (ER) record(s) by reviewing e-mail notifications from the Defect Tracking System (e.g., Jira) or running queries. Identify relevant enhancement request records in *Status* "Open"
    
   * - 2a
     - Review enhancment request(s) - Examine the enhancement record
     - Review the *Summary* and *Description* to determine if it describes:
	 
       -  New functionality. In this case, determine if a new requirement is required to reflect the request.
	   
       -  Unexpected or incorrect behavior or properties. In this case, change the *Type* to "Defect", which will be evaluated following the `Defect Management Process <../../Operations/DefectManagement/DefectManagementProcess.html>`__.
	   
   * - 2b
     - Review enhancment request(s) - Plan and take appropriate action
     - Determine the appropriate action:
	 
       -  If the ER is a duplicate of an existing enhancement request or Epic, mark it as "Duplicate." This will close the ER.

       -  Reject or withdraw a request (i.e., the enhancement request has already been implemented in a future release or will not be implemented for some reason).
	   
	  -  Make note of the reason for rejecting the ER and mark "Reject". This will close the ER.
          -  **Note:**  The submitter may request an ER to be "Withrawn". This will close the ER.
       
       -  Accept the ER (i.e., change *Type* to "Epic").
	   
	  -  If the ER is requesting a new functionality and the PM decides that there is sufficient value to add the new functionality to the product backlog, then change the *Type* of the ER to "Epic". Enter the required information in the Epic record. An Epic will now be available in the Requirements Management tool (e.g., Jira Agile). The Epic will be evaluated per the `Requirements Development Process <./RequirementsDevelopmentProcedure.html>`__.
	  -  **Note:**  This does not indicate that the ER will be implemented, but that the ER is now entered in the backlog for evaluation in the next sprint. 

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 04/29/2020   | N/A                     | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 06/11/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Updated based on the feedback from Martin.  Converting this into a procedure instead of process.    |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+


.. |image0| image:: ../../../_static/CoreDev/Requirements/ERManagement.jpg