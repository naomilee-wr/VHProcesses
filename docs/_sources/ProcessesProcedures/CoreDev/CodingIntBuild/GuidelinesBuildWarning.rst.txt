:orphan:
|
|
|

=========================================== 
Build Warning Guidelines for VxWorks 7
===========================================

|

This document provides guidelines and information on build warnings for VxWorks 7. A nightly build warning report is generated from the VxWorks 7 integration branch and send out to development teams to review and analyze. The guideline on VxWorks 7 is to ensure there are "0" warnings within VxWorks code (3rd party code are excluded) when certain configurations are compiled with the indicated warnings flags. 

|

**Report & owners of build warning**
-------------------------------------

1. Daily report will be generated based on build tests of nightly test.
2. Build warning owners are generated based on the coverity ownership.
3. Building warning should be handled following P1 defect policy, even defects may not be created.

|

**Build warning flags enabled**
--------------------------------

1. In SR0600:
   - GCC: -Wall -Wsystem-headers -Wconversion -Wnosign-conversion -Wno-prio-ctor-dtor
   - LLVM: -Wall -Wsystem-headers -Wconversion -Wnosign-conversion 
2. In SR0610, we will enable –Wsign-convention. The complete flags are as below:
   - GCC: -Wall -Wsystem-headers –Wconversion -Wno-prio-ctor-dtor -Wsign-conversion
   - LLVM: -Wall -Wsystem-headers -Wconversion -Wsign-conversion
3. SR0620 and beyond
   - Guidelines here: `Resolving compiler warnings <ResolvingCompilerWarnings.html>`__

|

**Test cases used in build tests**
------------------------------------

**Build cases**
~~~~~~~~~~~~~~~~

|image0|

 
**Build with RTP/DKM/ShareLibraries**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

|image1|
 

**Build with ksoft/khard/soft (khard is the default one covered by other build tests)**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

|image2|

 
**Build configurations**
------------------------

Nightly build tests have full coverage on the combinations of build options:

1. All BSP & boards supported
2. smp & up
3. 32 & 64 bits support
4. Available CPU supported for IA


Detailed information can be found in LTAF from links in the report of nightly test.

|

**Notes**
----------

1. The difference of this build warning tests and the one in CI pipeline is the coverage of configurations. Nightly build test covered all the possible BSP/CPU combination.
2. File names in report may not be precise as the parallel build may corrupt the logs.
3. When same warning happened in several files which may map to several owners, only one owner will be identified. 
4. This summary dose not cover 653 related build warning in SR0600. This work is still under discussing. 

|

**Change Log**
--------------
+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/18/2020     | N/A            | 0.1            | Shree Vidya    | Transferred content from Build Warning|
|                |                |                | Jayaraman      | Guidelines Jive page                  |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+

.. |image0| image:: ../../../_static/CoreDev/CodingIntBuild/BuildWarning_Image0.jpg
.. |image1| image:: ../../../_static/CoreDev/CodingIntBuild/BuildWarning_Image1.jpg
.. |image2| image:: ../../../_static/CoreDev/CodingIntBuild/BuildWarning_Image2.jpg
