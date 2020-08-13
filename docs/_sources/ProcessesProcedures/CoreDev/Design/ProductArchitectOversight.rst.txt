:orphan:
|
|
|

======================================================
Product Architect Oversight
======================================================

**Purpose**
-----------

The Development team must ensure that the development of new features/epics has the appropriate architectural oversight. This oversight is key in making sure the product remains coherent and abides by the organization's values.  The following document provides a combination of process description and recommendations on how to ensure oversight.

|

**Important References**
------------------------

- `Code Review Procedure Using Code Collaborator Tool <../CodingIntBuild/PeerReviewProcedure_CodeCollaborator.html>`__

|
 
**Feature/Epic in Jira Agile**
------------------------------

- Product Architect(Product Owner/PA-Owner) are assigned as soon as Features/Epics get promoted into the "Selected for Development" state  

  - It is the the assigned PA-Owner's responsibility to contact the Technical Feature Owner to establish an ongoing dialogue
  - Following the initial introduction, it is the development team's responsibility to keep their PA-Owner updated of any meaningful development or changed within the Feature/Epic

- A PA-Owner can request a “Proof of Concept” (PoC) to be demonstrated prior to a Feature being promoted to "Selected for Development" (a PA-PoC Story is created in Jira Agile to track the request)

  - The PoC must be demonstrated before an HLD is started
  - The PA-Owner needs to be involved in all brainstorming session(s) regarding the PoC

    - A Workbench PoC can involve the generation of GUI wizard and workflow mockups

- The PA-Owner should be invited to all scrum, planning, grooming, and retrospective, etc. meetings associated with development of the feature/epic

  - The intent of this is to promote involvement between Developers and PA-Owners, and meeting attendance should be adjusted as necessary
  - If the PA-Owner cannot attend any of the aforementioned meetings, due to time zone differences, for example, the meeting minutes should be summarized and distributed to the meeting attendees and the PA-Owner
  - The information from these meetings, either by direct attendance or from the meeting minutes, shall be used by the PA-Owner to estimate the amount of time that needs to be allocated to provide adequate support to the scrum team(s) in developing the feature.  Specifically, the estimated effort should include code reviews
  - If any aspect of the information provided in any of the aforementioned meetings is not clear enough, the PA-Owner shall request clarification or more information.

- To encourage a closer coupling between PA-Owners and Developers, PA-Owners can be assigned “actual work” (e.g. perform some coding, generate some documentation, generate uTest or vxTest code)

  - This is needs to be agreed on by both the Development team and PA-Owners
    
|

**Code Review in Code Collaborator**
-------------------------------------

- The following process information pertains to the PA-Owner related aspects of the general code review process captured `Code Review Procedure Using Code Collaborator Tool <../CodingIntBuild/PeerReviewProcedure_CodeCollaborator.html>`__
- The PA-Owner shall be added as a “Reviewer” in Code Collaborator reviews.  The PA-Owner can certainly downgrade themselves to “Observer”, but the default role for the PA-Owner when creating the review should be “Reviewer”
- A "2-day" grace period shall be provided which allows a PA-Owner to respond.  The purpose of the grace period is two-fold:

  - to provide sufficient time for a PA-Owner to respond to a code review initiated in a different time zone, and
  - to prevent PA-Owner inactivity from stalling the scrum teams progress.

- A PA-Owner should immediately, or on the next day from the perspective of a scrum team in a different time-zone, assess whether they can/should actively participate in the code review.  The following scenarios can occur:

  - The PA-Owner doesn’t have sufficient time in the short term and/or perhaps doesn’t feel their participation is critical: The PA-Owner should change their role to “Observer”
  - The PA-Owner is able to provide comments immediately: the code review proceeds as usual until “Completion”
  - The PA-Owner’s participation in the review is deemed critical, but the PA-Owner doesn’t have sufficient time in the short term to provide useful/insightful comments.  In this case, it is recommended that the PA-Owner add a comment in the general ‘Chat’ section of the comment indicating that they plan on providing review comments “shortly” (in a few days).   Note that as mentioned above, a PA-Owner should be involved in Scrum team meetings (and sprint planning meetings) and thus a PA-Owner should be aware of any pending code reviews (and allocate sufficient time to perform the review).  Thus it's expected that this 3'rd scenario is relatively rare.
  - If a PA-Owner appears to be unresponsive, i.e. one of the above 3 actions have not occurred, after 2 days, the scrum team should explicitly remind the PA-Owner (via a Code Collaborator “Poke” and/or a direct e-mail) that their participation as a “Reviewer” is required.
  - If a PA-Owner continues to be unresponsive to a “Poke” and/or direct e-mail after another 1 day, then the scrum team can change the role to “Observer”
  
- A 'PA-Owner' will indicate acceptance of a feature by changing the 'PA-Tracking' of the feature/epic from "SprintReady" to "Accepted"

- **IMPORTANT: All of the above activities only pertain to the PA-Validation related activities, i.e., the existing PA-HLD related process is to remain as-is.** 	
	
|

**Change Log**
--------------

+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/16/2020     | N/A            | 0.1            | Shree Vidya    | Transferred content from Ensuring PA  |
|                |                |                | Jayaraman      | Oversight Jive page                   |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
