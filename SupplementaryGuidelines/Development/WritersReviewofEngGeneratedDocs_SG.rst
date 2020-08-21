:orphan:

|
|
|

=======================================================
Writers Review of Engineering Generated Documents
=======================================================

|
|

**Purpose**
-------------

When code comments and other code-based documentation are consistent with the Wind River writing standard used for our product guides, we ensure that our customers perceive our products as having a high quality, suitable for safe and secure deployments. Clear, consistent communication in all aspects of documentation reduces confusion and ensures customer success without the costly support calls.  

**All customer-facing documentation created by development must be reviewed by a Writer before release**. The review should be done as part of the normal development process using the same tools used for technical review of code. For example:

- Add a Writer to the code collaborator review of a new customer API.
- Add a Writer to the email distribution list for any README.txt review.


A Lead Writer for each technology line is available. If they are busy, or the technology is better understood by someone else, they will defer the request to another Writer.

+--------------------------------+-------------------------------------------------------------------+------------------------------------------------------------------------+
|          **Program**           |                     **Lead Writer/Reviewer**                      |                     **Expected Review Content**                        |
+--------------------------------+-------------------------------------------------------------------+------------------------------------------------------------------------+
| VxWorks                        |`Shoba Tumma <https://jive.windriver.com/people/stumma>`__         | comment blocks of new published APIs, new visible CDF components, new  |
|                                |                                                                   | layers.vsbl, customer visible*.vxconfig additions, target.ref updates, |
|                                |                                                                   | and anynon-DEBUG output to the console via printf(), logMsg(),         |
|                                |                                                                   | printErr(), and printExc(), and so forth.                              |            
+--------------------------------+-------------------------------------------------------------------+------------------------------------------------------------------------+
| Linux                          |`Mark Morton <https://jive.windriver.com/people/mmorton>`__        | layer readme.txt files                                                 |
+--------------------------------+-------------------------------------------------------------------+------------------------------------------------------------------------+
| Helix Device Cloud             |`Julia Keffer <https://jive.windriver.com/people/JKeffer>`__       | REST APIs, agent API references                                        |
+--------------------------------+-------------------------------------------------------------------+------------------------------------------------------------------------+
| TiServer                       |`Juanita Balraj <https://jive.windriver.com/people/JBalraj>`__     | REST APIs, in-product text documents                                   |
+--------------------------------+-------------------------------------------------------------------+------------------------------------------------------------------------+
| VxWorks 653                    |`Rod Nickel <https://jive.windriver.com/people/RNickel>`__         | comment blocks of new published APIs, new visible CDF components, new  |
|                                |                                                                   | layers.vsbl, customer visible*.vxconfig additions, XML references,     |
|                                |                                                                   | target.ref updates, and any non-DEBUG output to the console via        |
|                                |                                                                   | printf(), logMsg(), printErr(), and printExc(), and so forth.          |
+--------------------------------+-------------------------------------------------------------------+------------------------------------------------------------------------+

|

**Scope**
---------

    Only **new** engineering content. Existing engineering content needing review can be noted in a JIRA enhancement or defect. Reviewing existing content can be scheduled as a separate feature or user story in the normal Agile process used by the program.
    Only customer facing documentation, internal documents requiring review require a separate commitment from the documentation manager and may be done on an as-available basis.
    In conjunction with the engineering review, the Writer(s) will use the normal review tools of the program and make their comments at the same time in the review cycle as the technical review.
    The Writer **will review, not write**. If the required textual content is incomplete or misleading, the Writer will indicate this as a bug in the review tool to be resolved by the developer in consultation with other engineers. The Writer will **not research** the technology in order to provide incomplete or missing text.

|

**Change Log**
--------------
+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/19/2020     | N/A            | 0.1            | Shree Vidya    | Transferred content from DOC-53016    |
|                |                |                | Jayaraman      |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+

