:orphan:
|
|
|

================================
Requirements Gathering Process 
================================

|

The process describes a sequence of activities performed to gather customer requirements.

The Product Manager is responsible for this process.

|

+----------------------------+---------------------------------------------------------------------------+
|**Entry Criteria/Inputs**   | - Customer/Product Requirements from the market segments                  |
+----------------------------+---------------------------------------------------------------------------+
|**Exit Criteria/Outputs**   | - Customer/Product Requirements from the market segments are              |
|                            |   entered in to the Requirements Backlog (e.g., Salesforce)               |
|                            | - Product Backlog (Features backlog) is created by the Product team       |
|                            |   in the Engineering Requirement System (e.g., Jira Agile)                |
+----------------------------+---------------------------------------------------------------------------+

|

**Stakeholders**
-----------------	

+------------------------+-------------------------------------------------------------------------------+
| **Role**               | **Responsibilities**                                                          |
+------------------------+-------------------------------------------------------------------------------+
| Internal Customers     | Includes Market Segment team  Field Engineers, Customer Service               |
|                        | Organization (CSO), and Product Management team                               |
|                        |                                                                               |
|                        | Market Segment team is responsible for the Requirements Backlog               |
|                        | (e.g., Salesforce)                                                            |
|                        |                                                                               |
|                        | Product Management team is responsible for the Product Feature Back log       |
|                        | (e.g., Jira Agile)                                                            |
+------------------------+-------------------------------------------------------------------------------+
| Product Manager        | Responsible for:                                                              |
|                        |                                                                               |
|                        | - entering and managing the Epics/Features in the Product Feature Backlog     |
|                        | - reviewing and prioritizing the list of features in the backlog              |
|                        | - promoting the top priority features for technical analysis/investigation    |
|                        | - entering the desired release targeted for the feature                       |
+------------------------+-------------------------------------------------------------------------------+

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
     - Gather customer/product requirements  
     - The marketing team documents the customer requirements in to the requirements backlog (e.g., Salesforce) and the Product Management Team enters one or more features/epics for each product requirement in the Requirement Management System (e.g., Jira Agile) according to the `Feature/Epic Template Guideline - Jira Agile <../../../ProcessDocuments/CoreDev/Requirements/FeatureTemplateGuideline_JiraAgile.docx>`__.  This is called the Feature (epic) backlog.  

   * - 2
     - Review feature backlog
     - The Product Manager/Owner reviews the feature backlog and other Enhancement Requests (ERs).  ERs entered in the Defect Management System (e.g., Jira) are evaluated by the Key Stakeholders (e.g., Product Manager, Engineering Manager, Technical Feature Owner) as possible requirements.  ERs are entered according to the `Enhancement Requests Management process <./EnhancementRequestManagementProcedure.html>`__

       The Product Manager/Owner prioritizes each Epic against all other Epics in the feature backlog and enters the desired release targeted for the Epic.  
       The Product Owner promotes the top priority list of epics for technical analysis/investigation.
	 	 
   * - 3
     - Evaluate and convert customer requirements to software requirements (i.e., development team user stories and tasks)
     - The Product Architect in collaboration with the Scrum Team reviews and refines the customer requirements and identifies the security related requirements according to the `Requirements Development procedure <./RequirementsDevelopmentProcedure.html>`__.   The evaluation is performed collaboratively with Product Manager to ensure alignment.  

|

**Related Process Assets/Tools**
--------------------------------

- `Requirements Process Summary Flow Diagram <../../../_static/CoreDev/Requirements/Requirements.jpg>`__
- `Enhancement Requests Management Procedure <./EnhancementRequestManagementProcedure.html>`__
- `Requirements Development Procedure <RequirementsDevelopmentProcedure.html>`__
- Requirements Backlog (e.g., Salesforce)
- Requirements Management system (e.g., Jira Agile)
- Defect Management system (e.g., Jira)
   
|

**References**
-----------------

- `Requirements Summary Flow Diagram <../../../_static/CoreDev/Requirements/Requirements.jpg>`__
- `Product Requirements Workflow Diagram <https://jive.windriver.com/docs/DOC-76575>`__
- `MST to Product Team Product Requirements Processes <https://jive.windriver.com/docs/DOC-71790>`__
- `Requirements Prioritization Process.pptx <https://jive.windriver.com/docs/DOC-71813>`__
- `Wind River Enhancement Request Process <https://jive.windriver.com/docs/DOC-37616>`_ 
- `Enhancement Requests using Jira Workflows (version 6.0) <https://jive.windriver.com/docs/DOC-37617>`_
- `Backlog management in Jira Agile <https://jive.windriver.com/docs/DOC-76366>`__
- `Epics in Jira Agile <https://jive.windriver.com/docs/DOC-76323>`__
- `Jira Agile Documentation Index <https://jive.windriver.com/docs/DOC-76381>`__

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/26/2020   | N/A                     | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 07/24/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Update based on Martin, Kitty and Guillaume's feedback                                              |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+


.. |image0| image:: ../../../_static/CoreDev/Requirements/RequirementsGatheringProcess.jpg