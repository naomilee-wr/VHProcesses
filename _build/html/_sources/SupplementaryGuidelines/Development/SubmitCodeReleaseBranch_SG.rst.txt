:orphan:

|
|
|

========================================================
Submitting Code into a Release Branch (via Pull Request)
========================================================

|
|

On Feature Complete date, a new "vx7-SRxxxx-features" branch is created off of the "vx7-integration" branch.

The purpose of this new branch is to prepare the software for release and limit new code submissions for the purpose of enhancing product stability.  A situation may arise when a developer needs to submit code into the release branch to address some critical or last minute issue.  This code is submitted via a Pull Request.

*Note*: Any code submitted into a -features branch should also be submitted into the "vx7-integration" branch to ensure future versions of the software contain the modification. To cut down on merge conflicts this will be handled by the build team. 

See Submitting Code into the Integration Branch  for the procedure on how to submit into "vx7-integration", this only comes into play when both the vx7-integration branch and the feature branch are open.

|

**Creating the Pull Request**
----------------------------------

- When code is ready to be merged go to: http://bitbucket.wrs.com/.  Log into the website using your Windows credentials.

- Select the VxWorks project: http://bitbucket.wrs.com/projects/VX7/repos/vxworks/browse 

- Select the VxWorks repository from the list

- Create the Pull Request by clicking on the "Pull Request" button in the leftmost column and then the "Create Pull Request" button in the top-right corner

- In the Create Pull Request window you will have to select both the source and destination branch.  The source is the branch that contains your change while the destination will be the release branch. 

  Note that release branches have the following naming convention vx7-<releaseNumber>-features, where <releaseNumber> is an internal release version.

  *TIP*: While creating a Pull Request, tabs at the bottom of the window will provide you with a diff of the code.  You should review the diff to ensure the submission contains the desired changes.

- Click on "Continue".  This will bring you to the "Description" window where you will be required to enter links to your development artifacts.

|

**Filling in the Pull Request Template**
-----------------------------------------

- In the "Description" window you must provide all the information described in the `VxWorks Pull Request Submission Template <../../ProcessDocuments/CoreDev/CodingIntBuild/PullRequestChecklistTemplate_v5.xlsx>`_
  
  *Note*:  The Jive document also provides instructions on how generate the appropriate development artifacts
  
  In situations where all the artifacts are not required, please comment on the reason why

|

**Verifying the Pull Request**
-------------------------------

- In order for a Pull Request to be merged, it must pass the Submission Pipeline verification. 
- To start the verification process, go to: http://vxjenkins2.wrs.com:8080/job/CI_Pipe_No_Merge/  and login using your Linux credentials
- Select "Build with Parameters" from the left-side menu.  (If the option is not visible, you may have forgotten to log into Jenkins.)
- Populate the VX7_BRANCH with your branch name and  "TARGET_BRANCH" with the destination branch
- Click on the "Build" button at the bottom of the form.
- Monitor the progress or start this process long before creating the pull request:
   -  Go to: http://vxjenkins.wrs.com:8080/  and login using your Linux credentials
   -  Select the "vx7 project" tab and click on the "VX7 Release Integration" entry 
   -  Select the " Project VX7 Release Integration" from the pipeline list:  http://vxjenkins2.wrs.com:8080/job/CI_Pipe_No_Merge/ 
   -  Select "Build with Parameters" from the left-side menu.  (If the option is not visible, you may have forgotten to log into Jenkins.)
   -  The right-side will be populated with several different options for building and testing your Pull Request.  You must provide your originating branch name for the VX7_BRANCH parameter. In most cases, the default values for all other parameters will be sufficient.
   -  Click on the "Build" button at the bottom of the form.
   -  Track the progress of your build in the left column's "History" window.  Upon completion of either method, your Pull Request should have a green "check mark" in the upper right corner beside the words "2 builds"
   -  If any failures have occurred, you can refer to the Jenkins "VX7 Helix Spin" pipeline to find the final reports:

|
   
**Merging the Pull Request**
-------------------------------
- Once your Pull Request has passed the pipeline build (mentioned in the above steps), gatekeepers will approve the pull request. Once approved the branch can be merged

*Tip*: For large code submissions, you are encouraged to solicit additional and final feedback from stakeholders before merging.  Once a merge has been completed, it CANNOT be undone.

|

**Change Log**
--------------

+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**  | **Version**   | **Change By**           | **Description**                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 05/01/2020   | N/A                    | 0.1           | Naomi Lee               | Transferred content from Submit Code Release Branch Jive page                       |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 06/26/2020   | N/A                    | 0.2           | Shree Vidya Jayaraman   | Incorporated Kitty's feedback                                                       |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 08/20/2020   | N/A                    | 0.3           | Shree Vidya Jayaraman   | Incorporated Shawn's feedback                                                       |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
