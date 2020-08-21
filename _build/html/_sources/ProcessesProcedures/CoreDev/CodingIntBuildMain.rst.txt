:orphan:

|
|
|

============================================
**Coding, Integration, and Build**
============================================

|
|

`Coding Integration & Build Process Summary Flow Diagram <../../_static/CoreDev/CodingIntBuild/Coding.jpg>`__
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

|

Policies
========== 

*Note:  Team to identify policy(ies) as applicable*

|

Processes & Procedures
======================

- `Code Development Process <./CodingIntBuild/CodeDevelopmentProcess.html>`__

  - `Development (Unit) Testing Procedure <./CodingIntBuild/DevUnitTestingProcedure.html>`__
  - `Peer Review Procedure Using Code Collaborator <./CodingIntBuild/PeerReviewProcedure_CodeCollaborator.html>`_
  - `Check-in Procedure <./CodingIntBuild/CheckinProcedure.html>`__

- `Continuous Build and Nightly Regression Testing Process <./CodingIntBuild/ContinuousBuildTestingProcess.html>`__
- `Release Build Process <./CodingIntBuild/ReleaseBuildProcess.html>`__

|

Standards & Guidelines
======================

- `VxWorks Coding Standard <http://bitbucket.wrs.com/projects/VX7/repos/codingstandard/browse>`__
- `Coding Standards <../../ProcessDocuments/CoreDev/CodingIntBuild/WindRiverVxWorksCodingStandard.pdf>`__     **Draft version updated but not reviewed/approved**

  - `Coding Style Guide <../../ProcessDocuments/CoreDev/CodingIntBuild/WindRiverVxWorksCodingStyleGuide.pdf>`__
  - `Coding Rules Guide <../../ProcessDocuments/CoreDev/CodingIntBuild/WindRiverVxWorksCodingRulesGuide.pdf>`__

- `Submitting code to Integration Branch <../../SupplementaryGuidelines/Development/SubmitCodeIntegrationBranch_SG.html>`__
- `Submitting code to Release Branch <../../SupplementaryGuidelines/Development/SubmitCodeReleaseBranch_SG.html>`__
- `Submitting code to Maintenance Branch <../../SupplementaryGuidelines/Development/SubmitCodeMaintenanceBranch_SG.html>`__
- `Dealing with VSBL, Spec Files and RPMs <../../SupplementaryGuidelines/Development/VsblSpecFilesRpm_SG.html>`__
- `Doc as Code Guideline <../Operations/InformationDevelopment/DocAsCodeGuideline.html>`_   
- `Accessing and Installing a VxWorks Spin <../../SupplementaryGuidelines/Development/Accessing_InstallingVxWSpin_SG.html>`_
- `Set up Development Environment from Git <../../SupplementaryGuidelines/Development/SetupDevelopmentEnvironmentFromGit_SG.html>`_
- `Accessing and Modifying VxWorks 7 code using Git <../../SupplementaryGuidelines/Development/AccessingAndModifyingVxWorksCodeUsingGit_SG.html>`_

  - `Git Cheat Sheet #1 <../../ProcessDocuments/CoreDev/CodingIntBuild/GitCheatSheet_1.pdf>`__
  - `Git Cheat Sheet #2 <../../ProcessDocuments/CoreDev/CodingIntBuild/GitCheatSheet_2.pdf>`__
  
- `Generating a new RPM <../../SupplementaryGuidelines/Development/GeneratingNewRPM_SG.html>`__
- `Guidelines for deprecating or EOL'ing layers and components, or releasing "unsupported" content, or moving functionality between layers <../../SupplementaryGuidelines/Development/GuidelinesforLayersComponents_SG.html>`__
- `Restricted Files in VxWorks 7 <../../SupplementaryGuidelines/Development/RestrictedFilesinVxWorks_SG.html>`_
- `Maintaining Coverity "Clean" Code <../../SupplementaryGuidelines/Development/MaintainingCoverityCleanCode_SG.html>`_
- `Build Warning Guidelines of VxWorks 7 <../../SupplementaryGuidelines/Development/GuidelinesBuildWarning_SG.html>`__
- Code Reviews and Doc Reviews  

  - `Code Review Improvements <../../ProcessDocuments/CoreDev/CodingIntBuild/CodeReviewImprovements.pptx>`__
  - `Writers Review of Engineering Generated Documents <../../SupplementaryGuidelines/Development/WritersReviewofEngGeneratedDocs_SG.html>`__
  - `Code Review Checklist Guidelines <../../SupplementaryGuidelines/Development/CodeReviewChecklistGuidelines_SG.html>`__
  
- `Responding to Nightly Validation <../../SupplementaryGuidelines/Development/RespondingToNightlyValidation_SG.html>`_
- `How to Handle Build Issues <../../ProcessDocuments/CoreDev/CodingIntBuild/HowToHandleBuildIssues_Final.docx>`__
- `Documenting a Feature/Epic <../../SupplementaryGuidelines/Development/DocumentingAFeature_SG.html>`__
- `Open Source BSP process <../../SupplementaryGuidelines/Development/OpenSourceBSPProcess_SG.html>`__
- `Managing Third Party Libraries Located in WR GitHub <../../SupplementaryGuidelines/Development/ManagingThirdPartyLibrariesLocatedInWindRiverGitHub_SG.html>`__
- `Declaring New and Modified 3rd Party IP <../../SupplementaryGuidelines/Development/DeclaringNewAndModifiedThirdPartyIP_SG.html>`_
- `CVE tracking & Third Party Library upgrade process <../../SupplementaryGuidelines/Development/CveTrackingThirdPartyLibraryUpgrade_SG.html>`__
- `Setting up a Development Environment <../../SupplementaryGuidelines/Development/SettingUpDevelopmentEnvironment_SG.html>`__
 



|

Tools & Templates
=================

*Note: Team to identify additional Tools & Templates as applicable*

+-------------------------------------+----------------------------------------------------------+-------------------------------------------+
| Tool Name                           | Description                                              | Tool in use                               |
+-------------------------------------+----------------------------------------------------------+-------------------------------------------+
| Peer Review system                  | Track and manage peer review comments                    | Code Collaborator                         |
|                                     |                                                          | http://codereview.wrs.com                 |
+-------------------------------------+----------------------------------------------------------+-------------------------------------------+
| Configuration Management System     | Program repository                                       | Jenkins                                   |
|                                     |                                                          | http://vxjenkins.wrs.com:8080/            |
+-------------------------------------+----------------------------------------------------------+-------------------------------------------+
| Build System                        | Track and manage nightly builds                          | Jenkins                                   |
|                                     |                                                          | http://vxjenkins.wrs.com:8080/            |
+-------------------------------------+----------------------------------------------------------+-------------------------------------------+

Templates
--------------

- `VxWorks Pull Request Submission Template <../../ProcessDocuments/CoreDev/CodingIntBuild/PullRequestChecklistTemplate_v5.xlsx>`__

|

Related Process Assets 
=======================

- `Design Process <./Design/DesignProcess.html>`__
- Engineering Requirements Management system (e.g., Jira Agile)

|

References 
=============

*Note: Team to review the reference links below*

- `Requesting and Dealing with Hardware Requests <https://jive.windriver.com/docs/DOC-57260>`_
- `VxWorks 7 Git Check-in Process <https://jive.windriver.com/docs/DOC-72793>`_
- `How to Run Coverity for VxWork 7 Before Running CI Launcher <https://jive.windriver.com/docs/DOC-71808>`_
- `VxWorks Real-Time Process (RTP) System Calls and Binary Compatibility <https://jive.windriver.com/docs/DOC-77173>`_
 