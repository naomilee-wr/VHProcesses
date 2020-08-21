:orphan:

|
|
|

===============================================================
Managing Third Party Libraries Located in Wind River GitHub
===============================================================

|
|

**Purpose**
------------

The third party libraries we put on GitHub is “as-is” without any warranty.  For what it’s worth, we will make sure it works with the latest release only but no support or maintenance or warranty. We will add a specific Git tag to each project after each release verification. This can help the customer to know the mapping between GitHub codes and Vx7 releases. Customers will be able to download the specific content based on the “Vx-SR0XX" tags. This process document is to describe how and when we apply tags.

|

**Guideline**
--------------

#. After the successful testing of a VxWorks release, testing team will create an annotated tag on the master branch, for example, “Vx7-SR0540” and/or “Vx7-SR0600”.

#. If the testing for a specific release failed, there will be no tag created. Defect(s) will be created instead. When all the defects have been fixed and pushed to GitHub, go to step 1.

#. To save the additional testing effort, we will only retrospect to SR0540 or the last successfully tested release if it was not SR0540.

|

**SR0540 Example**
---------------------

We are going to add tag "Vx7-SR0540" to the following GitHub projects with note "Verified with VxWorks 7 - SR0540".

Since there is no code change, there is no need for IP review.

- `VxWorks 7 Recipe Layer for iPerf3 (GitHub) <https://github.com/Wind-River/vxworks7-layer-for-iperf>`__

- `VxWorks 7 Recipe Layer for OpenAMP (GitHub) <https://github.com/Wind-River/wr-MultiOS-OpenAMP>`__

- `VxWorks 7 Client for IBM Bluemix Platform (GitHub) <https://github.com/Wind-River/vxworks7-client-for-bluemix>`__

- `VxWorks 7 Client for AWS IoT Devise SDK (GitHub) <https://github.com/Wind-River/vxworks7-client-for-aws>`__

|

**Change Log**
--------------
+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/10/2020     | N/A            | 0.1            | Naomi Lee      | Transferred content from DOC-72724    |
|                |                |                |                | Jive page                             |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
