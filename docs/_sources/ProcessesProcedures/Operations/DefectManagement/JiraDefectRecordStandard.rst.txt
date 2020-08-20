:orphan:

|
|
|

===============================
Jira Defect Record Standard
===============================

|

The Jira defect tracking tool is located at: http://jira.wrs.com.

The following table is a list of the fields in a Jira defect record and the description of the fields.

+--------------------------------------+-------------------------------------------------------------------------------+
|**Field**                             |**Description**                                                                |
+--------------------------------------+-------------------------------------------------------------------------------+ 
|**Project**                           |Jira Project.                                                                  |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Issue Type**                        |+--------------------------------------+--------------------------------------+|
|                                      || **Type**                             | **Description**                      ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Bug**                              | The terms Bug and Defect are used    ||
|                                      ||                                      | interchangeably. A defect is defined ||
|                                      ||                                      | as a failure of a work product to    ||
|                                      ||                                      | meet either:                         ||
|                                      ||                                      |                                      ||
|                                      ||                                      | -  Requirement                       ||
|                                      ||                                      | -  Design                            ||
|                                      ||                                      | -  Standard                          ||
|                                      ||                                      | -  Peer review checklist item        ||
|                                      ||                                      | -  Document template                 ||
|                                      ||                                      | -  Clarity                           ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Enhancement Request**              | An enhancement request is additional ||
|                                      ||                                      | functionality beyond the product     ||
|                                      ||                                      | requirements.                        ||
|                                      |+--------------------------------------+--------------------------------------+|
+--------------------------------------+-------------------------------------------------------------------------------+

|

**Overview Tab**
----------------

