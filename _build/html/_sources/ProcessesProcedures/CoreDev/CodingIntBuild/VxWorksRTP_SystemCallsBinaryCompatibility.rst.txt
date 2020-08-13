:orphan:
|
|
|

==========================================================================
VxWorks Real-Time Process (RTP) System Calls and Binary Compatibility
==========================================================================

|

This document provides background information about VxWorks Real-Time Processes (RTPs) and the mechanism for RTPs to invoke kernel services via system calls. This document also provides detailed information on how to add or modify VxWorks 7 system call services.

Regarding the modification (or deletion) of existing VxWorks 7 system calls, starting with SR0620, a binary compatibility guarantee is being provided to customers (see Feature F8963). In other words, the execution of RTP binaries built against an SR0610 kernel shall be supported on a similarly configured kernel any future “release”.

The key caveat with respect to the binary compatibility guarantee is that the VSB/VIP for building the kernel on which the RTP binary will be executed against must have an “equivalent” composition and configuration as the VSB/VIP used to originally build the RTP. Also, the term “release” in the previous paragraph really means any combination of layer versions, regardless of the scope of the layer version increments, provided in future releases (assuming of course that the resultant VSB/VIP has an equivalent composition and configuration as the “original” VSB/VIP).

Thus, in general, existing system calls should not be modified or deleted unless approved by the appropriate VxWorks architect(s) and Product Management. The term “system calls” not only refers to the signature and numbering of the system call themselves, but to any kernel functionality invoked by the system call handler.

This document is an essential reference any engineer who intends to add or modify a system call to the VxWorks operating system.

|

**Change Log**
--------------
+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/18/2020     | N/A            | 0.1            | Shree Vidya    | Transferred content from VxWorks RTP  |
|                |                |                | Jayaraman      | System Calls and Binary Compatibility |
|                |                |                |                | Jive page                             |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+


