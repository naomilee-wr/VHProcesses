:orphan:
|
|
|

============================================
Prepare Defect for Publication Procedure
============================================

|
<EPMs to discuss this policy with Dev & CSO>
Decide if defect is suitable to be published; record the decision, and if it is to be published, prepare and review the published information.  Customer-reported defects are published at submission by the Customer Support Engineer submitting the defect. Defects found by engineering are published by the Technical Lead.

Which defects must be published and how quickly is defined in the `Defect Publication Policy <./DefectPublicationPolicy.html>`__.

|

+--------------------------------------+--------------------------------------+
| **Entry Criteria**                   | -  A defect is in a product released |
|                                      |    to customers. The defect may be   |
|                                      |    reported by a customer, or found  |
|                                      |    during development and not fixed  |
|                                      |    before the product was released.  |
+--------------------------------------+--------------------------------------+
| **Inputs**                           | -  Defect record has *Publish to     |
|                                      |    OLS* field set to "To be          |
|                                      |    determined" or "Ready for Review" |
+--------------------------------------+--------------------------------------+
| **Exit Criteria**                    | -  Customer Support and Development  |
|                                      |    reported defects are published at |
|                                      |    the appropriate time and marked   |
|                                      |    as "Reviewed - Publish" or        |
|                                      |    "Reviewed - Publish pending       |
|                                      |    release" and has Publication      |
|                                      |    Hierarchy set                     |
|                                      | -  Defects not published             |
|                                      |    are marked as "Reviewed - Do NOT  |
|                                      |    Publish" and the reason for not   |
|                                      |    publishing is explained in the    |
|                                      |    *Comments*                        |
|                                      | -  Defects not affecting customers   |
|                                      |    are marked as "Never shipped to   |
|                                      |    customer"                         |
+--------------------------------------+--------------------------------------+
| **Outputs**                          | -  Defect record is updated with     |
|                                      |    *Publish to OLS* field updated    |
|                                      | -  Defect is updated on WR Support   |
|                                      |    Network (WRSN)                    |
+--------------------------------------+--------------------------------------+

|

**Steps**
---------

#. **Review defects with the** *Publish To OLS* **field set to "None, "To be determined" or "Ready for Review**"
#. **Change the** *Publish To OLS* **field to "Reviewed - Publish pending release", "Reviewed - Publish", "Reviewed - Do NOT publish" or "Never shipped to customer". Refer to the criteria for publication in the** `Defect Publication Policy <./DefectPublicationPolicy.html>`__.
#. **For defects to be published:**

   -  Set the information to be published:  *Published Summary, Published Description,* and *Publication Hierarchy*. See Appendices B and C.
   -  Review the information to be published:  *Severity, Component/s, FIx Version, Steps to Reproduce, Workaround, Host OS,* and *Processor Architecture*
   -  Update the published fields as necessary
   -  Set *Publish to OLS* as "Reviewed - Publish pending release" or "Reviewed - Publish"
   -  Click on *Update* to save the record

#. **For defects not to be published:**

   -  Set the *Publish to OLS* field to "Reviewed - DO NOT Publish".  Add a comment to explain why the defect report will not be published.

#. **For defects that do not affect customers:**

   -  Defects which do not affect customers (not in a released version or fixed prior to release) should be marked as "Never shipped to customer"

#. **When the Criteria for Publication in Appendix A are met, the defect record will be automatically published.** How a defect can become unpublished again is described in "Removing a Published Defect" in the Variations section below.

|

**Variations**
--------------

**Modifying a Published Defect**

Any changes made to a published defect will automatically update to WR Support Network (WRSN) without going through again through the review process.  Modification to OLS published fields should be checked for accuracy before saving any changes.      

The following fields are published to WR Support Network (WRSN):

-  Published Summary
-  Published Description
-  Severity
-  Component/s
-  Fix Version
-  Steps to Reproduce
-  Work Around
-  Host OS
-  Processor Architecture

If the changes to the published fields are significant, the defect should be submitted for review by setting the *Publish to OLS* field to "Ready for Review", which will cause the defect to be removed from WR Support Network (WRSN) until it has been reviewed.

**Removing a Published Defect**

A published defect is removed from WR Support Network (WRSN) if any one of the following is true:

-  The *Publish To OLS* field is NOT set to "Reviewed - Publish"
-  The *Issue Type* is reclassified as "Enhancement Request"
-  The *Publication Hierarchy* does not have at least 2 levels.

|

**Appendices**
--------------

**Appendix A - Criteria for Publication**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

All of the following conditions must be met for a defect to be published on WR Support Network (WRSN). When these criteria are met, the defect is automatically published.

