:orphan:

|
|
|

=================================
Configuration Management Process
=================================

The configuration management process describes how to establish and maintain the integrity of program-related work products and baselines throughout the lifecycle and make them available to relevant stakeholders in time for their need.

A Software Configuration Management (SCM) Plan is used to document and guide project stakeholders in the CM tools and methods used within the program.

The Configuration Management(CM)/ Build & Configuration Lead is responsible to see that this process is performed.

|

+--------------------------------------+----------------------------------------------------------------------------+
| **Entry Criteria**                   | -  A new program has been initiated/authorized and has begun planning      |
+--------------------------------------+----------------------------------------------------------------------------+
| **Inputs**                           | -  Program planning data and information                                   |
+--------------------------------------+----------------------------------------------------------------------------+
| **Exit Criteria**                    | -  The product is no longer in use and has been successfully and           |
|                                      |    permanently archived                                                    |
+--------------------------------------+----------------------------------------------------------------------------+
| **Outputs**                          | -  Documented plan for Configuration Management                            |
|                                      | -  Controlled and released configuration items and baselines               |
|                                      | -  Configuration status (accurate information on the program work products |
|                                      | -  Configuration audit reports (verification of configuration records)     |
+--------------------------------------+----------------------------------------------------------------------------+

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
     - Develop and maintain plan for software configuration management
     - The CM Lead develops the program's SCM plan.  The plan is updated to reflect any major changes.  Key elements in the plan are:
	 
       -  Roles and responsibilities
       -  Required resources, tools and repositories
       -  Identification of Configuration Items (CIs) to be controlled
       -  Strategy and methods for creating and releasing baselines, configuration control and configuration status accounting and auditing   **<<need to revisit after Devstar launch>>**
	   
       The SCM plan should be approved by all key stakeholders (e.g., Engineering Management, Product Management, Engineering Program Management, Info Dev, etc)
  
   * - 2
     - Identify program release items for control (Configuration Items)
     - The CM Lead, in conjunction with the key stakeholders (e.g., Engineering Manager, EPM, Technical Lead, and Test Lead) identify the CIs that have been documented in the SCM plan. These CIs compose the baselines at given points in the lifecycle.

   * - 3
     - Establish and maintain the CM framework
     - The CM Lead establishes the framework for the CM activities and multiple levels of control, per the SCM plan. 
	 
   * - 4
     - Create and release baselines
     - The CM Lead, supported by the Development and Test Managers and teams, establish and maintain baselines at designated points in the lifecycle, per the SCM plan. 

       A baseline is a set of CIs that has been reviewed and agreed on, which thereafter serves as the basis for further development and which can be changed only by following the change control process and program change request procedure. Baselines can be internal or external and typically include functional (e.g., committed set of requirements), development (e.g., builds) and release (e.g., product deliveries) baselines.

       The CI description that compose the baselines are updated, placed under control, and communicated.  After their approval, the baselines are communicated to the team using various collaboration mechanisms (e.g., Team email, Jive/SharePoint).

   * - 5
     - Track and control changes to baselined configuration items
     - The CM Lead, Development, Test Managers and teams initiate and record a defect or Change Request to address changes to baselined requirements and development work products (e.g., design). Meeting with the Key Stakeholders is held to request, evaluate, approve, disapprove and implement changes to baselined CIs according to the `Change Management Procedure <./ChangeManagementProcedure.html>`_. The changes encompass both error correction and enhancement.

       The degree of formality necessary for the change process, as well as the change mechanism used depends on the baseline affected and the impact of the change within the configuration structure, as outlined in the `Change Management Procedure <./ChangeManagementProcedure.html>`_.

   * - 6
     - Control obsolete configuration items
     - When a CI becomes obsolete, the obsolete CIs are handled as per the SCM plan in place.

   * - 7
     - Perform configuration audits and reviews
     - The CM Lead and SQA Lead conduct functional and physical configuration audits and reviews on a regular basis to ensure the following:
	 
       -  CM practices are followed per plan.
	 
       -  The product package contains all of the components it is supposed to contain.
	 
       -  Baselines are correctly maintained, to ensure completeness, correctness and consistency.
	 
       Audits are performed per the `Audit Process <../SWQualityAssurance/InternalAuditProcess.html>`__.

   * - 8
     - Record and communicate status
     - The CM Lead reports the configuration status to affected stakeholders on a need basis. Example reports include the current status of CIs (e.g., under work, checked in, tested, released), changes to CIs since the last baseline and various build views.

   * - 9
     - Control the storage and handling of baselined configuration items
     - Backup (including disaster recovery), storage and handling of baselined CIs are performed by the Wind River Information Technology (IT) group.

   * - 10
     - Control the delivery of baselined configuration items
     - The Release Operations team is responsible for the delivery of baselined CIs.

   * - 11
     - Monitor progress
     - The Engineering Program Manager and Engineering Manager monitor CM progress and activities on a regular basis.

|

**Related Process Assets/Tools**
---------------------------------

- ??  

|

**References**
-----------------

- ??

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/01/2020   | N/A                     | 0.1           | Naomi Lee               | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 07/20/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Updated the flow diagram and added link to step 5                                                   |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 08/13/2020   | N/A                     | 0.3           | Shree Vidya Jayaraman   | Updates based on the feedback received from Martin                                                  |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+


.. |image0| image:: /_static/Operations/ConfigurationManagement/SWConfigManagementProcess.jpg    