+--------------------------------------+-------------------------------------------------------------------------------+
|**Summary**                           |A brief one-line summary of the issue. For example, "Red Angry Nerd is scary." |
+--------------------------------------+-------------------------------------------------------------------------------+ 
|**Priority**                          |+--------------------------------------+--------------------------------------+|
|                                      || **Priority**                         | **Definition**                       ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **P1**                               | Highest priority. Indicates that     ||
|                                      ||                                      | this issue takes precedence over all ||
|                                      ||                                      | others.                              ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **P2**                               | Indicates that this issue is         ||
|                                      ||                                      | causing a problem and requires       ||
|                                      ||                                      | urgent attention.                    ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **P3**                               | Indicates that this issue has a      ||
|                                      ||                                      | significant impact.                  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **P4**                               | Indicates that this issue has a      ||
|                                      ||                                      | relatively minor impact.             ||
|                                      |+--------------------------------------+--------------------------------------+|
+--------------------------------------+-------------------------------------------------------------------------------+
|**Severity**                          |+--------------------------------------+--------------------------------------+|
|                                      || **Severity**                         | **Definition**                       ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Critical**                         | A **Critical** issue involves one or ||
|                                      ||                                      | more of the following conditions:    ||
|                                      ||                                      |                                      ||
|                                      ||                                      | -  data loss or corruption           ||
|                                      ||                                      | -  Loss of operations                ||
|                                      ||                                      | -  Failure of customer devices that  ||
|                                      ||                                      |    are in commercial operation with  ||
|                                      ||                                      |    end customers                     ||
|                                      ||                                      | -  'work stop' situation for         ||
|                                      ||                                      |    customer or end customer          ||
|                                      ||                                      | -  Grave impact to business          ||
|                                      ||                                      |    operations                        ||
|                                      ||                                      | -  Incorrect code is generated with  ||
|                                      ||                                      |    no warning or error message       ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Severe**                           | A **Severe** issue involves one or   ||
|                                      ||                                      | more of the following conditions:    ||
|                                      ||                                      |                                      ||
|                                      ||                                      | -  Loss of major functionality in    ||
|                                      ||                                      |    product                           ||
|                                      ||                                      | -  Work is severely impacted but can ||
|                                      ||                                      |    continue                          ||
|                                      ||                                      | -  Incorrect code is generated but a ||
|                                      ||                                      |    warning or error message is       ||
|                                      ||                                      |    generated                         ||
|                                      ||                                      | -  Product or customer device        ||
|                                      ||                                      |    crashes but product or device may ||
|                                      ||                                      |    be restarted                      ||
|                                      ||                                      | -  Business operations continue but  ||
|                                      ||                                      |    are significantly impacted        ||
|                                      ||                                      | -  Loss of data or data corruption   ||
|                                      ||                                      |    that is reversible                ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Standard**                         | A **Standard** issue involves one or ||
|                                      ||                                      | more of the following conditions:    ||
|                                      ||                                      |                                      ||
|                                      ||                                      | -  Problem encountered, but systems  ||
|                                      ||                                      |    are operational and development   ||
|                                      ||                                      |    continues                         ||
|                                      ||                                      | -  Product or customer device issues ||
|                                      ||                                      |    an error message but product or   ||
|                                      ||                                      |    device may be restarted           ||
|                                      ||                                      | -  Generated code is correct but not ||
|                                      ||                                      |    ideal (i.e. optimization not      ||
|                                      ||                                      |    done)                             ||
|                                      ||                                      | -  Business operations continue with ||
|                                      ||                                      |    minimal impact                    ||
|                                      ||                                      | -  Significant error in              ||
|                                      ||                                      |    documentation, or feature         ||
|                                      ||                                      |    documentation missing             ||
|                                      ||                                      | -  May have reasonable workaround    ||
|                                      ||                                      |    available                         ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Trivial**                          | A **Trivial** issue involves one or  ||
|                                      ||                                      | more of the following conditions:    ||
|                                      ||                                      |                                      ||
|                                      ||                                      | -  Minor documentation error, or     ||
|                                      ||                                      |    feature documentation needs       ||
|                                      ||                                      |    updating                          ||
|                                      ||                                      | -  No significant loss of            ||
|                                      ||                                      |    functionality in product          ||
|                                      ||                                      | -  Business operations are minimally ||
|                                      ||                                      |    affected                          ||
|                                      ||                                      | -  No data loss or corruption        ||
|                                      ||                                      | -  Cosmetic or nuisance issues       ||
|                                      |+--------------------------------------+--------------------------------------+|
+--------------------------------------+-------------------------------------------------------------------------------+
|**Affects Version**                   |Project version for which the issue is (or was) manifesting.                   |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Planned Fix in Release**            |Used for planning, can select a version that this fix will be fixed in.        |
|                                      |If multiple planned fixes are required, the user must clone the defect.        |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Planned Fix in Delivery**           |Text field allowing spin, DVD or other identifier that a defect is going       |
|                                      |to be fixed in.                                                                |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Patched In**                        |Patch versions.                                                                |
|*(if applicable)*                     |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Fix Version**                       |Project version in which the issue was (or will be) fixed.  When the issue     |
|*(if applicable)*                     |is resolved, this field is updated from the "Planned Fix in Release" field.    |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Environment**                       |The hardware or software environment to which the issue relates.               |
|*(if applicable)*                     |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Description**                       |A detailed description of the issue. (published on OLS)                        |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Internal Description**              |A description not published on On Line Support.                                |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Workaround**                        |How to get around the bug. (published on OLS)                                  |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Component(s)**                      |Project component(s) to which this issue relates.                              |
|*(if applicable)*                     |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Acknowledged**                      |Checkbox – issue has been acknowledged.                                        |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Assignee**                          |The person to whom the issue is currently assigned.                            |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Publish To OLS**                    |  -  None                                                                      | 
|                                      |  -  To be determined                                                          |
|                                      |  -  Reviewed -- Publish                                                       |
|                                      |  -  Reviewed -- Do NOT Publish                                                |
|                                      |  -  Never Shipped to Customer                                                 |
+--------------------------------------+-------------------------------------------------------------------------------+
| **Labels(s)**                        |Labels to which this issues relates.  Bug Board approval, marking customer     | 
| *(if applicable)*                    |specified defects and other activities are handled with labels.                | 
+--------------------------------------+-------------------------------------------------------------------------------+        
|**On Hold Disposition**               |The reason an issue has a status of "On Hold". Values:                         |
|                                      |  -  Incomplete                                                                |
|                                      |  -  Waiting for Customer                                                      |
|                                      |  -  Waiting for Vendor                                                        |
|                                      |  -  Waiting for Submitter                                                     |
|                                      |  -  Submitted to Open Source                                                  |
+--------------------------------------+-------------------------------------------------------------------------------+  