-  The *Issue Type* = Bug
-  *Publish To OLS* = Reviewed - Publish
-  The Publication Hierarchy has at least 2 levels
-  Status and resolution matches one of the following combinations:

+------------------------------+---------------+
| **Status**                   | **Resolution**|
+------------------------------+---------------+
| On Hold  and                 | None          |
| On Hold Disposition = Backlog|               |
+------------------------------+---------------+
| In Progress                  | None          |
+------------------------------+---------------+
| Checked In                   | None          |
+------------------------------+---------------+
| Resolved                     | Fixed or      |
|                              | Won't Fix     |
+------------------------------+---------------+
| Closed                       | Fixed or      |
|                              | Won't Fix     |
+------------------------------+---------------+

See Jira FAQ for more information:

- `Jira FAQ: Jive Link <https://jive.windriver.com/docs/DOC-22124#jive_content_id_What_records_are_published_to_Knowledge_Library_from_Jira>`__
- `Jira FAQ: Sharepoint Link <https://windriversystems.sharepoint.com/sites/CSO-Ops/Shared%20Documents/SCP/SCP%202020/7.09%20Service%20Request%20Resolution%20Process/JIRA_FAQ.pdf>`__

**Appendix B - Published Summary and Published Descriptions**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The **Published Summary** becomes the **Title** of the defect when it appears on WR Support Network (WRSN).

-  The goal is to provide a clear description of the symptoms resulting from the defect so that customers searching through published defects can quickly determine whether they are seeing this defect in their system or project

The **Published Description** becomes the **Description** of the problem on WR Support Network (WRSN).

-  Provide a clear description of problem with additional detail around symptoms and how the problem was fixed
-  If applicable, an indication that a workaround is available.

   -  If this is the case, the workaround must be documented in the *Workaround* field.

-  If the defect is not to be fixed then the reason why this determination has been made must be documented.
-  Patch availability or information indicating the release version the defect was fixed in (not internal code names, but actual release versions)

The **Workaround** remains the **Workaround** field on WR Support Network (WRSN)

-  If a Workaround is found for the problem exists, then a Workaround description should be created and published.
-  Any published Workaround should be broadly applicable and must be tested by engineering.

**Appendix C - Style Guidelines**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Published fields must be reviewed and sanitized. In particular:

-  All references to specific customers must be removed
-  Any embarrassing, offensive or derogatory language must be removed
-  Avoid forward-looking information/data. Avoid making promises of Wind River action. Remember that a public transaction will live for many years.
-  Convey sufficient and useful information. The key here is to avoid the call into the Call Center. The Published Description should be complete enough for the customer to determine if the issue affects them. By all means, avoid dangling a juicy tidbit that prompts frantic calls into the Call Center. It is perfectly acceptable to put test cases in a public transaction if that helps convey the information.

-  Product names should be spelled and formatted correctly.

   -  All product names are capitalized.
   -  Some product names have internal capitalization (such as
      ScopeTools).
   -  Spell out product names (do not use WB for Workbench, PS for
      ProfileScope, and so on).
   -  When discussing our target OS:

      -  "Wind River Linux" should be used when discussing the product.
      -  "Wind River Linux #.#(.#.#)" should be used only when discussing a specific image file.  For example:  Wind River Linux 8.0 for major release or Wind River 8.0.0.2 for RCPL2.
      -  "WR Linux" should never be used.

   -  Linux, Windows, and other operating system or third-party product names should be capitalized appropriately.

-  All fields should contain complete sentences whenever possible. They should begin with capital letters and end with periods.
-  The *Steps To Reproduce* field should contain numbered steps. Each step should be a complete sentence whenever possible.
-  The published bug description must NEVER include project names, CCM/PS references, references to older WR products and/or discussions explaining that we made a mistake in a port.
-  The description should be re-written to explain the component that is broken and the symptoms of the failure.   All other details should be  removed unless relevant to the external reader.
-  The Subject from cloned defects includes the word 'cloned', which should be removed.
-  Customers will not see the *Internal Description* or *Comment* fields. Use these fields for any mention of attached logs or screenshots, host/target configuration information, specific tests run, or any other internal Wind River information.

|

**References (not created/maintained by Engineering)**
--------------------------------------------------------
- `Tools Group Defect Publication Criteria <https://jive.windriver.com/docs/DOC-75001>`__
- `Posting Jira Defects for Publication <https://jive.windriver.com/docs/DOC-74237>`__
- `Defect Publication Guidelines <https://jive.windriver.com/docs/DOC-49197>`__

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 08/07/2020   | N/A                     | 0.2           | Shree Vidya Jayaraman   | Updates based on Rodger's feedback                                                                  |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+