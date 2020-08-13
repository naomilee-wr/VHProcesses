:orphan:
|
|
|

======================
Using China Git Mirror
======================

The instructions below are meant for non-Linux teams in China who need to clone repositories from Bitbucket but are experiencing speed issues.

 
The VxWorks (VX7), Host Tools (HOSTTOOLS), and Workbench (WB4) repositories have been mirrored from Bitbucket to a Git server in Beijing to provide easier cloning. These are read-only clones, and are updated every 4 hours from Alameda.

To clone a repository from the mirror:

#. Visit **`Bitbucket <http://bitbucket.wrs.com/>`_**  and get the HTTP and SSH clone paths to the repository. If you don't see the SSH clone path, you need to set up SSH in Bitbucket: `Set up an SSH key - Atlassian Documentation <https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/>`_ 
#. Get the local address by changing the HTTP clone path: change **http://bitbucket.wrs.com/scm** to **git://pek-gitmirror-prod.wrs.com**, e.g., **http://bitbucket.wrs.com/scm/demo/demonstration.git** becomes **git://pek-gitmirror-prod.wrs.com/demo/demonstration.git**.
#. Use git clone with the local address to get the repository, e.g. **git clone git://pek-gitmirror-prod.wrs.com/demo/demonstration.git**.
#. cd into the repository.
#. Point the repository back to Bitbucket by running this command:

   - **git remote set-url origin SSH PATH**, e.g. git remote set-url origin ssh://git@bitbucket.wrs.com:7999/demo/demonstration.git
   
**Note: Changes cannot be pushed until this step is completed**.
   
#. Run **git pull** to update the repository.
 

If any issues, `file a Support Request <https://jira.wrs.com/secure/CreateIssue.jspa?pid=11306&issuetype=2>`_. Include the error message(s), the name of the repo(s), and make sure you say that the issue is with the Git mirror.


|

**Change Log**
--------------

+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**  | **Version**   | **Change By**           | **Description**                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 08/03/2020   | N/A                    | 0.1           | Shree Vidya Jayaraman   | Transferred content from the Jive page: DOC-82366                                   |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
