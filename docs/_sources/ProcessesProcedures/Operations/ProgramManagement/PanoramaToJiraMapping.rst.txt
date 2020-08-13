:orphan:
|
|
|

===========================================
Panorama-To-Jira Mapping
===========================================

|

**Summary**
------------

Panorama and Jira are used in combination to manage product lines, programs, and releases. This guideline lays out the comparable parts of each system and how data flows between them.

|

**Record Types**
-------------------

**Product Line**
~~~~~~~~~~~~~~~~~~~~~~

Panorama’s Product Line encompasses all the program releases a given product line. The level of granularity is large: VxWorks, Linux, Engineering Success.

The comparable object in Jira is the Project Category. Category is an attribute of all Jira projects, and is set when the project is created in Jira.

**Program**
~~~~~~~~~~~~~~

Panorama’s Program manages all the releases for a given stream of deliveries, and tends to focus on a set of releases of the same development effort, e.g., VxWorks 7, WRL 9.0.0.x, Infrastructure Development.

The comparable object in Jira is the Project. A Panorama program will have at least two Jira projects: a program project, used for planning and containing epics, actions/issues/risks, and PCRs, and one or more execution projects for stories, sub-tasks, and bugs. High-level content planning will happen in the program project and scrum activity will take place in the execution project(s).

**Release/Milestone**
~~~~~~~~~~~~~~~~~~~~~~~

Panorama’s Release is a single development effort that may result in one or more deliveries, e.g. VxWorks SR0610, WRL-9.0.0.19, Panorama 3.1. A Milestone is a specific delivery or completion of a process phase, e.g., EAR, GA.

The comparable object in Jira is the Version, also known as Release. The Jira version has a name, a start date, and an end date. Content (epics, stories, bugs) can be aimed at one or more versions. Showing the issues aimed at a version shows the work done for that Version. The version appears in the Fix Version/s field.

Refer to `Releases in Jira <./ReleasesInJiraAgile.html>`_ for more details.


**Reporting**
~~~~~~~~~~~~~~~~~~~~~~~

Content reporting in Panorama is done on the Content tab, and features the Burnup chart and a list of features, represented in Jira as epics.

Jira offers a version burnup chart in the Reports section of the execution project’s scrum backlog board. It is called Version Report and can be run against any version in the project.

The list of features on the Content tab can be reproduced in Jira by creating a filter that includes only the program project and only the version affiliated with the Panorama release. This will return the assigned to the version.

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

 