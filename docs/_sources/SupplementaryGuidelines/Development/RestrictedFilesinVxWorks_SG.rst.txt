:orphan:
|
|
|

================================= 
Restricted Files in VxWorks 7
=================================
**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

**Purpose:** 

(Source:https://jive.windriver.com/docs/DOC-76456)

Restricted files in VxWorks 7 are source code files that may impact binary compatibility for RTPs. Starting with VxWorks 7 SR0620, an RTP executable shall remain binary compatible with future "versions" of the kernel. This capability has been requested via Feature F8963.  See the following document for technical details on VxWorks RTPs and system calls: `VxWorks Real-Time Process (RTP) System Calls and Binary Compatibility <./VxWorksRTP_SystemCallsBinaryCompatibility_SG.html>`__
 
The following is the current list of restricted files in the VxWorks 7 run-time git repository:

- vxworks/helix/guests/vxworks-7/pkgs_v2/os/core/kernel/h/syscallArgs.h
- vxworks/helix/guests/vxworks-7/pkgs_v2/os/core/kernel/h/syscallLib.h
- vxworks/helix/guests/vxworks-7/pkgs_v2/os/core/kernel/h/private/syscallLibP.h
- vxworks/helix/guests/vxworks-7/pkgs_v2/os/arch/ppc/kernel/base/h/arch/ppc/syscallPpc.h
- vxworks/helix/guests/vxworks-7/pkgs_v2/os/arch/arm/kernel/armbase/h/arch/arm/syscallArm.h
- vxworks/helix/guests/vxworks-7/pkgs_v2/os/arch/ia/kernel/h/arch/i86/syscallI86.h
- vxworks/helix/guests/vxworks-7/pkgs_v2/os/arch/ia/kernel/h/arch/i86/x86_64/syscallX86_64.h
- vxworks/helix/guests/vxworks-7/pkgs_v2/os/arch/simulator/kernel/h/arch/simlinux/syscallSimlinux.h
- vxworks/helix/guests/vxworks-7/pkgs_v2/os/arch/simulator/kernel/h/arch/simnt/syscallSimnt.h
- vxworks/helix/guests/vxworks-7/pkgs_v2/os/core/syscalls/vxworks/syscall_defs/*
- vxworks/helix/guests/vxworks-7/build/mk/tcl/scgen.tcl

The official list of restricted files is maintained in the file vxworks/README-restricted-files.md. 

The git hooks (installed by setup-tools) check for modifications to the files and provide a warning to the developer. This warning is also appended to the commit message when making the commit so it is clear to the developer that they are committing a modification to a restricted file.

The Development team needs to Contact and work with the VxWorks Architects via the email alias: *vx-architects@list-int.wrs.com* on the changes before pushing changes into Git. When modifying a restricted file, consult with the Architects to ensure review and approval. 

In addition, the CI Pipeline will be updated to gate commits that have modified any one of the aforementioned files.

 
**Developer Responsibilities**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- The Code Collaborator "File Subscription" facility will ensure that the relevant VxWorks Architects are automatically added as a "Reviewer" to any reviews involving one or more of the restricted files outlined above. Ensure at least one of the architects approve the review, and do not change their role to "Observer".
- Commit locally.  If a restricted file is modified, notify the VxWorks architects using the *vx-architects@list-int.wrs.com* e-mail alias.
- An architect must be a "Reviewer" for the Code Collaborator review, or the CI pipeline build will fail (Update Pending)

|

**Change Log**
--------------
+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/18/2020     | N/A            | 0.1            | Shree Vidya    | Transferred content from Restricted   |
|                |                |                | Jayaraman      | Files in VxWorks 7 Jive page          |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+


