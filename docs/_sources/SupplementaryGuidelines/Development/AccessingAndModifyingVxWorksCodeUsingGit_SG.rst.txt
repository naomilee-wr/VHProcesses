:orphan:

|
|
|

=================================================
Accessing and Modifying VxWorks 7 Code Using Git
=================================================

|
|

**Purpose**
------------

Git is the primary tool used to access and submit VxWorks 7 code.  The following provides the steps required to setup your Git environment, access VxWorks 7 code, and perform submissions.

|

**Important Reference**
------------------------

- `Primary BitBucket Portal <http://bitbucket.wrs.com/dashboard>`_
- `Git Workflow <../../ProcessDocuments/CoreDev/CodingIntBuild/VxWorksSR0520GitWorkflow-v2.pptx>`_
- `Environment setup for VxWorks 7 in Git: Setup Development Environment from Git <./SetupDevelopmentEnvironmentFromGit_SG.html>`_ 
- `Virtualization Profile documentation on getting started <https://jive.windriver.com/docs/DOC-74113>`_
- Security Profile documentation on getting started: `How to get started with the VxWorks 7 security development <https://jive.windriver.com/groups/vxworks-7-security/blog/2017/02/17/getting-started>`_

|

**Procedure**
--------------

|

**Setting-Up Your Environment**
----------------------------------

The recommended steps for setting up your environment and cloning the VxWorks 7 repository can be viewed at `Helix Product Setup Guide <./HelixProductSetupGuide_SG.html>`_

|

**Creating Branches (for Pull Requests)**
-------------------------------------------

See the image below or for the instructions on how to create and manipulate branches using Git.

|image0|

To create a branch that will allow you to add code to vx7-integration, you must follow the steps below:

- git clone ssh://git@stash.wrs.com:7999/vx7/vxworks.git -b vx7-integration
- git clone git://pek-gitmirror-prod.wrs.com/vx7/vxworks.git -b vx7-integration (for git clone from China git mirror from `Using the China Git mirror <./UsingChinaGitMirror.html>`_)
- cd vxworks
- ./setup-tools
- ./setup-tools -site pek/ctu -set-url (for git clone from China git mirror to set remote url back to stash.wrs.com or else git push will go to the China git mirror and not stash.wrs.com, note that the set remote url requires **git version 2.25 or above**)
- git pull
- git checkout vx7-SR0XXX-features (to start with another base branch instead of vx7-integration)
- git checkout -b <source branch>
- git push --set-upstream origin <source branch>

|

**Modifying and Committing Code**
-------------------------------------------

- Typically, to modifying and commit code you simply have to follow these steps:
  - make modifications to a <file>
  - git add <file>
  - git commit
  - git push
- Good commit messages help give details on the commit and the impact. It provides traceability to the work.
  - `Git Commit Message Standard <./GitCommitMessageStandard_SG.html>`_
  - Sample commit message template:
  
|image1|

|

**How To Do Rebases To Prevent Merge Commits**
-------------------------------------------------

(IMPORTANT!) DO NOT create merge records.  The steps on getting around the creation of merge records are clearly explained in `VxWorks SR0520 Git Workflow <../../ProcessDocuments/CoreDev/CodingIntBuild/VxWorksSR0520GitWorkflow-v2.pptx>`_

|

**Change Log**
--------------

+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**  | **Version**   | **Change By**           | **Description**                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 08/03/2020   | N/A                    | 0.1           | Shree Vidya Jayaraman   | Transferred content from Jive page: DOC-57324                                       |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 08/24/2020   | N/A                    | 0.2           | Shree Vidya Jayaraman   | Updates based on Shawn's feedback                                                   |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+


.. |image0| image:: /_static/SupplementaryGuidelines/Development/AccessingAndModifyingVxWorksCodeUsingGit_Image0.jpg 

.. |image1| image:: /_static/SupplementaryGuidelines/Development/AccessingAndModifyingVxWorksCodeUsingGit_Image1.jpg 

