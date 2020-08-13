:orphan:

====================================================
CVE Tracking and Third Party Library Upgrade Process
====================================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**

This page documents the process & guidelines of VxWorks 7 CVE monitoring and the related 3rd party libraries upgrade.

(Source: https://jive.windriver.com/docs/DOC-79998)

|

**Guideline of CVE tracking**
-------------------------------

Wind River commits to take the actions on CVE following the Security Vulnerability Response policy (policy link in the useful links paragraph). For VxWorks7, the general workflow is as following for CVE tracking: 

#. Engineering (CVE contact) to monitor new CVEs from NIST on monthly basis;

#. Engineering (domain/library owner) to assess security impact, update WR CMS database AND CVE components tracker where required;

#. PM to create EPIC per CVE affected library upgrade per release based on engineering update from CVE components tracker; (Details of library upgrade can be found in the following paragraph.)

#. Engineering (domain/library owner) to update WR CMS database and the CVE components tracker again when the work is done.

**Guideline of CVE tracking**
-------------------------------
The general proposed guideline is to upgrade all 3rd party libraries with CVE fix in the coming release. Exceptional cases are allowed if the upgrade takes huge efforts or is disruptive after discussing with PM. For libraries without CVE fix, the upgrade is also encouraged especially when the upgrade is not disruptive and efforts are minor. All such upgrade should be tracked by EPICs which are categorized as PM features or sponsor as Product Management in Jira. Details are as following:

#. For 3rd party libraries with CVE fix impacting VxWorks latest version, PM should create one EPIC per 3rd party library and request the fix in the coming release.

#. For 3rd party libraries without CVE fix impacting VxWorks latest version, engineering team can create the EPIC directly based on bandwidth if the efforts are minor (less than 2 person weeks) and not disruptive. Such works should not impact normal feature commitments. One EPIC per library is needed. PM can defer or reject the request if any concerns.  

#. 3rd party library upgrade with big efforts or customers impacts are handled by PM based on business value. 

#. All 3rd party library upgrade EPIC of one release should be created and reviewed by POR with updates on CVE component sheet also. Then, these EPICs will follow normal feature process. Otherwise, normal PCR process is needed.

**How to Documents:**
----------------------

- `How to update Wind River CVE database for VxWorks <https://jive.windriver.com/docs/DOC-80265>`__

- `How to publish security notice for VxWorks <https://jive.windriver.com/docs/DOC-80266>`__

- `How to create RSS feeds <https://jive.windriver.com/docs/DOC-80267>`__

**Useful Links:**
-----------------
- `Vx7 CVE component tracking sheet <https://jive.windriver.com/docs/DOC-80227>`__

- `Security Vulnerability Process <https://jive.windriver.com/docs/DOC-42354>`__ (2016-02.07.pptx)

- `uHLD 1600 <http://wiki.wrs.com/PBUeng/MicroHld1600>`__

- `uHLD 1601 <http://wiki.wrs.com/PBUeng/MicroHld1601>`__

- `VxWorks 7 SDL <https://jive.windriver.com/docs/DOC-76246>`__

- `Security Vulnerability Response Policy of Wind River <https://support2.windriver.com/docs/Security_Vulnerability_Response_Policy_doc.pdf>`__  
 