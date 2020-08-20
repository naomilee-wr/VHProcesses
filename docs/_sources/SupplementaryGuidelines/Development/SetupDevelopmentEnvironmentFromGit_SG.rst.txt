:orphan:

|
|
|

===========================================
Set up Development Environment from Git
===========================================
**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

**Purpose:** 

(Source:https://jive.windriver.com/docs/DOC-72948)

- There are two kinds of Development Environments of VxWorks 7, Spin installation (same as what customer see) or just use Git to get the newest code from remote branch in the Git environment.

- After installing Git on your desktop or servers, clone the VxWorks 7 repository using http clone.

  **git clone -b vx7-integration http://vxgit.wrs.com/scm/vx7/vxworks.git**            //If no -b vx7-integration, it will clone default on vx7-release branch

- Or alternatively, use SSH clone so that you do not need to input passwords every time when you push remotely:
	
  **git clone -b vx7-integration ssh://git@stash.wrs.com:7999/vx7/vxworks.git**      //If no -b vx7-integration, it will clone default on vx7-release branch	

  - Before you do SSH clone, add SSH keys on Bitbucket:

    - `SSH keys on Bitbucket <http://vxgit.wrs.com/plugins/servlet/ssh/account/keys>`_
    - `Using SSH keys to secure Git operations - Atlassian Documentation <https://confluence.atlassian.com/bitbucketserver048/using-bitbucket-server/controlling-access-to-code/using-ssh-keys-to-secure-git-operations?utm_campaign=in-app-help&utm_medium=in-app-help&utm_source=stash>`_
    - `Creating SSH keys - Atlassian Documentation <https://confluence.atlassian.com/bitbucketserver048/using-bitbucket-server/controlling-access-to-code/using-ssh-keys-to-secure-git-operations/creating-ssh-keys>`_

|

|image0| (*NL 8/12:  need to look for these image files*)

|

- The transfer speed is not fast, one tip is to save the cloned git package to a zip file and then unzip it to the directory you want to add new git environment.

- The cloned git package only contains some source code, there's needs to download host tools, use below commands:

  - **cd vxworks**

  - **git pull**

  - **./setup-tools**

  - **./setup/postinstall.sh**

- Now the git development environment had been setup, you can use the development shell or WorkBench for your development.

  - **./wrenv.exe -p helix** (or **./wrenv.sh -p helix** ), or

  - **cd workbench-4**

  - **./startWorkbench.bat** ( or **./startWorkbench.sh**) 

- **Synchronization**

  - Since the vx7-integration branch is shared among all the Engineers, it's content is changing everyday. So **synchronize from remote branch** before integrating the modifications to it.

    - **cd vxworks**

    - **git checkout vx7-integration**   //Whatever branch you want to sync

    - **git pull**

    - **git status**

|image1| (*NL 8/12:  need to look for these image files*)

There's modified files for sub modules, so need to update them for latest references

**git submodule update --recursive --init**

|image2|  (*NL 8/12:  need to look for these image files*)

**./setup-tools -clean**      //When host tool changed, it's necessary to update it again, this will be notified by SIT.   

**./setup-tools**

**./setup/postinstall.sh**

|

`Access to wget.exe file <../../ProcessDocuments/CoreDev/CodingIntBuild/wget.exe>`_


|

**References**
---------------

- `Git Bash Installation on Windows <https://jive.windriver.com/docs/DOC-72859>`_
- `Git Commands and Practices <https://jive.windriver.com/docs/DOC-72860>`_
- `Helix Product Setup Guide <./HelixProductSetupGuide_SG.html>`_

|

**Change Log**
--------------

+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**  | **Version**   | **Change By**           | **Description**                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 08/03/2020   | N/A                    | 0.1           | Shree Vidya Jayaraman   | Transferred content from Jive page: DOC-72948                                       |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+


.. |image0| image:: /_static/SupplementaryGuidelines/Development/SetupDevelopmentEnvironmentFromGit_Image0.jpg
.. |image1| image:: /_static/SupplementaryGuidelines/Development/SetupDevelopmentEnvironmentFromGit_Image1.jpg
.. |image2| image:: /_static/SupplementaryGuidelines/Development/SetupDevelopmentEnvironmentFromGit_Image2.jpg