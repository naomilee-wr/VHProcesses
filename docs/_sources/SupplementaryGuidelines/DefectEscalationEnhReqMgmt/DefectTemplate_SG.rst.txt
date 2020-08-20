:orphan:

|
|
|

=============================================
Defect Template
=============================================

**THIS PAGE IS CURRENTLY SERVING AS A PLACEHOLDER.  IN PROGRESS for updates.**


(Source: https://jive.windriver.com/docs/DOC-51833)

**Background:**
---------------

*Why we have defect template?*

- First, help developer analysis: provide enough information at first creation, reduce ping-pong between dev/test
- Second, helpful to publish: reduce error words and provide enough information to customer.

*How the defect template is defined?*

- We try to define a common defect template for Vx7/WB4 and/or compiler.
- Publish fields (highlight in Yellow) should be filled as accurate as possible when publish.
- Some fields are defined mandatory.
- Some fields are defined mandatory.

*How Reporter fill defect information following template?*

- Because Jira is common used tool for all teams, it is not easy to update Jira system.
- So need reporter to fill information manually following template.
- Best solution should be Jira can have template (text format, make field required…)

*How can we reduce Reporter's effort in following template?*

- 1.) Proactively check defects opened and tell Reporter what are missed, like following sample.
  
  - There is one or multiple defects reported by you are not in template format.
  - Please check found problem in the following MissItems.
  - If MissItems is empty, you can ignore it.
  - You can click the following URL for details: https://jira.wrs.com:8443/issues/?jql=filter=22926 (*Note*: this url is from jive page, but returns error)
	 
.. list-table::
   :widths: 25  20  30  20  20  25  120  120
   :header-rows: 1   
   
   * - Key
     - Priority
     - Assignee
     - Reporter
     - Status
     - Resolution
     - Summary
     - Info
	    
   * - `WB4-7510 <https://jira.wrs.com/browse/WR4-7510>`__
     - P3      
     - Shen, Zhensheng (Jason)
     - Ge, Lei 
     - Open
     - None       
     - Sometimes no 'Binaries' subdir for cmake project in UI when clean project and build
     - MissItems: 
	   - Steps To Reproduce is empty 
	   - Incorrect word used in Published Description: ['SEE [A-Z ]ATTACH']
	    
   * - `V7COR-5475 <https://jira.wrs.com/browse/V7COR-5475>`__
     - P2      
     - Kong, Kitty
     - Ge, Lei 
     - Open
     - None       
     - No difference for two Vx7 Cert VSB configurations: SAFETY_CERT_ARMARCH7_CORE_SAFETY_1_0_5_0000_cert and SAFETY_CERT_ARMARCH7
     - MissItems: 
	   - Found In Versions is wrong 
	   - Labels is one of NONFT|Vx7_SR0510_Release|Vx7_SR0520_Release|F9830|F9831|F9889
	   - Reproducibility is empty
..

- 2.) If defects already entered Checked-in/Resolved status, we can skip template check.
  
  - Because we assume dev/test already reached agreement.
  - Sometimes dev opens quickly fixed/non-published defect for himself/herself.

- 3.) Some defects can be excluded: Cloned.
  
  - It is normal Cloned defect is very old and is not applicable to defect template.

**What is current defect template compliance status in Beijing?**

- Pick yesterday (May 14) Miss Template as example: 
  
  - 3 in Vx7&WB4,  ~100 engineers, ~50% are testers

**Template:**
------------------

