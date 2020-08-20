:orphan:

|
|
|

===========================================
Definition of Done for Epics (Features)
===========================================

|

**Overview**
------------

-  An important concept that impacts the success of an Agile Project is having a common understanding and agreement throughout the team on the release's Definition of Done
-  Epics (features) that have not met the "DONE" criteria go back into the Product Backlog and their ranking is reviewed as part of backlog grooming and release planning.
-  The Product Owner/Technical Feature Owner or Delegate accepts the Epics (features). Note:  For Engineering Epics, the engineering team may accept the Epic.

|

**Definition of Done**
----------------------

The acceptance of Epic (feature) is contingent on the following criteria being met.

#. If applicable, HLD document updated and reviewed
#. Coding done
#. Code inspection done

   - Involve Technical Feature Owner/Domain Lead/Technical lead, Design peers and Product Architect as the reviewer
   - Involve Product Architect and scrum testers as observer
   - All reviewers have approved code review in the Code Collaborator

#. Ensure zero Coverity issues, zero compiler warnings for Epic's that delivery code

   - Provide Coverity and build logs evidence by running existing check script

#. Scrum team has written and executed story specific tests (Coverity)

   - Story test case coverage = 100%, pass rate > 90%
   - Deliver automation cases to release team
   - Test result should be reflected in the Test Management/Reporting System (LTAF)
   - Provide test logs

#. If applicable, Information Development ( Technical Publications) documentation updated or engineering technical overview submitted
#. New IP and encryption disclosed
#. If applicable, demo complete

   - Provide a demo live session (if possible) to Product Manager and Product Architect, and store a recording

#. Defects have been fixed prior to release

   - No gating P2 defects

#. All stories are accepted

|

**Change Log**
--------------

+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 05/21/2020     | N/A            | 0.1            | Shree Vidya    | Initial Draft                         |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/29/2020     | N/A            | 0.2            | Shree Vidya    | Updates based on Rodger's feedback    |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+