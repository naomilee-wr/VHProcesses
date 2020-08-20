:orphan:

|
|
|

===========================================
Projects in Jira Agile
===========================================

|

**Summary**
------------
The program development life cycle (PDLC) at Wind River governs the development of products within a program structure. Panorama is the tool used to manage programs at Wind River.

Panorama uses a hierarchy of Product Line → Program → Release → Milestone to manage the parts of the PDLC. Jira Agile uses a similar hierarchy to manage agile activities properly and link them to the PDLC process and Panorama. The Jira Agile hierarchy is Project Category → Project → Version. The Release and Milestone levels in Panorama combine to form the Version in Jira Agile.

This guideline details how to manage product lines, programs, and projects using Jira Agile.

|

**Managing Projects in Jira Agile**
------------------------------------

Jira Agile uses two types of Jira projects: **Program Project** and **Execution Project**. Each has a place in program management.

A program project is where you manage and plan features and multiple related releases. The program project will contain your feature backlog. From your feature backlog, you can plan and execute multiple releases.

Wind River requires all teams to use Jira’s **Epic** issue type to represent their features, and epics are available only in program projects. The program project is also where **Program Actions/Issues/Risks** and **Change Requests** will be stored. Program project reporting focuses on the progress of epics.

An execution project is focused on sprint-level issues, such as **Stories** and **Bugs**. Stories and bugs (defects) are available only in execution projects. The scrum team plans and manages the stories and bugs into Sprints, executing on the sprint and delivering into Versions. Execution project reporting focuses on sprint performance and version burnup.

This separation of program planning and tracking from program execution has multiple benefits:

1. Keeps story work with technology work.
2. Separates technology lines (for example, USB or networking) from programs, naturally supporting:
   a. Multiple technology teams working on the same feature.
   b. Single technology teams working on multiple programs.
3. Simplifies feature management (all related features in one project).
4. Allows bug management structure to live separately from program structure.
5. Aligns with PDLC and Panorama.

For more information on using the program project, refer to `Epics in Jira Agile <./EpicsInJiraAgile.html>`_ and `Releases in Jira Agile <./ReleasesInJiraAgile.html>`_.

For more information on using the execution project, refer to `Sprints in Jira Agile <./SprintsInJiraAgile.html>`_ and `Releases in Jira Agile <./ReleasesInJiraAgile.html>`_.

The following sections discuss the implementation of program management pieces in Jira Agile.

|

**Product Line**
---------------------------

Product lines are represented in Jira Agile as **Project Categories**.


**Creating a Project Category**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Creating a product Line in Panorama will create the corresponding project category in Jira.

Note: The Panorama project category creation functionality is not yet in place. File a `support request in Jira <https://jira.wrs.com/secure/CreateIssue.jspa?pid=11306&issuetype=2>`_ requesting a new project category and providing the name of the product line, exactly as it appears in Panorama. Note in the request if any existing Jira projects should be added to the new project category.

**Maintaining a Project Category**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once a project category has been created, it does not need to be updated. Any change to the product line’s name in Panorama will be reflected in the project category.

|

**Execution Projects**
---------------------------

An execution project is where daily work is done in Jira. The scrum backlog is managed, stories and bugs are ranked, and sprints are planned and executed.

Most existing Jira projects are execution projects.


**Creating New Execution Projects**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To create a new Execution Project, follow the existing instruction below:

- File a `support request in Jira <https://jira.wrs.com/secure/CreateIssue.jspa?pid=11306&issuetype=2>`_ requesting a new execution project category 

- Use the component ALM: Jira.

- Provide these details:

  - What is the Project name?
  - What is the Project category (left side of http://jira.wrs.com/secure/BrowseProjects.jspa)?
  - Who is the project lead?
  - Will the project publish its bugs to Knowledge Library?
  - Is the project eligible to be accessed by non-WR personnel (e.g., customer), aka 'External Visibility Allowed'?
  - Will the project have Program Actions, Risks, and Issues?

Once the new project exists, it can be associated with its program project in Panorama.

**Converting Existing Execution Projects**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The new abilities needed for Agile will be enabled when the project is connected to a program project.

|

**Program Projects**
---------------------------
A program project is where features and releases are managed. The program project contains the feature backlog. From that feature backlog, you can plan and execute multiple releases.  The program project is also where program actions/issues/risks and change requests are stored.

The program project and execution projects in a program will be maintained together. The versions used in these projects must be aligned. Refer to `Releases in Jira Agile <./ReleasesInJiraAgile.html>`_ for more information.

**Creating Program Projects**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

All execution projects for a program must exist before you create a program project.

When you create a program in Panorama, the corresponding program project will be created in Jira, and it will be associated with its execution projects.

|

**Maintaining Projects**
-------------------------

**Projects**
~~~~~~~~~~~~~

If you need to add a new execution project to an existing program project, follow the steps in the Creating new Execution Projects section above.

If you need to disconnect an execution project from a program project, file a `support request in Jira <https://jira.wrs.com/secure/CreateIssue.jspa?pid=11306&issuetype=2>`_. The following information must be provided in the request:

- Name of your program, exactly as it appears in Panorama
- Execution project to disconnect

If the program’s name changes in Panorama, the name of the program project in Jira must be updated as well. This will be handled by Panorama.

Note: This functionality is not yet in place. If you need a program project name change, file a `support request in Jira <https://jira.wrs.com/secure/CreateIssue.jspa?pid=11306&issuetype=2>`_ .  **----Check with Doina/Rodger**


**Project Artifacts**
~~~~~~~~~~~~~~~~~~~~~~
Once the Projects have been created, Versions and Components should be created by the Jira Project Lead.

**Versions**
``````````````
Refer to `Releases in Jira Agile <./ReleasesInJiraAgile.html>`_ for more information.

|

**Change Log**
--------------

+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 07/31/2020     | N/A            | 0.1            | Doina Lepadat  | Initial Draft                         |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+

 