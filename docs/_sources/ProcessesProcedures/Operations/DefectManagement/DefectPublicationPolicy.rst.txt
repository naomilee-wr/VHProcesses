:orphan:
|
|
|

=============================
Defect Publication Policy
=============================

|

#. All defects in released products[1] are to be prepared for publication[2] within 10 days of their acknowledgment[3] or release, whichever occurs later, with the following exceptions:

   -  Publication of the defect could reasonably be expected to expose a customer, partner, or Wind River to unnecessary risk. Included under this exception are defects for which publication would:

      - Expose a problem related to a non-public security alert or other security advisory agency, or
  
      - Compromise pending litigation, or risk legal liability

   -  The quality of the information, or the nature of the defect itself, makes it unsuitable for publication, as determined by the Bug Board[4].

      - **Note**: This exception shall *not* be applied to a *customer-reported* defect.

#. The rationale for not publishing a defect must be recorded in each instance.
#. The following defect record text fields are published.

   - Published Summary
   - Published Description
   - Severity
   - Component/s
   - Fix Version
   - Steps to Reproduce
   - Workaround
   - Host OS
   - Processor Architecture
 
|

**Notes**
~~~~~~~~~~

#. Development defects fixed prior to release are not published because they never appear in a released product.
#. Customer-reported defects are prepared for publication by the Customer Support Engineer submitting the defect. Defects found by engineering are prepared for publication by the Technical Lead.
#. Defect "Open" state definition: "Engineering acknowledges that the Symptom Details provided constitute a product defect. 

   **Note:** The ability to reproduce the defect is not required: difficult-to-reproduce symptoms should be Opened.

   - An acknowledgment is not a commitment to fix the problem - it is simply feedback to the submitter that [engineering agrees] that [the symptom] described reflects a defect.

#. Customer Support may request a defect to be published.

|

**Change Log**
--------------

+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| **Date**     | **Change Request ID**   | **Version**   | **Change By**           | **Description**                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
| 05/08/2020   | N/A                     | 0.1           | Shree Vidya Jayaraman   | Initial Draft                                                                                       |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+
|              |                         |               |                         |                                                                                                     |
+--------------+-------------------------+---------------+-------------------------+-----------------------------------------------------------------------------------------------------+