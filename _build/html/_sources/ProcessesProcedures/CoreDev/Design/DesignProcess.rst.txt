:orphan:

|
|
|

==================================
Design Process (HLD Development)
==================================

|

This process describes the creation of the High Level Design (HLD) for each requirement, as applicable.

The Technical Feature Owner and/or scrum team members are responsible for executing this process.

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | Software requirements are identified |
|                                      | as Epics/Stories in the Requirements |
|                                      | Management System and available for  |
|                                      | evaluation if a high level design    |
|                                      | document is required for the release.|
+--------------------------------------+--------------------------------------+
| **Inputs**                           | -  Software requirements are         |
|                                      |    identified as Epics/Stories in the|
|                                      |    Requirements Management System    |
|                                      |    (e.g., Jira Agile)                |
|                                      | -  Design Standard (if applicable)   |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | Refined software requirements and    |
|                                      | their approved HLDs documented, if   |
|                                      | applicable.                          |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | -  Approved HLDs stored in CM        |
|                                      |    system.                           |
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
     - Examine software requirements (i.e., Features/Epics from marketing segment and product team)
     - The Key Stakeholders (e.g.,  Product Architect, Technical Feature Owner, Engineering Manager, Test Lead, Product Manager, etc.) examines software requirements and assigns Technical Feature Owner or scrum team member to review the requirement. 
    
   * - 2
     - Review each software requirement 
     - The assignee (Architect, Technical Feature Owner or Scrum team) reviews the description and clarifies requirement for a Feature/Epic, defines Development team's Stories and Tasks by following steps 3 - 10 below.
    
   * - 3
     - Determine HLD creation for software requirements 
     - The assignee checks with the Product Architect and the Technical Feature Owner to determine if a separate HLD is required for a Feature/Epic and the decision is recorded in the HLD Story.

       HLDs are usually only required for complex epics, significant changes or changes that have significant interaction with other teams.

   * - 4
     - Create new HLD
     - The assignee creates a new HLD. The design must use the HLD template and conform to the design standard (if applicable). 

       The HLD identifier is the name of the file in the CM system.

   * - 5
     - Ensure traceability between requirement and HLD 
     - As HLDs are created for each requirement as applicable, the author of the HLD (Tehcnical Feature Owner or Scrum Team member) ensures traceability between the HLDs and software requirements, and the hierarchy of the requirement is maintained. 

   * - 6
     - Review design
     - The HLD is reviewed by the Security and Product Architects and other Key Stakeholders as appropriate.  The author of the HLD fixes review defects.

   * - 7
     - Perform Green Light Review
     - The Product Architect determines when the HLD is complete and ready for final review and approval. The design is expected to not require major changes at this point.  The review is performed according to the `Green Light Review <./DesignGreenLightReviewProcess.html>`__ and the design is approved when the review is completed and tracked to closure in the Peer Review system (e.g., Code Collaborator).

   * - 8
     - Store approved HLD in the CM system
     - The approved HLD is baselined and stored in CM system.

   * - 9
     - Write implementation Stories
     - The author of the HLD investigates, refines requirements and writes implementation Stories.  The Scrum team develops the implementation stories using the `Code Development Process <../CodingIntBuild/CodeDevelopmentProcess.html>`__.
	   
|

**Related Process Assets/Tools**
--------------------------------

- `Design Summary Flow Diagram <../../../_static/CoreDev/Design/Design.jpg>`__
- `HLDs <https://jive.windriver.com/community/engineering/operation-system-common-platforms/teams/vxworks/vat/hlds>`__
- Peer Review system (e.g., Code Collaborator)
- Requirements Management system (e.g., Jira Agile)
   
|

**References** 
-----------------

- `Epics in Jira Agile <https://jive.windriver.com/docs/DOC-76323>`__
- `Jira Agile Documentation Index <https://jive.windriver.com/docs/DOC-76381>`__

|	   

**Change Log**
--------------

+---------------+------------------------+---------------+-------------------------+---------------------------------------------------------------------------------+
| **Date**      | **Change Request ID**  | **Version**   | **Change By**           | **Description**                                                                 |
+---------------+------------------------+---------------+-------------------------+---------------------------------------------------------------------------------+
| 05/01/2020    | N/A                    | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                   |
+---------------+------------------------+---------------+-------------------------+---------------------------------------------------------------------------------+
| 06/10/2020    | N/A                    | 0.2           | Shree Vidya Jayaraman   | Updated based on Kitty's feedback                                               |
+---------------+------------------------+---------------+-------------------------+---------------------------------------------------------------------------------+
| 07/16/2020    | N/A                    | 0.3           | Shree Vidya Jayaraman   | Updated based on Kitty's feedback                                               |
+---------------+------------------------+---------------+-------------------------+---------------------------------------------------------------------------------+
|               |                        |               |                         |                                                                                 |
+---------------+------------------------+---------------+-------------------------+---------------------------------------------------------------------------------+

.. |image0| image:: ../../../_static/CoreDev/Design/SoftwareDesignProcess.jpg
