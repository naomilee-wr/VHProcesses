:orphan:

|
|
|

=============================================
Defect Creation and Publication Guidelines
=============================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

(Source: https://jive.windriver.com/docs/DOC-70924)

**Procedure:**
---------------

Defect Creation Guidelines
+++++++++++++++++++++++++++

When creating a defect, besides the mandatory Jira fields (marked with " * "), below fields should be also filed in. 

These fields are queried to ensure the defect provides sufficient information that allows the investigation to start. Failure to fill in these fields could result in the defect being re-assigned to the reporter.

+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| **Jira Tab**                | **Jira Field**                         | **Details**                                                                          |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Description                            | Provide a summary of the issue                                                       |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Reproducibility                        | Select from the pull down menu                                                       |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Steps to Reproduce                     | This field should allow any user to reproduce the defect. It should also give a      |
|                             |                                        | quick explanation on what the expected outcome should be in contrast to the actual   |
|                             |                                        | result.                                                                              |
|                             |                                        |                                                                                      |
|                             |                                        | Make sure to not use the following:                                                  |
|                             |                                        |                                                                                      |
|                             |                                        | - Barcode                                                                            |
|                             |                                        | - Git info                                                                           |
|                             |                                        | - Repo                                                                               |
|                             |                                        | - Jenkins                                                                            |
|                             |                                        | - Spin name                                                                          |
|                             |                                        | - WASSP                                                                              |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Environment                 | Environment                            | Provide details of the environment used                                              |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+


Please note also the values to be entered for below fields:

+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| **Jira Tab**                | **Jira Field**                         | **Details**                                                                          |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Found in Versions                      | Release name: "SRxxx" or "CRxxx". Enter one value only: the release in which the     |
|                             |                                        | defect was found.                                                                    |
|                             |                                        |                                                                                      |
|                             |                                        | Mandatory Jira Field                                                                 |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Fix Version                            | Release name:  "SRxxx" or "CRxxx"                                                    |
|                             |                                        |                                                                                      |
|                             |                                        | Mandatory Jira Field                                                                 |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Found in Release                       | RPM version                                                                          |
|                             |                                        |                                                                                      |
|                             |                                        | Optional Jira Field - recommendation to enter the RPM version                        |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Fixed in Release                       | RPM version                                                                          |
|                             |                                        |                                                                                      |
|                             |                                        | Optional Jira Field - recommendation to enter the RPM version                        |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+


Defect Publication Guidelines
++++++++++++++++++++++++++++++

- If "Found in Versions" = "Fixed Version" the defect is not published.
- The editable fields that get published on OLS are captured below.
- For more information on publication guidelines, see `Vx-7 Defect Publication Guidelines <https://jive.windriver.com/docs/DOC-49197>`__  

+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| **Jira Tab**                | **Jira Field**                         | **Guidelines**                                                                       |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Severity                               | Severity Definitions:                                                                |
|                             |                                        |                                                                                      |
|                             |                                        | - *Critical*: Product is not functionally usable.  System crash or major data loss.  |
|                             |                                        |   No workaround is available.                                                        |
|                             |                                        | - *Severe*: A feature is not meeting a defined specification. Major functionality    |
|                             |                                        |   is impacted. A workaround may be available.                                        |
|                             |                                        | - *Standard*: A feature is not working well but meets defined specifications. No     |
|                             |                                        |   major functionality is impacted or a workaround is in place.                       |
|                             |                                        | - *Trivial*: Minor usability issue.  No functional impact to the customer.  Includes |
|                             |                                        |   defects in documentation.                                                          |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Components                             | Select right value from pull-down list.                                              |
|                             |                                        |                                                                                      |
|                             |                                        | Component cannot be a "parent" (starts with "_" or "Unknown".                        |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Found in Versions                      | Release name: "SRxxx" or "CRxxx"                                                     |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Fix Version                            | Release name: "SRxxx" or "CRxxx"                                                     |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Steps to Reproduce                     | This field should allow any user to reproduce the defect.  It should also give a     |
|                             |                                        | quick explanation on what the expected outcome should be in contrast to the actual   |
|                             |                                        | result.                                                                              |
|                             |                                        |                                                                                      |
|                             |                                        | Make sure to not use the following:                                                  |
|                             |                                        |                                                                                      |
|                             |                                        | - Barcode                                                                            |
|                             |                                        | - Git info                                                                           |
|                             |                                        | - Repo                                                                               |
|                             |                                        | - Jenkins                                                                            |
|                             |                                        | - Spin name                                                                          |
|                             |                                        | - WASSP                                                                              |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Overview                    | Workaround                             | Fill in basic information, if a valid workaround has been identified.                |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Environment                 | Host OS                                | Fill  in this information if this is a host tool defect                              |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Environment                 | Processor Architecture                 | Fill  in this information if this is a run-time defect                               |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Publishing                  | Published Summary                      | Brief description of the issue.                                                      |
|                             |                                        |                                                                                      |
|                             |                                        | Make sure to not use the following:                                                  |
|                             |                                        |                                                                                      |
|                             |                                        | - Barcode                                                                            |
|                             |                                        | - Git info                                                                           |
|                             |                                        | - Repo                                                                               |
|                             |                                        | - Jenkins                                                                            |
|                             |                                        | - Spin name                                                                          |
|                             |                                        | - WASSP                                                                              |
|                             |                                        | - Do not reference attachments or URLs                                               |
|                             |                                        |                                                                                      |
|                             |                                        | Mandatory field if published                                                         |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
| Publishing                  | Published Description                  | Ensure description is clear and concise.                                             |
|                             |                                        | Use Specific board names.                                                            |
|                             |                                        | Describe specific device in details.                                                 |
|                             |                                        |                                                                                      |
|                             |                                        | Make sure to not use the following:                                                  |
|                             |                                        |                                                                                      |
|                             |                                        | - Barcode                                                                            |
|                             |                                        | - Git info                                                                           |
|                             |                                        | - Repo                                                                               |
|                             |                                        | - Jenkins                                                                            |
|                             |                                        | - Spin name                                                                          |
|                             |                                        | - WASSP                                                                              |
|                             |                                        | - Do not reference attachments or URLs                                               |
|                             |                                        |                                                                                      |
|                             |                                        | Mandatory field if published                                                         |
+-----------------------------+----------------------------------------+--------------------------------------------------------------------------------------+
