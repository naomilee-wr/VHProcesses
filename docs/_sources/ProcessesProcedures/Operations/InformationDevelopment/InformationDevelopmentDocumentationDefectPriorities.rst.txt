:orphan:

|
|
|

========================== 
Jira Usage For Writers
========================== 

|
|

**Purpose**
------------

The purpose for this document is to detail defect priorities for documentation issues that arise from formal testing, and through defects created as a result of product usage. Documentation issues and defects do not always align with code-related defects, so the intent is to provide guidelines based on customer impact. The guidelines here are just that – recommendations based on typical customer impact. If at any time the defect creator feels a higher priority defect is required to meet a pending customer issue, they can use their discretion to escalate as necessary.
 
All documentation defects should take into account the defect itself along with the overall Wind River product impact. For example, an issue with a new product during a box opening may be classified with a higher priority than a defect for an existing product, because it not only impacts the product usage, but the pending product delivery. Another similar example is a defect for an older product that impacts a long-term or high visibility customer.
 
From a formal testing perspective, which typically occurs pre-release, the ability to fix the content before it is made available to a customer should be taken into consideration. Documentation should not block a release unless underlying product issues are pervasive and unresolved.

|

**Suggested Defect Priorities**
-------------------------------

The following suggestions apply to typical documentation issues: 

- **P1**: A P1 defect should rarely apply to a documentation issue, and should only be used for escalation.
- **P2**: A P2 defect represents the highest level of documentation defects for released products. This includes any defect that breaks a procedure or makes it impossible to complete it using the documentation alone. Examples include incorrect workflows, incorrect code commands, incorrect or misleading information, and structural issues preventing the completion of the procedure at-hand.
- **P3**: A P3 defect represents any documentation issue found in procedure, concepts, or reference material. This includes incorrect paths, incorrect code commands not part of an example step, out-of-date or broken cross-references, and specific relevant but missing information. if content has excessive number of broken cross-references, this would considered a higher priority due to the customer impact.  From a testing perspective, all defects prior to release should be considered a P3. The intent by Information Development is to resolve all defects prior to GA. If defects cannot be resolved, they will be escalated as necessary to match the severity of the issue after release on a case-by-case basis.
- **P4**: A P4 represents defects of minor concern, but still require fixing. This includes, but is not limited to, spelling issues, grammatical issues or inconsistencies, and so on. Spelling issues with high visibility, such as an incorrect product or feature name, or in a topic title, will have a higher priority, based on the impact.

|

**Defect Scope**
-------------------------------

Defect reporters should consider the topic to be the lowest level for maintaining a defect. For example, if a single topic includes multiple issues, they should all be defined in that single-topic defect. This approach helps reduce overhead while making defect fixes much simpler to accomplish, as all fixes are referenced in the same place. In a similar manner, if there are minor issues at the book level, combining defects into a single book-related defect is preferred, as it also helps save overhead and speed resolution.
 
There are times when a single issue impacts content across multiple topics. An example of this would be a path or command that has been updated in the product but not yet in documentation. When related defects occur in this manner, the defect creator should address the cause of the issue in a single defect, as opposed to creating separate defects for each instance. Note that it is not the overall responsibility of the defect creator to define every instance, but pointing out the issue with a sense of the overall impact helps the writer be aware and better prepared to adequately address every instance of the defect.

|

**Missing Content vs. Undocumented Content**
-------------------------------------------------

The amount and scope of documentation is typically determined at feature-creation time and agreed upon by the product development team. Some of the time, due to the amount of work or a decision to not fully include a specific feature, content is not included. This is an example of undocumented content, and is not considered a defect. If the undocumented content is a value-add, the method for getting it into the documentation is through an enhancement request (ER). The same information required to describe the defect is used to describe the need for the additional content. This approach lets product management better plan their resources.
 
When the lack of content causes confusion, or prevents a customer from being able to complete the task, it is considered a valid defect for missing content. Defects concerning missing content should be kept at the topic- or procedure-level. For example, if a topic or procedure is missing important information, such as supporting information concerning a command, or a supported BSP is not listed, this is considered a defect. If the missing content requires a new procedure, this is considered an enhancement, and requires an ER. Typically missing content is considered a P3 defect, but the defect scope and customer impact may justify escalation.
 
|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 08/18/2020   | N/A                     | 0.1           | Shree Vidya Jayaraman   | Transferred content from DOC-82727                                                                  |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+


