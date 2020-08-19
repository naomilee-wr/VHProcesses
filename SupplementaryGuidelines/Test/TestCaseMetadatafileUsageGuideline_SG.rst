:orphan:
|
|
|

=========================================================
Test Case Meta Data File (test_case.conf) Usage Guideline
=========================================================
**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

**Purpose:**

(Source: https://jive.windriver.com/docs/DOC-80297)
|

**General Guideline**
---------------------

One test suite needs one test_case.conf file in the associated git repo directory. For VxTest cases in C, one C file is treated as one test case.

After git check-in of test case meta data, use “Sync Test Repo” in LTAF GUI to import those test cases to LTAF database.

|

**Detail guideline by example**
-------------------------------

Follow test_case.conf file example in git: 
http://git.wrs.com/cgit/projects/wassp-repos/testcases/vxworks7/tree/networking-kong/IPNET/test_case.conf 

TEST_SUITE_NAME:  Test suite directory or file name. For example, IPNET or tmMemLib.c
COMPONENT: Same as the component names we used in release LTAF report, such as core, networking, etc.
TEST_CASE_TYPE: Must choose only one of these values (Functional, System, Performance, Compliance, Stress, Negative and OOBE)
FEATURE: Optional. Anything put here will be displayed in the "TC Feature" drop down list in LTAF.
AUTOMATION: yes or no
RCA: yes or no
DESCRIPTION: Put test suite or test case description here. It is shown as LTAF "Description" column.
TRACEABILITY: Put requirement IDs or tags here (Rally feature ID, User story ID, JIRA ID or other tag listed in this guide). Use comma to separate multiple IDs, for example, "F1234, US6789,V7NET-5000". For security testing, add tag "security" as an ID.
TEST_CASE_LIST: List one or more test case name here. You could set automation and traceability for each test case by following this example: http://git.wrs.com/cgit/projects/wassp-repos/testcases/vxworks7/tree/meta_data/core/tmSyscallCorruptSpTest/test_case.con… 
GIT_LINK: Test case meta data directory git tree link.
CREATED_DATE: Use YYYY-MM-DD format, like 2017-06-23.
RELEASE_NAME: Leave it blank.

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 07/15/2020   | N/A                     | 0.1           | Shree Vidya Jayaraman   | Transferred content from DOC-80297 jive page                                                        |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+