.. list-table::
   :widths: 35  40  30  40  30  120  120 120
   :header-rows: 1

   * - Tab
     - Field   
     - Owner   
     - Mandatory When Reported
     - KL Field When Published
     - Follow
     - Avoid
     - Sample

   * - Overview
     - Summary
     - Reporter
     - Y
     - N
     - **Keywords + Failure Info + [in Specific Architecture] + [in Specific BSP]**
	 
       Keyword can be Test Configuration or Feature Name.
     -  	
     - Good Examples:
   
       - SMP: second core enable fails when testing Posix
       - IPSCTP:TAHI: SCTP doesn't send CHUNK_ERROR when recving an invalid stream identifier DATA trunk
       - Code Review: Some task stack size in test code need increased
	   
   * - Overview
     - Priority
     - Reporter
     - Y
     - N
     - P1: The issue demands immediate attention.  Someone will be assigned immediately to work on this issue.
	 
       Examples: Nightly test failures (regression introduced), defects blocking test suite execution, defects blocking a developer from developing, defects where system is down.  	
     -  	
     -   	
	 
   * - Overview
     - Severity
     - Reporter
     - Y
     - Y
     - Critical: Product is not functionally usable.  System crash or major data loss.  No workaround is available. 
     -   
     -  
	 
   * - Overview
     - Components
     - Reporter
     - Y
     - Y
     - Select right value from pull-down list. Reporter can select umbrella component or unknown if not clear. 
	 
       Developer must fill it with concrete right component if published. 
     - Don't use parent component (start with _) or unknown if published.   
     -  
	 
   * - Overview
     - Found in Release
     - Reporter
     - N
     - N
     - Recommend to input RPM version introduced the defect. 
     -   
     -  
	 
   * - Overview
     - Found in Version
     - Reporter
     - Y
     - Y
     - Select right release name where it was found from drop-down list.
	 
       FIV is filled with one value only
	   
       If FIV=FV, it shouldn’t be published.
	   
       If FIV=FV and dev think it should be published, dev need update FIV to an older release    
     -     
     - For release tests, using the release name (SR/CR/EAR). 
	 
       For feature tests on feature branch, use the release name the feature delivered to. 
	 
   * - Overview
     - Fixed in Release
     - Designer
     - N
     - N
     - Recommend to input RPM version fixed the defect.  
     -   
     -  
	 
   * - Overview
     - Fix Version
     - Developer
     - Conditional Yes
     - Y
     - If Resolution=fixed, select right release name where it is fixed from drop-down list.  
     -   
     -  
	 
   * - Overview
     - Where Found
     - Reporter
     - Y
     - N
     - Select right value of which phase the defect was found from pull-down list.  
     -     
     -   
	 
   * - Overview
     - Description
     - Reporter
     - Y
     - N
     - Describe symptom and capture details, should not be empty.

       Optional Keywords:
	   
       Expected Result:
	   
       Actual Result:
	   
       Key error log output:  
     -     
     - Target's network down after ftp access attempt while debug is on.
	 
       Expected result: ftp access to target with no errors
	 
       Actual result: ftp access target failed and causes network down
	 
       Key error log: ** Failed assertion 'pkt->end + data_len <= pkt->maxlen' at <WIND_HOME>/workbench-4/workspace/fsl_p1p2_debug/krnl/h/public/ipcom_pkt.h:1713, task name: tNet0, Id: 20007b10 **  
	 
   * - Overview
     - Steps to Reproduce
     - Reporter
     - Y
     - Y
     - This field should allow ANY user (whether they are from Wind River or not) to reproduce the defect. It should also give a quick explanation on what the expected outcome should be in contrast to what is actually obtained.  
     - <OLS Generic Guide>
	 
       “See Description” or “refer to Description” should NEVER be used  
     - 1) Create a new TWD window using the IDT
	 
       2) Add a progress meter widget
	 
       3) Add a button widget
	 
       4) Change the button's Out Fill Color to same RGB value
	 
       5) Compare the color of the meter with that of the button  
	 
   * - Overview 
     - Workaround 
     - Reporter
     - N
     - Y
     - Fills in basic workaround info if known, from the viewpoint of external customer.
	 
       Developer should be responsible for the details and accuracy before it's published, as its a OLS data. Tester need validate and see if it works for the customers.  
     - <OLS Generic Guide>
	 
       Any internal workaround, such as “download the latest version of file from CC view” is not applicable to this filed.
	   
       “See Description” or “refer to Description” should NEVER be used    
     -  
	 
   * - Overview 
     - Email CC
     -  
     - N
     - N
     - Add related stakeholder here.  
     -   
     -  
	 
   * - Overview
     - Labels
     -  
     - N
     - N
     - For defect found in new feature tests, Feature ID need to be updated as label. 
	 
       For defect found in release tests, release test label need to be added.  
	   
       Free to add more label which can help for daily works  
     -    
     - Label FR120 VxBus Gen2 improvements defects with FR120
	 
       Label Vx7 SR0510 release defects with Vx7_SR0510_Release 
	 
   * - Overview
     - In Regression?
     - Reporter
     - N
     - N
     - Choose Yes if this defect is against a feature that is delivered before current release; and it is newly found in current (N) release, but not reproduced on last (N-1) release.  
     -   
     -  
	 
   * - Overview
     - Reproducibility
     - Reporter
     - Y
     - N
     - Choose Reproducible or Intermittent or "Not Reproducible"  
     -   	  
     -  
	 
   * - Overview
     - Attachment
     -  
     - N
     - N
     - Provide all logs including Eclipse log, test code, image, console output in attachment. (VSB build fail defect: Vsb.vxconfig, vsb.config, "*.wpj" should be attached; VIP Build fail defect: "*.wpj" from vip should be attached.)  
     - Don't simply provide links to the logs here. 
	 
       Links disappear when the logs are removed or that the server where the logs are is down.
	   
       Customers can't see attachments.    
     -   
	 
   * - Overview
     - Close Only By
     -  
     - N
     - N
     - Check it when creation: it means the defect should be closed by Reporter only.  
     -   	 
     -  

   * - Environment
     - Host OS
     - Reporter
     - N
     - Y 
     - Select right value from pull-down list if host tool defect  
     -   	  
     -  
	 
   * - Environment
     - Processor Architecture
     - Reporter
     - N
     - Y
     - Select right value from pull-down list if runtime defect  
     -     
     -  
	 
   * - Environment
     - Environment
     - Reporter
     - Y
     - N
     - Optional Keywords

       SW: Spin name or GIT info
	   
       HW: Barcode or Vxsim info
	   
       Host: Host name or IP or VNC information 
     -   	  
     - Test Environment:
	 
       SW: vx20150923171206_vx7-sep2015-features_vx7-release
	   
       HW: fsl_p2020rdb(barcode:19746)
	   
       HOST: pek-ferrum(128.224.158.62) ubuntu 14.04 
	 
   * - Development
     - Tester
     -  
     - N
     - N
     - Fill with Tester name who validate it if a Fixed defect and different from Reporter.
	 
       Fill with Tester name who do RCA if a Fixed defect created by CSO.   
     -   	   
     -   
 	 
   * - Publishing (Developer's part)
     - Publish to OLS
     - Designer
     - N
     - N 
     - Select right value from pull-down list.  
     -   	  
     -  
	 
   * - Publishing (Developer's part)
     - Published Summary
     - Designer
     - Conditional Yes
     - Y
     - **Keywords + Failure Info + [in Specific Architecture] + [in Specific BSP]**  
	 
       Keyword can be Test Configuration or Feature Name.
	   
       Mandatory if Published  
     - <OLS Generic Guide>  
     - Good Examples:
   
       - SMP: second core enable fails when testing Posix
	   
       - IPSCTP:TAHI: SCTP doesn't send CHUNK_ERROR when recving an invalid stream identifier DATA trunk
	   
       - Code Review: Some task stack size in test code need increased 
	 
   * - Publishing (Developer's part)
     - Published Description
     - Designer
     - Conditional Yes
     - Y
     - Write description following OLS Generic Guide.
	 
       Mandatory if Published  
     - <OLS Generic Guide>  	  
     - Target's network down after ftp access attempt while debug is on.
	 
       Expected result: ftp access to target with no errors
	   
       Actual result: ftp access target failed and causes network down
	   
       Key error log: ** Failed assertion 'pkt->end + data_len <= pkt->maxlen' at <WIND_HOME>/workbench-4/workspace/fsl_p1p2_debug/krnl/h/public/ipcom_pkt.h:1713, task name: tNet0, Id: 20007b10 **  
	   
**OLS Data Fields Fill in Guideline:**
---------------------------------------

**To Avoid:**
++++++++++++++
- User can't see attachment or access internal links, don't use "see attachment", "see url".						
- Any customer-names, internal DVD/view names(such as “vx692xJan12.wb56A.10fa), logs, milestones, twiki URL, issues, freeze points, derogatory language, proprietary information, etc. 
- Internal info should be moved to the field "Internal Description".						
- Any reference to the platform being tested (unless the problem is SPECIFIC to that platform).						
- Any forward-looking information/data. Avoid making promises of Wind River action. Remember that a public transaction will live for many years.						
- Any improper terms like “if you..”, “we…”, “This is very serious…” which make the defect unprofessional for external sharing.						

**To Do:**
++++++++++
- Ensure description is clear, precise, descriptive. Some made-up examples:						
 
  - Be specific: Don't say "X crashes", Do say "X can crash if 3 files are edited at the same time"						
  - Don't be alarmist: Don't say "Feature X is completely broken.", Say "Feature X fails if more than 2 widgets are created."						
  - Express the problem from a user's point-of-view. Don't say "File X has a bug at line 103", say "Feature YY has a bug which causes..."						

- Use wording that will help a customer's Textual Search find your description, i.e. use words that a customer might use to describe the problem, eg. "crash", "exception", text or error codes from a particular error msg, etc.						
- Product names and version numbers should be spelled and formatted correctly						
- All Wind River Product names are capitalized except some product names have internal capitalization (such as VxWorks). Other operating system or third-party product names should be capitalized appropriately.
						
  - VxWorks should be used when discussing the product.						
  - vxWorks should be used only when discussing a specific image file.						
  - vxworks should NEVER be used.						
  -  "Wind River Linux" should be used when discussing the product.						
  - "WR Linux" or "wrlinux" should NEVER be used.						
- Spell out product names (do not use WB for Workbench, PP for Performance Profiler, and so on).						
- Move internal info or improper into to the field of "Internal Description".						

**References:**
------------------
`Submit Defect Template <http://pek-mcbuild1.wrs.com/buildarea3/VxWorksProcess/Defect/DefectSubmit/TemplateDefectSubmit.html>`__  (*Note*: Url is from jive page, but seems to be broken)