|      

**Environment Tab**
-------------------
+--------------------------------------+-------------------------------------------------------------------------------+        
|**Host OS**                           |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+        
|**Processor Architecture**            |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+        
|**Processor**                         |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+        
|**Environment**                       |                                                                               | 
+--------------------------------------+-------------------------------------------------------------------------------+        
|**Attachment**                        |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+        

**Details Tab**
---------------
+--------------------------------------+-------------------------------------------------------------------------------+        
|**Found Through**                     |-  None                                                                        |
|                                      |-  Analysis                                                                    |
|                                      |-  Inspection                                                                  |
|                                      |-  Other Peer Review                                                           |
|                                      |-  Other Review                                                                |
|                                      |-  Coding/Build                                                                |
|                                      |-  Testing                                                                     |
|                                      |-  Validation/Demo                                                             |
|                                      |-  Install/Configure                                                           |
|                                      |-  Support/Normal Use                                                          |
|                                      |-  Build Error or Warning                                                      |
|                                      |-  Static Analysis                                                             |
|                                      |-  Other- Explain                                                              |
+--------------------------------------+-------------------------------------------------------------------------------+   
|**Root Cause**                        |+--------------------------------------+--------------------------------------+|
|                                      || **Root Cause**                       | **Subcause**                         ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Requirements                         | Requirement Specification (Missing,  ||
|                                      ||                                      | Unclear, Incorrect, Changed)         ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Requirements                         | Functional Description (Missing,     ||
|                                      ||                                      | Unclear, Incorrect, Changed)         ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Requirements                         | User Interface (Missing, Unclear,    ||
|                                      ||                                      | Incorrect, Changed)                  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Requirements                         | Software Interface (Missing,         ||
|                                      ||                                      | Unclear, Incorrect, Changed)         ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Design                               | Functional Description (Missing,     ||
|                                      ||                                      | Unclear, Incorrect, Changed)         ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Design                               | User Interface (Missing, Unclear,    ||
|                                      ||                                      | Incorrect, Changed)                  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Design                               | Software Interface (Missing,         ||
|                                      ||                                      | Unclear, Incorrect, Changed)         ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Design                               | Data Definition (Missing, Unclear,   ||
|                                      ||                                      | Incorrect, Changed)                  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Design                               | Module Design (Missing, Unclear,     ||
|                                      ||                                      | Incorrect, Changed)                  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Design                               | Logic (Missing, Unclear, Incorrect,  ||
|                                      ||                                      | Changed)                             ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Design                               | Error checking (Missing, Unclear,    ||
|                                      ||                                      | Incorrect, Changed)                  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Design                               | Standards (Missing, Unclear,         ||
|                                      ||                                      | Incorrect, Changed)                  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Code                                 | Data Handling (Missing, Unclear,     ||
|                                      ||                                      | Incorrect, Changed)                  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Code                                 | Logic (Missing, Unclear, Incorrect,  ||
|                                      ||                                      | Changed)                             ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Code                                 | Module/Interface Implementation      ||
|                                      ||                                      | (Missing, Unclear, Incorrect,        ||
|                                      ||                                      | Changed)                             ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Code                                 | Standards (Missing, Unclear,         ||
|                                      ||                                      | Incorrect, Changed)                  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Tests                                | (Missing, Unclear, Incorrect,        ||
|                                      ||                                      | Changed)                             ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || Documentation                        | (Missing, Unclear, Incorrect,        ||
|                                      ||                                      | Changed)                             ||
|                                      |+--------------------------------------+--------------------------------------+|
+--------------------------------------+-------------------------------------------------------------------------------+  
|**Root Subcause**                     |See "**Root Cause**" above.                                                    |
+--------------------------------------+-------------------------------------------------------------------------------+  
|**Root Cause State**                  |-  None                                                                        |
|                                      |-  Missing                                                                     |
|                                      |-  Unclear                                                                     |
|                                      |-  Incorrect                                                                   |
|                                      |-  Changed                                                                     |
+--------------------------------------+-------------------------------------------------------------------------------+  
|**Is Regression?**                    |-  None                                                                        |
|                                      |-  Yes                                                                         |
|                                      |-  No                                                                          |
+--------------------------------------+-------------------------------------------------------------------------------+  
|**Safety Flaw**                       |Does this issue expose a safety flaw?                                          |
|                                      |-  None                                                                        |
|                                      |-  Potential                                                                   |
|                                      |-  Confirmed                                                                   |
|                                      |-  Disproved                                                                   |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Security Flaw**                     |Does this issue expose a security flaw?                                        |
|                                      |-  None                                                                        |
|                                      |-  Potential                                                                   |
|                                      |-  Confirmed                                                                   |
|                                      |-  Disprove                                                                    |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Email CC**                          |Other users who will get notification about the issue                          |
+--------------------------------------+-------------------------------------------------------------------------------+

