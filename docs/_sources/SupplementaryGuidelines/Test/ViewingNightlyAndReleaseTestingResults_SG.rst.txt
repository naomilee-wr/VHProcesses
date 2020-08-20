:orphan:

|
|
|

============================================
Viewing Nightly and Release Testing Results
============================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

**Purpose:**  Although developer's are responsible for testing their own Features prior to submission, the Test Team also executes both Nightly and Release level testing on the product.  Developers may want to reference test results coming from the Test Team to assess the state of the release.

(Source: https://jive.windriver.com/docs/DOC-58993)

**Procedure:**
---------------
- To access the latest Nightly Testing results developers may reference either of the following:

  - Nightly testing reports sent by the Test Team, see `Responding to Nightly Validation <../Development/RespondingToNightlyValidation_SG.html>`__ for more information
  - Login into LTAF
   
    - Select the appropriate release in the top-right drop-down box
   
    - Select the "Reporting -> Nightly Report" menu options
   
    - *TIP:* Any Nightly Test Cases failing should have am associated JIRA defect record tagged with the labels "Vx7_<release>_Release" (where release follows enumeration convention SR0500, SR0510, etc.) and "Vx7_Nightly_Test".
	
- To access the latest Release Testing results developers must reference LTAF:

  - Login into LTAF
   
    - Select the appropriate release in the top-right drop-down box
   
    - Select the "Reporting -> Release Trend" menu options
   
    - *TIP:* Any Release Test Cases failing should have am associated JIRA defect record tagged with the labels "Vx7_<release>_Release" (where release follows enumeration convention SR0500, SR0510, etc.).

**Important References:**
--------------------------

- `LTAF Reports <http://pek-lpgtest3.wrs.com/ltaf/report.php>`__

- `JIRA <http://jira.windriver.com>`__