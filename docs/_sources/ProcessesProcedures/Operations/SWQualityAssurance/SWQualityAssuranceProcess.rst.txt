:orphan:
|
|
|

===============
SQA Process
===============

|

SQA provides visibility to management that the product conforms to the specified requirements, processes and established plans. This process describes the planning and executing Software Quality Assurance (SQA) activities on a release. 

The SQA lead is responsible for this process.

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | -  Commitment to the SQA policy.     |
|                                      | -  A set of requirements committed to|
|                                      |    a release                         |
|                                      | -  SQA resource committed            |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | A high level release schedule with   |
|                                      | milestone available                  |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | The SQA plan has been approved, and  |
|                                      | detailed audits and reviews have     |
|                                      | been planned. Audits and reviews are |
|                                      | executed. Status is reported.        |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | -  Approved SQA plan                 |
|                                      | -  Audit and review records          |
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
     - Create release level/generic SQA Plan
     - Based on the program release strategy, the SQA Lead develops the SQA plan.

       The SQA plan includes at a minimum:
	 
       -  quality goals
	 
       -  high level description of SQA activities - audits and reviews
	 
       -  responsibilities for audits
	 
       -  management of audit results
	 
       -  audit methods
  
       **Note:**  In cases where the program release level/Generic SQA plan already exists, the project may choose to use the existing document instead of creating them anew for the release.
    
   * - 2
     - Approve SQA Plan
     - The SQA plan is peer reviewed and approved by the Key Stakeholders (e.g., Engineering Managers/Director, EPM). The approved plan is placed under CM control.
    
   * - 3
     - Plan detailed audits and reviews
     - The SQA Auditor prepares a detailed plan for each individual audit and review. Note that the SQA Auditor role can be performed by the SQA Lead.

       A record is created with the following information: schedule, scope: what will be audited (e.g., work products, processes) or reviewed (e.g., phase gate artifacts), participants, SQA resources needed, and evaluation criteria (e.g., checklists) to be used. See the `Internal Audit process <./InternalAuditProcess.html>`__.

   * - 4
     - Perform audits
     - The SQA Auditor conducts designated audits and reviews per the detailed plans. See the `Internal Audit process <./InternalAuditProcess.html>`__.

   * - 5
     - Report SQA status
     - The SQA Auditor reports progress against the plan periodically to the Key Stakeholders (e.g., Engineering Managers/Director, EPM).

       The SQA Plan and detailed plans are updated to reflect any new or changed objectives or requirements. 

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                           |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------+
| 05/14/2020   | N/A                     | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                             |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------+
|              |                         |               |                         |                                                           |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------+


.. |image0| image:: /_static/Operations/SWQualityAssurance/SqaProcess.jpg