|

**Testing Tab**
---------------

+--------------------------------------+-------------------------------------------------------------------------------+
|**Tester**                            |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Test Case**                         |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Test Status**                       |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+

|
 
**Records Tab**
---------------

+--------------------------------------+-------------------------------------------------------------------------------+
|**Rally Project**                     |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Rally User Story ID**               |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Rally Defect ID**                   |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Rally Link**                        |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**External System**                   |Used for tracing defects in an external/third party defect system such as      |
|                                      |Linux does with Yocto.                                                         |
+--------------------------------------+-------------------------------------------------------------------------------+
|**External System ID**                |External System ID                                                             |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Knowledge Forum URL**               |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Legacy ClearQuest ID**              |ClearQuest record from which this one has been imported.                       |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Rally ID**                          |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Alternate Create Date**             |Used for data migration.                                                       |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Alternate Resolve Date**            |Used for data migration.                                                       |
+--------------------------------------+-------------------------------------------------------------------------------+

|

**State Fields**
----------------

+--------------------------------------+-------------------------------------------------------------------------------+
|**Status**                            |+--------------------------------------+--------------------------------------+|
|                                      || **Status**                           | **Description**                      ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Open**                             | All bugs that are not in progress    ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **In Progress**                      | Assigned and actively being worked   ||
|                                      ||                                      | on                                   ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **On Hold**                          | Any reason that causes a defect to   ||
|                                      ||                                      | stop progressing. This is clarified  ||
|                                      ||                                      | further with the "**On Hold          ||
|                                      ||                                      | Disposition**" field                 ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Resolved**                         | Defect resolved. This status is      ||
|                                      ||                                      | further clarified by the             ||
|                                      ||                                      | "**Resolution**" field               ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Integrated**                       | Integration complete                 ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Closed**                           | Fix is verified or approved.         ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Reopened**                         |                                      ||
|                                      |+--------------------------------------+--------------------------------------+|
+--------------------------------------+-------------------------------------------------------------------------------+
|**Resolution**                        |+--------------------------------------+--------------------------------------+|
|                                      || **Resolution**                       | **Definition**                       ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Fixed**                            | A fix for this issue has been        ||
|                                      ||                                      | implemented.                         ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Won't Fix**                        | This issue will not be fixed, e.g.   ||
|                                      ||                                      | it may no longer be relevant.        ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Duplicate**                        | This issue is a duplicate of an      ||
|                                      ||                                      | existing issue. In the Link field,   ||
|                                      ||                                      | create a link to the duplicated      ||
|                                      ||                                      | issue.                               ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Cannot Reproduce**                 | This issue could not be reproduced   ||
|                                      ||                                      | at this time, or not enough          ||
|                                      ||                                      | information was available to         ||
|                                      ||                                      | reproduce the issue. If more         ||
|                                      ||                                      | information becomes available,       ||
|                                      ||                                      | please reopen the issue.             ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Resolved**                         | Issues resolved in manner other than ||
|                                      ||                                      | modifying source/docs                ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Not Applicable**                   | Issue verified to not be in the      ||
|                                      ||                                      | specified releases due to package    ||
|                                      ||                                      | upgrade, change in technology, etc.  ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Rejected**                         |                                      ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Withdrawn**                        |                                      ||
|                                      |+--------------------------------------+--------------------------------------+|
|                                      || **Replaced by Requirement**          | This resolution will only be         ||
|                                      ||                                      | available for issues that are        ||
|                                      ||                                      | enhancement requests.                ||
|                                      |+--------------------------------------+--------------------------------------+|
+--------------------------------------+-------------------------------------------------------------------------------+

