:orphan:

|
|
|

======================
Check-in Procedure
======================

Developer submission of modified/created code to the CM system (e.g., Git) via Build Configuration system ( e.g., Jenkins).

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | Code/Code change passes code review  |
|                                      | process.                             |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | Code to be checked in                |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | -  CI pipeline build completed and   |
|                                      |    code checked into the Integration |
|                                      |    branch                            |
|                                      | -  Code is checked into the Release  |
|                                      |    branch                            |
|                                      | -  Stories and defect status updated |
|                                      |    for completing tasks              |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | -  Checked in code, if accepted      |
|                                      | -  Defects resolved                  |
|                                      | -  Stories marked "Done"             |
+--------------------------------------+--------------------------------------+

|

**Activities**
--------------

1. The Architect/Domain Lead is responsible to identify the configurations for the CI pipeline as well as the nightly regression tests.  The Build & Configuration team is responsible for ensuring the configs are part of the CI pipeline checks.

2. Using the CI pipeline (Jenkins) build tool, the Developer submits code into the integration branch according to the Work Instructions in `Submitting Code into the Integration Branch <../../../SupplementaryGuidelines/Development/SubmitCodeIntegrationBranch_SG.html>`__ 

   - Each code submission by the Developer goes through a series of configuration builds as part of the CI pipeline. The CI pipeline double checks/validates all the previously performed tests, warnings, analysis, reviews and code clean up by the Developer.
   - Once the CI pipeline check is completed, the Jenkins tool automatically checks in the code into the Integration branch and automatically update the state of the Jira Defect (if it is a Defect) to "Checked in".  
   - Once the code is committed to the Integration branch, the continuous build and nightly regression tests are initiated.  See `Continuous Build and Nightly Regression Testing Process <./ContinuousBuildTestingProcess.html>`__
   - If issues found, the Build & Configuration Engineer raises a defect in the Defect Management system, Jira according to the `Defect Management process <../../Operations/DefectManagement/DefectManagementProcess.html>`__
   - If no issues found, the Developer marks the Jira Defect as "Resolved" and the Jira Story/Task as "Done".   

3. After the Feature Complete date (code freeze), the Release Branch is created off of the Integration Branch.  

   - The Developer submits the code according to the Work Instructions in `Submitting Code into the Release Branch <../../../SupplementaryGuidelines/Development/SubmitCodeReleaseBranch_SG.html>`__.  The code is submitted via the `Pull Request Checklist Template <../../../ProcessDocuments/CoreDev/CodingIntBuild/PullRequestChecklistTemplate_v5.xlsx>`__
   
   - Once the code is committed to the regression branch, the continuous build and nightly regression tests are initiated.  See `Continuous Build and Nightly Regression Testing Process <./ContinuousBuildTestingProcess.html>`__
   
   - The release candidate is built according to the `Release Build Process <./ReleaseBuildProcess.html>`__ and ready for the Release verification testing. 
  
   - The testing team performs verification on the release spin according to the `Release Verification (Testing) Process <../Verification/ReleaseVerification_TestingProcess.html>`__
       
     - If issues found, the tester raises a defect in the Defect Management system, Jira according to the `Defect Management process <../../Operations/DefectManagement/DefectManagementProcess.html>`__
	
4. To submit fixes into the SR05xx maintenance branch, the Developer submits code into the Maintenance/Sustaining branch according to the Work Instructions in `Submitting Code into the Maintenance Branch <../../../SupplementaryGuidelines/Development/SubmitCodeMaintenanceBranch_SG.html>`__

   - The code is submitted via the `Pull Request Checklist Template <../../../ProcessDocuments/CoreDev/CodingIntBuild/PullRequestChecklistTemplate_v5.xlsx>`__
 
|

**Related Process Assets/Tools**
--------------------------------

- `VxWorks: Submitting code into the Integration Branch <../../../SupplementaryGuidelines/Development/SubmitCodeIntegrationBranch_SG.html>`__
- `VxWorks: Submitting code into a Release Branch <../../../SupplementaryGuidelines/Development/SubmitCodeReleaseBranch_SG.html>`__
- `VxWorks: Submitting code into the SRO5XX Maintenance Branch <../../../SupplementaryGuidelines/Development/SubmitCodeMaintenanceBranch_SG.html>`__
- `Release Build Process <./ReleaseBuildProcess.html>`__
- Engineering Requirements Management system (e.g., Jira Agile)
- Configuration Management system (e.g., Git)
- CI Launcher(e.g., Jenkins)

   
|

**References**
---------------

- `VxWorks Pull Request Submission Template <../../../ProcessDocuments/CoreDev/CodingIntBuild/PullRequestChecklistTemplate_v5.xlsx>`__

Note: For additional references, refer to `"Supplementary Guidelines" <../../../SupplementaryGuidelines/SupplementaryGuidelinesIndex.html#development>`_ section.


|

**Change Log**
--------------

+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**  | **Version**   | **Change By**           | **Description**                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 05/01/2020   | N/A                    | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                       |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 06/12/2020   | N/A                    | 0.2           | Shree Vidya Jayaraman   | Update based on Kitty's feedback                                                    |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 06/26/2020   | N/A                    | 0.3           | Shree Vidya Jayaraman   | Update based on Kitty's feedback                                                    |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 07/22/2020   | N/A                    | 0.4           | Shree Vidya Jayaraman   | Update based on Kitty's feedback                                                    |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 07/24/2020   | N/A                    | 0.5           | Shree Vidya Jayaraman   | Update based on Kitty's feedback (Continuous Build and Nightly Regression Testing)  |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
