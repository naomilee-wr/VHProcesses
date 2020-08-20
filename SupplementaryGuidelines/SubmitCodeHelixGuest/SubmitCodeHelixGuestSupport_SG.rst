:orphan:

|
|
|

=============================================
Submitting Code to Helix Guest Support
=============================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

The objective of this document is to capture the steps to submit code to helix_guest_support repository.

(Source: https://jive.windriver.com/docs/DOC-83630)

|

**Create Pull Request and manually start a buildHelix Guest Support Branch strategy:**
---------------------------------------------------------------------------------------
The branching strategy for the Helix guest support is very simple, at the Feature Complete (FC) for each release, a new branch is created for the next in-flight release. 

For Example, at the FC date for SR0650 (May, 29th 2020), a new branch for SR0660 should be created to submit code targeted for that release. 

At the time of writing this Jive page (https://jive.windriver.com/docs/DOC-83630), the status of the Helix Guest Support branches are captured below:

+--------------+------------------------------------------------------------------------+
| **Branch**   |  **Status**                                                            |
+--------------+------------------------------------------------------------------------+
| master       |  locked                                                                |
+--------------+------------------------------------------------------------------------+
| SR0620       |  locked                                                                |
+--------------+------------------------------------------------------------------------+
| SR0630       |  locked                                                                |
+--------------+------------------------------------------------------------------------+
| vx7-SC0630   |  Open for development                                                  |
+--------------+------------------------------------------------------------------------+
| SR0640       |  locked                                                                |
+--------------+------------------------------------------------------------------------+
| SR0650       |  Open for development                                                  |
+--------------+------------------------------------------------------------------------+
| SR0660       |  Any developer can create this branch at or after FC date              |
|              |  *Note:* if there are changes committed to SR0650 after FC date to fix |
|              |  bugs, the code should be merged into SR0660                           |
+--------------+------------------------------------------------------------------------+


**How to Integration code changes into Helix Guest Repository**
----------------------------------------------------------------
To submit code to `helix_guest_support <http://bitbucket.wrs.com/projects/VX7/repos/helix_guest_support/browse>`__, create a branch of <current release branch> (for e.g. SR0650), and test the code before merging it back into the <current release branch>.

Once the your code is approved and merged, follow these steps to apply the new code to VxWorks repository (`vx7-integration branch <http://bitbucket.wrs.com/projects/VX7/repos/vxworks/browse?at=refs%2Fheads%2Fvx7-integration>`__)

- capture the SHA of the merge (HEAD) of the  helix_guest_support <current release branch>
- create a branch of VxWorks repository vx7-integration branch
- update the .guestref file to add the SHA using this format:
  
  - <Helix Guest Support HEAD SHA> # <current release>
  - e.g.: c99536121df92000d5c0a59c3260ee564a1baf0c # SR0650

If this is the first time the package is being updated, a spec file up-rev is required (check notes below)

- push the code change to your branch and start Helix Launcher build to test
- Start CI Launcher to integrate your branch to vx7-integration (Please consult this Jive for more details Submitting Code into the Integration Branch)

Note: Sometimes updating the SHA requires spec file Version and changelog update. This is required the first time a package is update in the release. If spec file change is required, check the table below to identify the spec file.

**Location of spec files in VxWorks repository vx7-integration:**
------------------------------------------------------------------
These spec files are located under: `helix/guests/guest_packaging <http://opengrok.wrs.com/source/xref/vx7-integration/helix/guests/guest_packaging/>`__ 

+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| **Spec file Name in VxWorks repo**                                                                           | **Corresponding Helix Guest Support path/folder**           |
|                                                                                                              |                                                             |
|                                                                                                              | (see below for URLs to path/folder)                         |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `agl_arm.spec <https://jive.windriver.com/document/agl_arm.spec>`__                                          |  helix_guest_support/agl/agl-5.0.3                          |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `nxp_linux_4_nxp_imx8.spec <https://jive.windriver.com/document/nxp_linux_4_nxp_imx8.spec>`__                |  helix_guest_support /nxp-linux-4/nxp-imx8/                 |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `nxp_linux_4_nxp_s32g.spec <https://jive.windriver.com/document/nxp_linux_4_nxp_s32g.spec>`__                |  helix_guest_support /nxp-linux-4/nxp-s32g                  |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `windows_10.spec <https://jive.windriver.com/document/windows_10.spec>`__                                    |  helix_guest_support/windows-10/drivers                     |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `windows_7.spec <https://jive.windriver.com/document/windows_7.spec>`__                                      |  helix_guest_support/windows-10/driver                      |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_6_intel_x86_64.spec <https://jive.windriver.com/document/wrlinux_6_intel_x86_64.spec>`__            |  helix_guest_support /wrlinux/wrlinux-6                     |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_7_intel_x86_64.spec <https://jive.windriver.com/document/wrlinux_7_intel_x86_64.spec>`__            |  helix_guest_support /wrlinux/wrlinux-7                     |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_8_fsl_ls1046.spec <https://jive.windriver.com/document/wrlinux_8_fsl_ls1046.spec>`__                |  helix_guest_support /wrlinux/wrlinux-8.0.0.25/fsl-ls1046   |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_8_intel_x86_64.spec <https://jive.windriver.com/document/wrlinux_8_intel_x86_64.spec>`__            |  helix_guest_support /wrlinux/wrlinux-8.0.0.25/intel-x86-64 |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_8_renesas_rcar3.spec <https://jive.windriver.com/document/wrlinux_8_renesas_rcar3.spec>`__          |  helix_guest_support/wrlinux/wrlinux-8.0.0.25/renesas-rcar3 |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_8_xilinx_zynqmp.spec <https://jive.windriver.com/document/wrlinux_8_xilinx_zynqmp.spec>`__          |  helix_guest_support/wrlinux/wrlinux-8.0.0.25/xilinx-zynqmp |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_lts18_intel_x86_64.spec <https://jive.windriver.com/document/wrlinux_lts18_intel_x86_64.spec>`__    |  helix_guest_support/wrlinux/wrlinux-lts18/intel-x86-64     |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_lts18_nxp_imx8mq.spec <https://jive.windriver.com/document/wrlinux_lts18_nxp_imx8mq.spec>`__        |  helix_guest_support /wrlinux/wrlinux-lts18/nxp-imx8mq      |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_lts18_nxp_ls1046.spec <https://jive.windriver.com/document/wrlinux_lts18_nxp_ls1046.spec>`__        |  helix_guest_support /wrlinux/wrlinux-lts18/nxp-ls1046      |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| `wrlinux_lts18_xilinx_zynqmp.spec <https://jive.windriver.com/document/wrlinux_lts18_xilinx_zynqmp.spec>`__  |  helix_guest_support/wrlinux/wrlinux-lts18/xilinx-zynqmp    |
|  (*note:* url broken in orig jive page)                                                                      |                                                             |
+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+

**Helix Guest Support path/folder**
+++++++++++++++++++++++++++++++++++

- `helix_guest_support <http://bitbucket.wrs.com/projects/VX7/repos/helix_guest_support/browse>`__
- `agl <http://bitbucket.wrs.com/projects/VX7/repos/helix_guest_support/browse/agl>`__
- `nxp-linux-4 <http://bitbucket.wrs.com/projects/VX7/repos/helix_guest_support/browse/nxp-linux-4>`__
- `windows-10 <http://bitbucket.wrs.com/projects/VX7/repos/helix_guest_support/browse/windows-10>`__
- `wrlinux <http://bitbucket.wrs.com/projects/VX7/repos/helix_guest_support/browse/wrlinux>`__
- `wrlinux-8.0.0.25 <http://bitbucket.wrs.com/projects/VX7/repos/helix_guest_support/browse/wrlinux/wrlinux-8.0.0.25>`__
- `wrlinux-lts18 <http://bitbucket.wrs.com/projects/VX7/repos/helix_guest_support/browse/wrlinux/wrlinux-8.0.0.25>`__