|

**Other Fields**
----------------
+--------------------------------------+-------------------------------------------------------------------------------+
|**Reporter**                          |The person who entered the issue into the system.                              |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Created**                           |The time and date on which this issue was entered into JIRA.                   |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Updated**                           |The time and date on which this issue was last edited.                         |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Votes**                             |The number shown indicates how many votes this issue has.                      |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Watchers**                          |The number shown indicates how many people are watching this issue.            | 
+--------------------------------------+-------------------------------------------------------------------------------+

|

**Log Work Fields**
-------------------
+--------------------------------------+-------------------------------------------------------------------------------+
|**Time Spent**                        |An estimate of how much time spent working                                     |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Date Started**                      |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+ 
|**Remaining** **Estimate**            |The **Remaining Estimate**, i.e. the current estimate of the remaining         |
|                                      |amount of time required to resolve the issue.                                  |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Work Description**                  |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|                                      |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|                                      |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|                                      |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|                                      |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+

|

**Additional**
--------------

+--------------------------------------+-------------------------------------------------------------------------------+
|**Link**                              |A list of links to related issues.  (Strikethrough text indicates that an issue|
|                                      |has been resolved.)                                                            |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Due**                               |The date by which this issue is scheduled to be completed.                     |
|*(if applicable)*                     |                                                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Resolved**                          |The time and date on which this issue was resolved.                            |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Estimate**                          |The **Original Estimate** of the total amount of time required to resolve the  |
|                                      |issue, as estimated when the issue was created.                                |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Logged**                            |The sum of the **Time Spent** from each of the individual work logs for this   |
|                                      |issue.                                                                         |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Development**                       |If you use Bitbucket or Stash to manage your code repositories, you can create |
|                                      |code branches in your code development tools directly from JIRA issues.        |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Agile**                             |Lets you view your issue on your Scrum of Kanban board.                        |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Migrated from ClearQuest**          |Date of CQ/Jira migration.                                                     |
+--------------------------------------+-------------------------------------------------------------------------------+

|

**Security**
---------------

+--------------------------------------+-------------------------------------------------------------------------------+
|**Security Issue**                    |Mark if this is a security issue                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Origin of reported vulnerability**  |The source of the security issue                                               |
+--------------------------------------+-------------------------------------------------------------------------------+
|**CVSS V3 Score**                     |Unknown, or score 0.0 - 10.0                                                   |
+--------------------------------------+-------------------------------------------------------------------------------+
|**CVSS V3 Severity**                  |The severity (if available)                                                    |
+--------------------------------------+-------------------------------------------------------------------------------+
|**CVSS V3 URL**                       |The URL Result of CVSS V3 Calculator                                           |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Vulnerability ID**                  |e.g. CVE-2017-12581, CESA-2017:1759, OSSA-2017-003                             |
+--------------------------------------+-------------------------------------------------------------------------------+
|**Comment**                           |Internal details of the defect                                                 |
+--------------------------------------+-------------------------------------------------------------------------------+

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1          | Shree Vidya Jayaraman    | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+