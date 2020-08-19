:orphan:

=============================================
Open Source BSP Process
=============================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

(Source: https://jive.windriver.com/docs/DOC-75360)

|

**Delivery Model:**
--------------------

Open source BSPs (aka, unsupported BSP) are provided for quick customer experimenting, it adopts 2 types of release comparing to the normal feature delivery:

- On train delivery with SR06x0

  - The code should have no impact to all the formal features and product
  - Codes are directly integrated into vx7-integration branch or vx7-SR06x0-features branch using CI launcher or pull request
  - Follow the FC date of  normal SR06x0 releases, feature code must be checked in before FC.

- Delivery on GitHub (`Wind River · GitHub <https://github.com/Wind-River>`__ )
   
  - It must be based on SR06x0 release
  - It has the necessary source tree and one README.md to describe how to use those source files
  - The corresponding code must be checked into vx7-integration, thus there's two situations:
  - The code already checked in at the same time of the base SR06x0 release (sync development)
   
    - The code delivered after SR06x0 release, but before SR06(x+1)0 release (Async development)

      - The delivered content must be merged back to SR06(x+1)0 release, that is another on train delivery with SR06(x+1)0 release

      - If there's updating, then the released GitHub content needs UpRev, or else, just update the README.md to indicate it's based on the new SR06(x+1)0 release.

**Stakeholders**
-----------------

+-----------------------+------------------------------------------------+------------------------------------+-----------------------+
| **Entry Criteria**    | **Responsibilities**                           |  **Contacts**                      |  **Notes**            |
+-----------------------+------------------------------------------------+------------------------------------+-----------------------+
|  PM                   | 1. BSP Feature creating, priority assign,      |  Yan.Yan@windriver.com             |                       |
|                       |    device support listing                      |  michel.chabroux@windriver.com     |                       |
|                       | 2. Help getting the HW and manuals             |                                    |                       |
+-----------------------+------------------------------------------------+------------------------------------+-----------------------+
|  EPM                  | 1. Working with Eng to monitor the feature     | rodger.williams@windriver.com      |                       |
|                       |    release states and ensure features are      |                                    |                       |
|                       |    completed                                   |                                    |                       |
|                       | 2. Monitoring and communicating any issues     |                                    |                       |
|                       |    regarding IP and Export                     |                                    |                       |
+-----------------------+------------------------------------------------+------------------------------------+-----------------------+
| Eng/Scrum Team        | 1. Scope discussing with PM, release plan      | shengjiang.wu@windriver.com        |                       |
|                       | 2. Feature development and quality assurance   | Shanghui.Ye@windriver.com          |                       |
|                       | 3. Working with stakeholders to make sure the  |                                    |                       |
|                       |    feature is released as planned              |                                    |                       |
|                       | 4. Upload contents to GitHub and responsible   |                                    |                       |
|                       |    for maintenance                             |                                    |                       |
+-----------------------+------------------------------------------------+------------------------------------+-----------------------+
| PT                    | 1. PA tracking to NoAction by default          | zoltan.laszlo@windriver.com        |                       |
|                       | 2. If there's new design/API change that       | andrew.gaiarsa@windriver.com       |                       |
|                       |    impact the current or future VxWorks        |                                    |                       |
|                       |    behavior, review and approve the content    |                                    |                       |
|                       |    change                                      |                                    |                       |
+-----------------------+------------------------------------------------+------------------------------------+-----------------------+
| IP                    | 1. Scan for GitHub licenses and get GitHub     | mark.gisi@windriver.com            |                       |
|                       |    contents published                          | alisa.sedneva@windriver.com        |                       |
|                       | 2. Review on train code to check no IP issues  |                                    |                       |
|                       |    for code delivered                          |                                    |                       |
+-----------------------+------------------------------------------------+------------------------------------+-----------------------+
| Export                | For GitHub release, non-GA external Software   | export-classification@windriver.com| See attached email    |
|                       | Distribution Request must be approved by export|                                    | as an example         |
|                       | team                                           |                                    |                       |
+-----------------------+------------------------------------------------+------------------------------------+-----------------------+

**License**
-----------------
- All files for open source BSP must include BSD license (`Wind River BSD-3-Clause Open Source Copyright/License Notice <https://jive.windriver.com/docs/DOC-44742>`__)
 
**Quality Assurance**
-----------------------
Unsupported BSPs are to be provided as-is (which is another way of stating “unsupported”) and are meant to enable customers and partners to start experimenting/developing on the target as quickly as possible. In other words, an open source BSP need not, and should not, have the same level of functionality as a supported BSP nor does it need to have the usual VxWorks production quality.

- WR does not ensure it's an formal release and no supporting is guaranteed to customer
- No formal feature test / regression test/release test are performed by test team
- However, scrum team must try best to make it high quality or equal quality of formal release to ease later formal integration. More over, if the code can be regarded as formal release, then use formal review and integrate to SR06X0 directly with formal quality criteria.
 

On the other hand, an open source BSP must meet some minimum standards:

- Scrum team will do internal feature functionality test to verify the BSP's functionality and driver features
- Scrum team will do vxtest (INCLUDE_TM_ALL) for the BSP to make sure it's passed
- Scrum team will do vxtest (INCLUDE_TM_OS_CORE_USER_SGND) test for RTP make sure it's passed
- Test results must be uploaded to release LTAF if it's an on train release.
- Code Review within Scrum team must be completed for all codes
- Workaround is allowed if the resolution effort is too big or new design is needed
- Coverity issues and warnings must be cleaned.
- Defects are allowed only if PM approved
- Know issues and limitations must be recorded in the BSP Document (target.txt)
- IP/Export get closed
 
If/when it’s decided to transition a BSP from “unsupported” to “supported”, the usual design and code reviews need to be performed on the BSP. Basically the BSP development should proceed as if starting from scratch from a design and review standpoint (with the benefit of having the source code from the “unsupported” version as reference).


**Working Model**
------------------
For a BSP release, any file folders may need to be updated, but per the request of unsupported BSP, it should have no negative impact to the formal released product. Thus, codes supporting the unsupported BSP are divided into two parts: 

- **Formal standard part** (full release test and regression)

  - This includes all the formal product that not related to this unsupported BSP on SR06x0, example: Python update, PPC update while the unsupported BSP is ARM
  - Driver/Core/Arch update that have impact to this unsupported BSP and all the other BSPs that introduced by other features
  - Driver/Core/Arch update introduced by this unsupported BSP
   
    - If the driver updates meet the release criteria and also useful to other BSPs, then there's no need to make it open source, just integrate to SR06x0 directly, example: http://codereview.wrs.com/ui#review:id=63115 
    - Some generic Core or Arch part may need to be updated to support this unsupported BSP, example: GicV3 update, new driver framework. As these updates are so generic that they impact all the other BSPs and all future work, they should not be treated as open source, instead, they must meet the release criteria and have all the quality and process for formal product to make sure they are well designed and have no side/negative impact to other parts.

- **Open source part**
   
  All open source part of an unsupported BSP is treated as self-contained package that put under the same unsupported folder: vxworks\helix\guests\vxworks-7\pkgs_v2\unsupported, and they all have BSD license.
  
  - Git
   
    - vxworks\helix\guests\vxworks-7\pkgs_v2\unsupported\rpi_3
    - vxworks\helix\guests\vxworks-7\pkgs_v2\unsupported\ti_k3_am65x
	  
  - Native Spin
   
    - [InstallDir]\vxworks-7\pkgs_v2\unsupported\rpi_3               (all open source contents of rpi_3 BSP)
    - [InstallDir]\vxworks-7\pkgs_v2\unsupported\ti_k3_am65x   (all open source contents of am65x BSP)
	  
  - For each BSP folder, the contents are something like below:
    - BSP:                          rpi_3\rpi_3  
    - PSL:                          rpi_3\bcm2837                   (Includes all the PSL contents and modified/cloned drivers)

- **Open source driver updates**

  - All the  open source drivers modified/updated/new written are in the PSL folder of the open source BSP part.
  - For drivers that needed to be modified specifically for this unsupported BSP, make a copy to the PSL folder, add open source license and modify accordingly
   
    - That means it cannot be delivered as formal release
    - Since the modified drivers are specifically for this BSP, there may have a copy for each unsupported BSP.
	  
  - For USB/Network/Storage drivers copied from the original layers, they must be built in the unsupported BSP open source PSL layer, if there are issues that cannot be resolved in the unsupported BSP folder, the original layer need to be modified, example: Public some header files.
   
    - Network drivers can be built out of pkgs_v2\net, no special change is needed
    - USB drivers can be built out of pkgs_v2\connectivity\usb with changes in the corresponding copied/modified drivers in open source BSP PSL folder, see `How to add USB driver into unsupported Raspberry Pi 3 BSP <https://jive.windriver.com/docs/DOC-77034>`__
    - Storage drivers has not been verified till now

- **Versioning**

  - Version is from 0.1.0.0 as all unsupported BSPs are regarded as new, and updated as the layer version scheme (`Versioning for Layers and Packages in VxWorks <https://jive.windriver.com/docs/DOC-24838>`__), only when it gets formal released, they'd be bumped to 1.0.0.0
   
  - So, the produced Spin version and GitHub's RPM based on SR06x0 release version examples are:
   
    - fsl_imx_<board_name>.0.1.0.0
    - fsl_imx6_<board_name>.0.1.0.0
    - fsl_imx.2.0.1.0     (formal released contents)
    - fsl_imx6.2.0.2.0   (formal released contents)
    - rpi_3.0.1.0.0
    - bcm2837.0.1.0.0
 
- **Layers**

  - It’s recommended to further reinforce the unsupported status of these BSPs by updating both the SYNOPSIS and HELP text to indicate that the BSP is unsupported, e.g.

.. code-block:: rst
	
   Layer rpi_3
   {
    SYNOPSIS         (Unsupported) Raspberry Pi 3 family board support \ package (BSP)
    HELP             (Unsupported) This layer provides the Raspberry Pi 3 \ family board support package.
    VERSION          0.1.0.0
    VENDOR           Wind River
    LAYER_REQUIRES   FDT VXBUS_DRV UTILS BCM2837 ARM
    FEATURE_REQUIRES
    LAYER_STATUS     UNSUPPORTED
   }

.. code-block:: rst

   Layer BCM2837
   {
    SYNOPSIS          (Unsupported) BCM2837 processor support libraries
    HELP              (Unsupported) This provides the BCM2837 processor \ support libraries (PSL).
    VERSION           0.1.0.0
    VENDOR            Wind River
    FEATURE           PSL
    VSB_REQUIRES      ARCH_arm
    LAYER_REQUIRES    FDT SERVICE UTILS VXBUS
    FEATURE_REQUIRES
    OPTIONAL          YES
    DEFAULT           NO
    LAYER_TYPE        PSL
    LAYER_STATUS      UNSUPPORTED
   }

**IP/Export**
------------------
- All contributors must take IP training and test here: https://www.classmarker.com/online-test/start/?quiz=fc35bb292d40ed6b
- For on train BSP release

  - All codes delivered must be reviewed by IP team as early as possible if no more changes to codes, better at FC
  - EPM will send out IP/Export confirmation to each contributor just as formal release

- For GitHub release

  - Unsupported BSP repo is created and set to internal on Wind River · GitHub 
  - If the repo is created already, it will be kept as public
  - Scrum team uploads code to the repo using **pull request** so IP team can review
  - IP team review and Scrum team fix issues, then the pull request can be merged to main branch
  - Scrum team prepares export "non-GA External Software Distribution Request" and send to "export-classification@windriver.com" for approval.
  - If IP and export got approval, the BSP repo will be set public by IP team

**Documentation**
------------------
- Only target.txt is used for customer's references under the unsupported BSP folders, no any APIGEN markup and just pure TXT file for customer reference.

  - Do not want to use README.md to differentiate with the formal released BSP contents in knowledge library.
  - When the unsupported BSPs are going to be integrated as formal BSPs, the target.txt will be divided into README.md and BSP supplement guide in knowledge library.
   
- On GitHub, the README.md is a simple description of how to use the source tree to install on a released VxWorks 7 versions.

**Sustaining**
------------------
- No Customer sustaining work is guaranteed
- On each new SR06x0 release, the Scrum team who made the unsupported BSP will check if it still works by running vxtest (INCLUDE_TM_ALL) and vxtest (INCLUDE_TM_OS_CORE_USER_SGND)

  - If defect existed, the Scrum team will estimate the effort of fix and discuss with PM whether it should be still a valid unsupported BSP on the new SR06x0 release


**References**
--------------
- GitHub of RPI_3:  `VxWorks 7 Raspberry Pi 3b/3B+ Community BSP (GitHub) <https://github.com/Wind-River/vxw7-bsp-raspberry-pi>`__
- `Open Source BSP Working Model <https://jive.windriver.com/docs/DOC-77042>`__
- Folder and Name Change (http://codereview.wrs.com/ui#review:id=62215, http://codereview.wrs.com/ui#review:id=62258)
- `Unsupported BSP Guideline <https://jive.windriver.com/docs/DOC-74003>`__
- `Quick BSP Release and Planning <https://jive.windriver.com/docs/DOC-74004>`__