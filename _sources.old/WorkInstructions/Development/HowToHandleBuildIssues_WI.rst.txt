:orphan:

=============================================
How to Handle Build Issues
=============================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

Build issues can be related to the software pipeline, as well as infrastructure issues.

(Source: https://jive.windriver.com/docs/DOC-85089)

**Software Pipeline**
---------------------

A software pipeline consists of a set of automated elements (processes and tools), that allow developers to build, test and deploy their code in the integration stream.

The pipeline process verifies the code to be submitted satisfies a set of checklists prior to being checked in, such as:

- No new static analysis issues
- No new build warnings
- Code reviews have been completed
- Sanity / Unit tests performed
- State of defect, story, epic is correct

Pipeline tools that support the processes:

- Revision Control System:

  - Git
   
    - Access and availability provided by Engineering Success
    - Structure and process by VxWorks
	
  - Bit Bucket
  
    - Access and availability provided by Engineering Success
    - Structure and process by VxWorks
	
- Compiler and Static Code Analysis:
  
  - Jenkins

    - Owned and maintained by VxWorks
	
- Code Collaborator

  - Access and availability provided by Engineering Success
	
  - Structure and process by VxWorks

- Coverity

  - Access and availability provided by Engineering Success
  - Structure and process by VxWorks

- Test Harness

  - Access and availability provided by Engineering Success
  - Structure and process by VxWorks

- Jira

|image0|

**Infrastructure**
---------------------

The Infrastructure consists of the components – hardware and software - that are supporting the software development environment.

Ownership:

- Physical Build Servers, OS, structure, maintenance, space – VxWorks
- Jenkins Servers, OS, structure, maintenance, space – VxWorks
- Targets – VxWorks
- R1 – Build repository server space, storage, maintenance and structure – VxWorks
- Virtual Build Servers – IT

Services:

- Infrastructure residing in IT owned space: Space, Power, and network access is supported by IT, everything else is by VxWorks
- Infrastructure residing in Engineering labs: Space, Power, and network access is supported by Engineering Success, everything else is by VxWorks 

  Note: “Space” is physical space/racks for servers/targets not hard drive space

Categories:

- Network Services

  - Firewalls
  - Hardware
  - Wireless Connectivity
	
- Servers & Data

  - Drive space
  - Operating Systems

**Build failures**
---------------------

Every build failure has to be tracked via a P1 defect.

This defect should be created by the Build & Config Team (see Note at the end of the document)

When creating the defect, [Build Failure] should prefix the summary.

Example:

[Build Failure]: VX7 Build Results for 20200418061605_vx7-native : FAILED due to installer conflicts

Once the defect is created, the Build & Config team would do the initial analysis, to understand the root cause and properly classify / re-direct the defect.

Build failures can have different causes – labels can be used to classify the root cause.

**Pipeline issues**
---------------------

In order to be able to determine if the issue is caused by a service not being available / not functioning properly, following dashboard has to be reviewed:
http://noc.wrs.com:3000/d/sQykHLZZz/engineering-services?orgId=1&refresh=5m

- Issue relates to the Tools access and availability

  - To be used when it was confirmed the tools are not available
  - Labels: **Vx_BUILD_PIPELINE_ISSUES**
   
    - “Tools” label should be used in addition to above, to capture an issue related to git, Code Collaborator, Coverity, Jira, Bit Bucket not being available
	  
  - A “Support Request” should be opened with the Engineering Support team
   
    - Create Issue
    - Select Project = Infrastructure Support
    - Issue Type = Support Request
    - Component/s =  select the component that matches the Tools causing the issue

  - Note: the Support Request may be moved to IT for resolution

|image1|

- Issue relates to the Tools structure and process 

  - To be used when tools are available, but issue is related to process / structure or for any Jenkins related issue
  - Labels: **Vx_BUILD_PIPELINE_ISSUES**
   
    - “VxWorks” label should be used in addition to above
    - The defect will be created in the “Vx7 Build & Host Side Tools” project
    - Resolution may be provided by the Build & Config team, or by the submitters in the build, depending if issue is related to structure or process

- Issue relates to a submission in the pipeline 

  - Labels: **Vx_BUILD_PIPELINE_ISSUES**

    - “Dev” label should be used in addition to above, to capture the issue relates to a submission
    
  - Defect should be created in the “Vx7 Build & Host Side Tools” project

    - Build & Config team will do the initial analysis and, based on the results, can assign the defect to the designer who’s submission caused the failure
    - See “Service Level Agreement” section for more details

**Infrastructure issues**
--------------------------

Those are related to any of the Categories listed under the “Infrastructure” section

- Issue relates to infrastructure owned by VxWorks 

  - Those issues could be related to:

    - Physical Build Servers, OS, structure, maintenance, space
    - Jenkins Servers, OS, structure, maintenance, space
    - Targets 
    - R1 – Build repository server space, storage, maintenance and structure 

  - Labels: **VX7_BUILD_INFRASTRUCTURE_ISSUES**

    - “VxWorks” label should be used in addition to above
    - The defect will be created in the “Vx7 Build & Host Side Tools” project
    - Resolution should be provided with the help of the owners of the infrastructure

- Issue relates to services provided by infrastructure residing in Engineering labs 

  - Those issues could be related to:

    - Space 
    - Power
    - Network Access

  - Labels: **VX7_BUILD_INFRASTRUCTURE_ISSUES**

    - “LabOPS” label should be used in addition to above
    
  - A “Support Request” should be opened with the Engineering Support team

    - Create Issue 
    - Select Project = Lab Ops
    - Issue Type = Support Request
    - Component/s =  select the lab where the ownership resides

  - Note: the Support Request may be moved to IT for resolution
 
|image2|

- Issue relates to services provided by infrastructure residing in IT owned space 

  - Those issues could be related to:

    - Space 
    - Power
    - Network Access
    - Virtual Build Servers

  - IT issues are tracked via “Remedy Force” tickets

  - To have visibility on the VxWorks project side, a P1 defect should be created, to track the issue

    - Project = Vx7 Build & Host Side Tools
    - Component = Build, Packaging and Media
    - In the summary, the Remedy Force ticket should be referenced
    - Labels: **VX7_BUILD_INFRASTRUCTURE_ISSUES**
	
      - Labels that could be used in addition to the above: 
      		
        - “Network” -  network  related issues 
      		
        - “Servers” – server related issues

    - The B&C defect will be put “On Hold”, until the Remedy Force ticket is resolved

|image3|

**Quick Reference**
---------------------

+--------------------+-----------------------------------+---------------------------------------+-------------------------------------------------------+
| **ISSUE**          | **WHEN**                          | **LABELS**                            | **WHAT**                                              |
+--------------------+-----------------------------------+---------------------------------------+-------------------------------------------------------+
| Pipeline           | Tools access and availability     | Vx_BUILD_PIPELINE_ISSUES & Tools      | “Support Request”  with the Engineering Support team  |
+--------------------+-----------------------------------+---------------------------------------+-------------------------------------------------------+
| Pipeline           | Tools structure and process	 | Vx_BUILD_PIPELINE_ISSUES & VxWorks    | Defect in “Vx7 Build & Host Side Tools” project       |
+--------------------+-----------------------------------+---------------------------------------+-------------------------------------------------------+
| Pipeline           | Issue related to submission	 | Vx_BUILD_PIPELINE_ISSUES & Dev        | Defect in “Vx7 Build & Host Side Tools” project       |
|                    |                                   |                                       |                                                       |
+--------------------+-----------------------------------+---------------------------------------+-------------------------------------------------------+
| Infrastructure     | Infrastructure owned by VxWorks   | Vx_BUILD_PIPELINE_ISSUES & Dev        | Defect in “Vx7 Build & Host Side Tools” project       |
|                    |                                   |                                       |                                                       |
+--------------------+-----------------------------------+---------------------------------------+-------------------------------------------------------+
| Infrastructure     | Services provided by              | VX7_BUILD_INFRASTRUCTURE_ISSUES       | “Support Request”  with the Engineering Support team  |
|                    | infrastructure residing in        | & LabOPS                              |                                                       |
|                    | Engineering labs                  |                                       |                                                       |
+--------------------+-----------------------------------+---------------------------------------+-------------------------------------------------------+
| Infrastructure     | Services provided by              | VX7_BUILD_INFRASTRUCTURE_ISSUES &     | Remedy Force + Defect in “Vx7 Build & Host Side       |
|                    | infrastructure residing in IT     | Network & Servers                     | Tools” project                                        |
|                    | owned space                       |                                       |                                                       |
+--------------------+-----------------------------------+---------------------------------------+-------------------------------------------------------+


**Service Level Agreement**
----------------------------

- Anyone submitting into a build is expected to monitor the build results and ensure that the load gets generated properly
- If the load does not build successfully, 7x24 focus until correction is done
- No new submissions are allowed until the issue is solved

**Note**
+++++++++

A backup team will be available in China, for CI pipeline related work.

This team will have the ability to lock CI/approve pull request/kick-start the build.

.. |image0| image:: /_static/WorkInstructions/Development/HowToHandleBuildIssues_Image0.jpg
   :width: 400pt
   
.. |image1| image:: /_static/WorkInstructions/Development/HowToHandleBuildIssues_Image1.jpg
   :width: 400pt   

.. |image2| image:: /_static/WorkInstructions/Development/HowToHandleBuildIssues_Image2.jpg
   :width: 400pt

.. |image3| image:: /_static/WorkInstructions/Development/HowToHandleBuildIssues_Image3.jpg
   :width: 400pt