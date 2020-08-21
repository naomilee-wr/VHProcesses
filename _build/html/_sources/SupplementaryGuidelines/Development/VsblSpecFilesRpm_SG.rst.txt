:orphan:

|
|
|

========================================
Dealing with VSBL, Spec Files and RPMs 
========================================

|

In the course of VxWorks development, engineers will need to manipulate both layer VSBL files and RPM spec files.  These files contain important meta-data that instruct the build and manufacturing systems on how to configure and package code, respectively.  VSBL files are interpreted when manipulating VSBs, while spec files are interpreted during manufacturing.  

This guideline provides information and simple tips on dealing with these files to avoid common mistakes done by developers.

|

**Creating a new VSBL or Spec File**
--------------------------------------

When creating a new VSBL or spec file:

#. Start by copying an existing file from elsewhere in install tree.

   - The following is a simple example taken from a VxWorks Graphics driver:

     - `VSBL File <http://vxgit.wrs.com/projects/VX7/repos/vxworks/browse/vxworks-7/pkgs/ui/fbdev/fslipu/layer.vsbl>`_
     - `Spec File <http://vxgit.wrs.com/projects/VX7/repos/vxworks/browse/vxworks-7/pkgs/ui/fbdev/fslipu/fslipu.spec>`_

#. Contact your PLM to confirm what YUM Group the RPM belongs to. 

   - Check your associated Rally Feature, in most cases this information should be provided in the description (see picture below).  If it is not, please ensure it is updated either by PLM or TFO.

#. Ask the Release Operations Team or PLM to assign the new RPM into the appropriate YUM Group in the Delivery+ system.

|

**Modifying a VSBL or Spec File**
----------------------------------
- Most code modifications will require layer and/or RPM version numbers to be updated
   -  Note that code submissions into a release will automatically fail to merge if the affected RPM versions are not updated
   -  Guidelines on version numbers (and updating them) are provided in the VxWorks Coding Standard in the Reference section of Chapter 8 (see link above)

      **NOTE:  Developers should coordinate with their teams and RPM/layer owners to ensure that version numbers are correctly updated**
   
   -  When updating a spec file version, you must also provide a new Change Log entry that describes what has changed.

      The guidelines for Change Log entries is not currently published in the VxWorks Coding Standard, but can be referenced `here <https://jira.wrs.com:8443/projects/VXWCS/issues/VXWCS-21>`_ (under Internal Description).

- Any other type of modification requires a more thorough understanding of the VxWorks Configuration system.  You are strongly encouraged to read the Layers HLD (see link above) and to include a Build & Config representative in your code review.

- If updating an RPM's name or YUM Group, you must first seek PLM approval.  
  -  You must also uprev the RPM and its associated layer.

- Ask the Release Operations Team or PLM to assign the newly named RPM into the appropriate YUM Group in the Delivery+ system.

|

**Appendix:  Common Mistakes**
--------------------------------

**Creating New or Renaming RPMs**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Failing to communicate the RPM name to the Release Operations Team will cause a load build failure on the main line!
  -  The build failure will lead to the following warning: “rpm package is unsorted”
- Failing to uprev the RPM version will lead the Installer to use the older RPM (even if it's still in an older YUM Group).
  -  To ensure your newly name RPM is part of the correct YUM Group, you may access the R1 repository and check the groups.xml under dedicated profiles  (E.g. http://pek-cdftp/r1/vxworks/vxworks-7.0/<SPIN_NAME>/<YUM_GROUP_NAME>/repodata/groups.xml)
	 
**Defect Publication Mismatch**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The spec file Change Log is also used as a means of verifying that the company is publishing the appropriate defects for customer reference.

- All JIRA defect numbers appearing in a spec file Change Log must be published
    
  Note: that when in doubt on whether a defect should be published or not, ask yourself: Can a customer ever encounter this defect?
  

**Version mismatches**
~~~~~~~~~~~~~~~~~~~~~~~~~~~

When making changes to a layer's content, you have to remember to upgrade the layer version and the version in the spec file that ships the code.

- If the spec file is in the same directory as the modified layer source and the layer.vsbl, then you just need to upgrade the version numbers in both those files
  - a/layer.vsbl
  - a/xxx.spec
- If the spec file is in a directory above, then you need to modify not only the layer.vsbl in the directory that you are changing but the layer.vsbl and the spec file in the directory that ships your new code.
  - a/b/layer.vsbl
  - a/layer.vsbl
  - a/xxx.spec
- If there are multiple spec files in the same directory they all need to have the same version number, (this happens in some areas to ship arch specific code, here is an example from the hypervisor code)
  - /pkgs/os/hv/hypervisor/hypervisor.spec
  - /pkgs/os/hv/hypervisor/hypervisor_arm.spec
  - /pkgs/os/hv/hypervisor/hypervisor_ia.spec
  
**Wrong layer name used in LAYER_REQUIRES or FEATURE_REQUIRES statements**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- A common mistake is using the wrong layer name in the layer metadata, for example it would be incorrect to use PPP when you expected to create a dependency on the /pkgs/net/ipnet/linkproto/ppp layer.
   
- The easy way to get the correct name is to use the "vxprj vsb info PPP" or "vxprj vsb info IPNET_1_1_1_2_LINKPROTO_1_0_1_2_PPP_1_2_1_4" command and to select the "Target Name".
    
  >vxprj vsb info PPP

  Name:                     PPP
	
  VENDOR:                   Wind River
	
  VERSION:                  1.2.1.4
	
  FEATURE:                  NETWORKING
	
  TYPE:                     GENERIC
	
  Target Name:              IPNET_PPP
	
  Full Name:                IPNET_1_1_1_2_LINKPROTO_1_0_1_2_PPP_1_2_1_4
  

**Container layer version changes**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Some layers, IPNET or USB for example, contain no source files and are not really meant to change.  We call these container layers.  In SR0450 these layers (and spec files) were altered such that they installed under a versioned directory name. If you have to change something that these spec files you will have to upgrade every layer under them. This is a bit of a pain but it is not expected to happen very often.

|

**References**
--------------
`Latest Layers HLD <../../ProcessDocuments/CoreDev/CodingIntBuild/VSBLayerHLDv1_28.doc>`_

- Developers are strongly encouraged to review the HLD prior to modifying any VSBL files.  The HLD contains comprehensive information on the format and language used in these files.
- The HLD also contains important information related to creating and modifying Makefiles for VxWorks layers.

`Coding Standard <../../ProcessDocuments/CoreDev/CodingIntBuild/WindRiverVxWorksCodingStandard.pdf>`_

|

**Change Log**
--------------

+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**  | **Version**   | **Change By**           | **Description**                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
| 06/18/2020   | N/A                    | 0.1           | Naomi Lee               | Transferred content from DOC-57146 Jive page                                        |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+
|              |                        |               |                         |                                                                                     |
+--------------+------------------------+---------------+-------------------------+-------------------------------------------------------------------------------------+