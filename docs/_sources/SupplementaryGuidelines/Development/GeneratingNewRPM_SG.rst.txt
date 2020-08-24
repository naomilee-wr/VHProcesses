:orphan:

|
|
|

========================= 
Generating a New RPM
========================= 

|
|

**Purpose**
-----------

To provide a set of steps that needs to be followed when enabling the generation of a new RPM.  Failure to follow these steps will result in failing to generate a "spin".

|

**Steps**
----------

1. Submit changes into the 'vx7-integration' branch with the .spec file disabled and layer.vsbl file disabled (naming the files xxx.spec.disabled and layer.vsbl.disabled)

   - At this point code is inert and not interacting in any builds
   
2. When the layer builds correctly and has no layer dependency issues enable the layer.vsbl (rename layer.vsbl.disabled to layer.vsbl)

   - This will enable the layer in git related builds only
   
3. Enable the .spec file (by renaming xxx.spec.disabled to xxx.spec) with the 'Group' and '#VX7Group' elements set to "not-shipped" 

   - This allows a test installation of the layer from a spin and would also allow test to start testing the layer as they have access to unshipped RPMs
   
4. If the RPM Group name and RPM name alrealy exits and that has been vetted with a PdM, try both of the following spin generators with that data set in your private branch: 

   - http://vxjenkins2.wrs.com:8080/job/vx7_PR_launcher/ 
   
5. If both spin generators results in a "green",  then  enable the .spec file in 'vx7-integration' branch (enable in this context means committing the xxx.spec file with the 'Group', '#VX7Group', 'Name', and '#VX7Name' elements set to the PdM vetted names?).  

6. If either one of the above spin generators fails with an error such as "FAILURE in manufacture: Unsorted RPMs found"  then please contact '+vx-osconfig' via e-mail and the team will co-ordinate with manufacturing that all the appropriate steps have been made to support the new RPM in the group that PdM has requested it be in (PdM must be in the loop for name and group assignments).

7. The layer will be enabled with these settings only after both of the test spins above (step 4) have succeeded.

|

**Change Log**
--------------

+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/17/2020     | N/A            | 0.1            | Shree Vidya    | Transferred content from Generating   |
|                |                |                | Jayaraman      | a new RPM Jive page                   |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 08/24/2020     | N/A            | 0.2            | Shree Vidya    | Updates based on Shawn's feedback     |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+

