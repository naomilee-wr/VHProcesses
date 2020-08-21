:orphan:

|
|
|

=========================
Release Build Process
=========================

|

This process describes how to create: 

- the spin/build (post Feature Complete code) on the Release branch for `Release Verification Process <../Verification/ReleaseVerification_TestingProcess.html>`__.
- the final spin/build (release candidate) for `Release Process <../../Operations/ProgramManagement/ReleaseProcess.html>`__.
 
The Build & Configuration (B&C) Lead is responsible for the build in the release branch and the Release Lead from the release team is responsible for the release delivery.

|

+--------------------------------------+---------------------------------------+
| **Entry Criteria**                   | - Development Feature Complete (FC)   |
|                                      |   milestone achieved                  | 
|                                      | - Release branch ready to be created  |
|                                      |   from integration branch             |
+--------------------------------------+---------------------------------------+
| **Inputs**                           | - Development & documentation content |
|                                      |   in the integration branch of the CM |
|                                      |   system (e.g., Git)                  |
+--------------------------------------+---------------------------------------+
| **Exit Criteria**                    | - Code Freeze achieved                |
|                                      | - Approved Release build              |
+--------------------------------------+---------------------------------------+
| **Outputs**                          | - Release candidate build ready for   |
|                                      |   release                             |  
|                                      | - Labeled baseline on development     |
|                                      |   in the CM system (e.g., Git repo)   |
|                                      | - Final Release content on web based  |
|                                      |   repositories (e.g., WindShare)      |
+--------------------------------------+---------------------------------------+

|

**Activities**
--------------

|image0| 

|

.. list-table::
   :widths: 10 30 120
   :header-rows: 1   
   
   * - Step #
     - Activity Name
     - Description
    
   * - 1
     - Create release branch based on the integration branch in the repo.
     - After the Feature Completion date, the B&C Lead spins off a side branch known as the Release branch for each product release (e.g., vx7-sr0660-features branch). Permissions are set for the release branch, including setting up pull request settings and merge strategy, default reviewers for pull requests, etc. 

   * - 2
     - Add content to the release branch
     - The Scrum Team - Developer submits code to the release branch according to the `Check in Procedure <./CheckinProcedure.html>`__ (post FC complete). The B&C Lead performs the maintenance of the release branch according to the `Build and Config Release Branch Operations <https://jive.windriver.com/docs/DOC-83617>`__.	 

	   Note: This is the stabilization period where mainly defect fixes are committed onto the release branch and no new features are added.

   * - 3
     - Run the spin/build using the launchers (e.g., Jenkins)
     - The B&C Lead runs build scripts which:

       - generate spin/build for the release testing:  

         - Internal spins including Technical Documentation 

       Issues are filed as necessary for spin failures.
 	    
   * - 4
     - Run release tests on the release branch
     - The Testing team performs the Release verification (testing) - Automated and manual tests.  See `Release Verification Process <../Verification/ReleaseVerification_TestingProcess.html>`__.

       Issues are filed as necessary for any test failures. See `Defect Management Process <../../Operations/DefectManagement/DefectManagementProcess.html>`__.    
	
       **Note:** Steps 2-4 happens on a daily/nightly basis from the point Feature Complete until Code Freeze.	
	   
   * - 5 
     - Approve release candidate build
     - The release candidate build is approved by the Key Stakeholders e.g., EPM, PM, Test and Dev Team.   The B&C Lead creates the release candidate build from the release branch based on the code freeze/`release criteria <../../../ProcessDocuments/Operations/ProgramManagement/ReleaseCriteria.xlsx>`__.    The EPM initiates `Release Process <../../Operations/ProgramManagement/ReleaseProcess.html>`__.  

|

**Related Process Assets/Tools**
----------------------------------

- `Check in Procedure <./CheckinProcedure.html>`__
- `Release Verification Process <../Verification/ReleaseVerification_TestingProcess.html>`__
- `Defect Management Process <../../Operations/DefectManagement/DefectManagementProcess.html>`__
- `Release Process <../../Operations/ProgramManagement/ReleaseProcess.html>`__
- Configuration Management system (e.g., Git)
- CI Launcher/Build tool(e.g., Jenkins)
   
|

**References**
--------------- 

- Refer to `Supplementary Guidelines <../../SupplementaryGuidelinesIndex.html>`_.
   
|

**Change Log**
--------------

+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**  | **Version**   | **Change By**           | **Description**                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 05/04/2020   | N/A                    | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                       |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 06/29/2020   | N/A                    | 0.2           | Shree Vidya Jayaraman   | Updates based on Kitty's feedback                                                   |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 06/30/2020   | N/A                    | 0.3           | Shree Vidya Jayaraman   | Updates based on Mike and Alan's feedback                                           |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 07/01/2020   | N/A                    | 0.4           | Shree Vidya Jayaraman   | Updates based on Kitty's feedback                                                   |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 07/13/2020   | N/A                    | 0.5           | Shree Vidya Jayaraman   | Updates based on Kitty's feedback                                                   |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 07/22/2020   | N/A                    | 0.6           | Shree Vidya Jayaraman   | Updates based on Kitty's feedback                                                   |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+

.. |image0| image:: ../../../_static/CoreDev/CodingIntBuild/ReleaseBuild.jpg

