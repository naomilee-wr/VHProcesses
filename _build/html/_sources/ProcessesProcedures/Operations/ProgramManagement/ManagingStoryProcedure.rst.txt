:orphan:
|
|
|

=============================
Managing Story Procedure
=============================

|

**Purpose**
-----------

Stories represent a simplified functional requirement of an overall Feature/Epic; it is the unit by which teams plan and execute their development work.  A story is sized to complete in a single sprint.

This document provides guidelines on how to create  Stories for  development along with tips and recommendations on how to handle certain situation.  Given the nature of the work and the infinite possible scenarios, it is impossible to provide an exact process on how to manage Stories.  In the absence of clear guidelines, teams are advised to follow Agile principles when dealing with planning:

- Our highest priority is to satisfy the customer through **early and continuous delivery of valuable software**.
- **Welcome changing requirements**, even late in development. Agile processes harness change for the customer’s competitive advantage.
- **Deliver working software frequently**, from a couple of weeks to a couple of months, with a preference to the shorter timescale.
- **Business people and developers must work together** daily throughout the project.
- **Build projects around motivated individuals**. Give them the environment and support they need, and trust them to get the job done.
- The most efficient and effective method of conveying information to and within a development team is **face-to-face conversation**.
- **Working software is the primary measure of progress**.
- Agile processes **promote sustainable development**. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.
- Continuous attention to **technical excellence and good design** enhances agility.
- **Simplicity** — the art of maximizing the amount of work not done — is essential.
- The best architectures, requirements, and designs emerge from **self-organizing teams**.
- At regular intervals, the **team reflects on how to become more effective**, then tunes and adjusts its behavior accordingly.

|

**Important References**
------------------------

- `Technical Feature Owner - Jira Agile Responsibilities <./TechnicalFeatureOwner_JiraAgileResponsibilities.html>`__
- `Estimating with Story Point <https://jive.windriver.com/docs/DOC-61754>`__
- `Story Point Estimation Guideline <https://jive.windriver.com/docs/DOC-62124>`__
- `Story Level Definition of Done <./StoryDoneDefinition.html>`__

|

**Procedure**
-------------

- Once a Feature has been promoted to the "Selected for Development" state, a Technical Feature Owner (TFO) is assigned by the Engineering Manager
- It's the TFO's responsibility to groom, implement, and deliver their Feature to completion

  - The exact list of responsibilities for the TFO are listed in Technical Feature Owner Responsibilities
  
- Grooming Features into Stories is an iterative process that should involve all stakeholders.
- The following are the basic guidelines on how to groom and create Stories for Features:

  - **Breaking Down Features/Epics into Stories**

    - The TFO should start by creating Stories that capture known Feature requirements

      - These Stories will typically include such things as Documentation, Prototyping, Investigations, etc.
      - It's not important to "right-size" or estimate the Stories at this time; the goal is to try and identify big rocks
      - It's important that the team consider what kind of milestones they can achieve during the development process

        - Equally important, how will these milestones be tested?

  - **Refining Stories**

    - On a weekly basis the TFO should seek to refine Stories with the team

      - Consider what has the team learned so far?
      - What will developers be doing in the coming weeks?
      - Sprints don't need to be filled to capacity

        - Enter only what is actually known, the team can always add later

      - Can milestones be cut down into smaller deliverable chunks?  Or, are there missing milestones?

    - A Story should be sized to fit into approximately 5 to 10 days worth of work
    - As larger Stories are broken down, it may be difficult to hit the "right size", consider that:

      - Not all Stories need to deliver code into "vx7 integration"
      - It may take several Stories to deliver a particular functional piece

    - When creating a Story, it's important to understand what is being delivered:

      - If at the end of the US, code is being submitted into "vx7 integration", it should follow the VxWorks 7 Definition of Done (DoD): Story Level Definition of Done

        - Fulfilling the Vxworks 7 DoD requires time and effort, ensure that this is taken into consideration when estimating and scheduling

      - If at the end of the US, the developer will need more time:

        - They need to be able to show progress, and should create a new Story for the continuation of the work

          - Avoid creating Stories stating "Part 1", "Part 2", etc. Provide more precise details (as much as possible).

        - Developers should be expected to explain what they have achieved or discovered
        - Ideally, they can demonstrate partial console logs, or some other development artifact

  - **Scheduling Stories**

    - When scheduling a Story, developers must commit to its delivery!

      - Given the nature of VxWorks development, it can be very difficult to commit to finished code!

        - Don't commit to delivering code if you don't know for sure that you'll be able to!
        - Instead, try reducing the scope of the Story and present your progress to team members

          - Create a follow-up Story afterwards

      - Avoid overloading a developer

        - Stories that are scheduled to take an entire Sprint are risky!

          - Consider breaking down the Story into 2-parts and present your progress mid-Sprint for feedback

        - If you don't know for sure, don't add it to the Sprint!

          - Particularly relevant at the start of Feature work, there may be a lot of unknowns.  It may be impossible to completely fill the Sprint.
          - Instead, schedule a follow-up planning meeting mid-Sprint to present your findings and decide on what to do next.
	
  - **Estimating Stories and Tasks**

    - Team members are advised to look into these to derive an estimation that is appropriate for their teams.

      - `Estimating Story Process <./EstimateStoriesProcess.html>`__
      - `Estimating with Story Point <https://jive.windriver.com/docs/DOC-61754>`__
      - `Story Point Estimation Guideline <https://jive.windriver.com/docs/DOC-62124>`__
  
  - **Closing Stories**

    - Teams don't need to wait until the end of their Sprint to close on Stories

      - They are encouraged to do so on a weekly basis

    - The team should quickly cover each Story one-by-one:

      - Discuss with the Team on the Story's acceptance criteria
      - Ask the primary developer to present their deliverable
      - Engage with the Product Owner to get their Acceptance

    - Splitting or re-scheduling Stories should NOT happen

      - Only in very rare cases (e.g. an unforeseen interruption) is it acceptable to move a Story to another Sprint
      - Team members are expected to commit to only what they know (for sure!) they can deliver

        - As previously mentioned, if a developer is finding it hard to commit, reduce the scope of Story and regroup during the Sprint to discuss

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
| 06/22/2020     | N/A            | 0.2            | Shree Vidya    | Updates based on Roger's feedback     |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
