:orphan:

|
|
|

===========================================
Setting up Jira Agile for Teams
===========================================

|

**Summary**
------------

Jira Agile has many aspects that are designed to facilitate team use, including shared filters, boards, and dashboards. These allow a team to see the same set of information and measure its progress on a real-time basis.

Managing the shared assets of the team usually falls to the scrum master and/or the EPM.

This guideline details how to create useful filters, boards, and dashboards and share them.

|

**Team Filters**
--------------------

**Useful Team Filters**
~~~~~~~~~~~~~~~~~~~~~~~~~

There are several filters that will help a team understand its workload and its progress.

- Backlog
- Outstanding work for Sprint
- Issues in a Release
- Issues in a Sprint
- Work remaining in Sprint

|

**Sharing a Filter**
~~~~~~~~~~~~~~~~~~~~~~~~

In order for team members to use the same filter, it must be created and then shared.

#. Create a filter, referring to the `Atlassian documentation for creating/maintaining filters <https://confluence.atlassian.com/jirasoftwareserver076/saving-your-search-as-a-filter-941595927.html>`__ as needed, and save it.
#. Run the filter.
#. Click the **Details** link near the filter name.
#. Click **Edit Permissions**.
#. In the **Add Shares** field, choose **Any logged-in user**.
#. Click **+Add**.
#. If you want another user(s) to be able to change the filter and save it, add their names to the **Share Ownership**.
#. Click **Save**.

Team members can then run the filter, `select it as a Favorite <https://confluence.atlassian.com/jirasoftwareserver076/saving-your-search-as-a-filter-941595927.html#Savingyoursearchasafilter-favorite_filtersAddingafilterasafavorite>`__, and subscribe to it.

|

**Team Boards**
--------------------

To begin using Jira Agile, the scrum master will need to create a scrum backlog board. The content of a board is determined either by associating it with a filter or by selecting one or more projects.

Note that a board is not a Dashboard. Boards appear under the Boards menu in Jira’s navigation bar.

|image0|


**Creating Scrum Backlog Board**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. Run any filter in the project.
#. On the left menu, click … or **Create Board**.
#. Click **Create a Scrum board**.
#. Choose **Board from an existing project**.
#. Provide a name for the board and choose the project(s) for the board, including the program project. The current project will already be chosen.
#. Click **Create Board**.

Creating the scrum backlog board will also activate the **Backlog** and **Active Sprints** links in the left menu.

All boards created in this way are visible to anyone looking at the project. If you want to restrict that access, update the board configuration and restrict the filter shares.

|

**Team Dashboards**
--------------------

A team dashboard can collect a set of filters that the team uses into one place, and add to those filters gadgets that can help the team examine its progress and workload.

Instructions for `creating a dashboard are available from Atlassian <https://confluence.atlassian.com%2Fjirasoftwarecloud%2Fconfiguring-dashboards-764478209.html>`__(*NL 8/12: this is not a valid link.  not sure where it should point to*), as are instructions for `adding gadgets to a dashboard <https:// confluence.atlassian.com%2Fjirasoftwarecloud%2Fadding-and-customizing-gadgets-764478204.html>`__(*NL 8/12: this is not a valid link.  not sure where it should point to*).


**Helpful Gadgets for Teams**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Sprint Health
- Sprint Burndown
- Assignee Pie Chart – show how many issues each person has assigned
- Workload Pie Chart – show how many hours each person has assigned
- Days Remaining in Sprint

For each gadget that requires a filter, the filter must be shared for the team members to be able to use the dashboard.

The dashboard can be the center of the team’s standup or checkin.

|

**Change Log**
--------------

+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 07/30/2020     | N/A            | 0.1            | Doina Lepadat  | Initial Draft                         |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+


.. |image0| image:: ../../../_static/Operations/ProgramManagement/SettingUpJiraAgileForTeams_Image0.jpg 
