:orphan:
|
|
|

===========================================
Defects in Jira Agile
===========================================

|

**Summary**
------------

In Jira Agile, Defects are filed as Bugs. Bugs/Defects are part of a team’s backlog, and can be scheduled in Sprints. Bugs/Defects have points, just like Stories, allowing the velocity of the team to be stable regardless of whether they are doing more or less bug-fixing.

Jira Agile does not change any of the current processes or policies for defects; it just allows better scheduling of them.

This guideline details how to manage bugs/defects using Jira Agile.

|

**Workflow**
--------------------------- 


**State Machine**
~~~~~~~~~~~~~~~~~~~~~~

The bug/defect’s state machine does not change as a result of Jira Agile.

|image0|

**Managing Defects**
~~~~~~~~~~~~~~~~~~~~~~
During triage or grooming, the team assigns story points to a bug. The scrum backlog board can be used to rank bugs with stories in the same backlog.  From the board, drag bugs into active or future sprints. Refer to `Sprints in Jira Agile <./SprintsInJiraAgile.html>`_ for details about the sprint planning process.


**Defects found when testing a Story**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A bug/defect should be linked to a Story if the defect is related to the work being done to implement that Story.  Use the bug/defect’s **More->Link** option to make a **relates to** link between the bug/defect and the story.

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


.. |image0| image:: ../../../_static/Operations/ProgramManagement/DefectsInJiraAgile_Image0.jpg 
 