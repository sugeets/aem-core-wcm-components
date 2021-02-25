
Phase-1.x East Coast Go-Live - EDAM Deployment/Rollback Steps for UAT
=====================================================================

*   [1\. Take Snapshot of East Coast EDAM Server VM:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [2\. Remove  ui.apps.uat.config :](#Phase1.xEastCoastGoLiveEDAMDeployment/R) 
*   [3.Remove ui.uat.acls :](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [4\. Stop AEM Server:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [5\. Change run-mode from edam-we to edam-east and install ICC profile:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [6\. Start AEM Server:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [7\. EDAM config - common:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [8\. EDAM config - Environment:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [9\. EDAM Config - oak index:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)

*   [10\. EDAM Config - ACLs:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [11\. EDAM App code :](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [12\. EDAM AEM Restart:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [13\. Reinstall AEM ACS Commons:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [14\. one time script execution to update permissions for existing content:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [15\. Post-Deployment Steps:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [Validation Check list: EDAM 1.x - East - Validation Checklist](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*    [Jenkins and RunDeck Jobs](#Phase1.xEastCoastGoLiveEDAMDeployment/R)

·  [Rollback Steps :](#Phase1.xEastCoastGoLiveEDAMDeployment/R)


*   [install ui.apps.uat.config:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)

*   [Reinstall edam.ui.apps-<version>.zip:](#Phase1.xEastCoastGoLiveEDAMDeployment/R)

*   [edam.ui.apps](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [ui.oak.index](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [ui.apps.common.config](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [ui.rep.namespaces](#Phase1.xEastCoastGoLiveEDAMDeployment/R)
*   [ui.system.user](#Phase1.xEastCoastGoLiveEDAMDeployment/R)

**1\. Take Snapshot of East Coast EDAM Server VM:**
---------------------------------------------------

Project team to raise a WSI SNOW ticket to take a snapshot of East coast server VM before deployment begins.

  **For Server details please refer the following URL:****  
**[EDAM - CNAME](/display/PS/EDAM+-+CNAME)****

**2\. Remove  ui.apps.uat.config :** 
-------------------------------------

**Source**  
**UAT** : **[https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/we/ui-apps-config/edam-we](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-west)**  
**UAT Destination**: **/apps/edam/config.edam-we.uat**  
This step uninstalls ui.apps.uat.config for EDAM

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced)
2.  Select Coast 'east' 
3.  Select 'ui.apps.uat.config' from drop down for project/type
4.  Provide version :'1.0.5'
5.  Enter admin password
6.  Click 'Run Job Now' button
7.  Verify logs and wait until job get finished 
8.  It takes ~ 2 min
9.  Enter URL, on the browser:
10.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/de/index.jsp
11.  Navigate to following folder /apps/edam/config.edam-east.rgs and delete config.edam.east.rgs\[This is the one manual step here, only required for the first time\]
12.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/[crx/packmgr/index.jsp](https://rundeck.wsgc.com/rundeck/project/wsgc/jobs/deploy/uat/edam/primary)
13.  Verify in the package manger ui.apps.uat.config-1.0.5.zip should not be there. 
14.  Goto /crx/de, navigate /apps/edam and under that config.edam-we.uat, it should be removed

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-24_1-19-26.png?version=1&modificationDate=1614109685677&api=v2)

**3.Remove ui.uat.acls :**
--------------------------

**Source** **UAT**:  
**WE: [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/we/ui-acls](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-west)**  
**Destination**: **/home/groups**  
This step uninstalls required ACLs for EDAM

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced)
3.  Select coast=“east”
4.  Provide version :‘1.0.4’
5.  Select ‘[ui.uat.](http://ui.uat.mg).acls’ from drop down for project
6.  Enter admin password
7.  Click ‘Run Job Now’ button
8.  Verify logs and wait until job get finished 
9.  It takes ~ 10 min
10.  Enter the following URL based on the environment on the browser
11.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/useradmin
12.  search for APR, you won't see any groups related to APR.

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-24_12-43-54.png?version=1&modificationDate=1614150754040&api=v2)

**4\. Stop AEM Server:**
------------------------

**Source: [https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/stop](https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/start)**  
This step stop the AEM server

Rundeck Job URL:  
UAT : [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/c896c5ea-8736-46cf-bb03-77265dd16316](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/c896c5ea-8736-46cf-bb03-77265dd16316)

1.  Go to Rundeck job:
2.  Select 'coast:east'
3.  Click 'Run Job Now' button
4.  Verify logs and wait until job get finished 
5.  It takes ~5 min
6.  Verify by entering following  URL  on the browser.
7.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com):4501/

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-19_2-54-21.png?version=1&modificationDate=1613683381030&api=v2)

**5\. Change run-mode from edam-we to edam-east and install ICC profile:**
--------------------------------------------------------------------------

**\[It's Deploying rpm package\]**

**Source : [https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/tree](https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/tree/master/src/main/resources/sys/etc/imageMagick)**

**[https://github.wsgc.com/eCommerce-DevOps/aem-edam-uat-config](https://github.wsgc.com/eCommerce-DevOps/aem-edam-uat-config)**

**Destination for ICC Profile: /etc/Imagemagick-6/[sRGB2014.icc](https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam/blob/release/ui.apps/src/main/content/jcr_root/etc/edam/ImageMagick/profiles/sRGB2014.icc)**

This step includes to update run mode and install ICC profiles

**Rundeck job URL:**

**UAT :[https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/abc01b93-15ed-4890-ae56-76539b9e4930](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/abc01b93-15ed-4890-ae56-76539b9e4930)**

Steps to follow : A rundeck job to be triggered for this step.

1.  Go to Rundeck job: 
2.  Select Coast : we
3.  env: 'uat1'
4.  Click 'Run Job Now'
5.  Verify logs and wait until job get finished 
6.  It takes ~5 min

**![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-19_2-49-13.png?version=1&modificationDate=1613683072920&api=v2)**

**6\. Start AEM Server:**
-------------------------

**Source: [https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/start](https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/start)**  
This step starts the AEM server in primary mode

1.  Go to Rundeck job:
2.  Select 'coast:east'
3.  Click 'Run Job Now' button
4.  Verify logs and wait until job get finished 
5.  It takes ~10 min
6.  Verify by entering following  URL  on the browser.
7.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com):4501/

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_12-51-44.png?version=1&modificationDate=1613683800570&api=v2)

**7\. EDAM config - common:**
-----------------------------

This step installs required common  config for EDAM  
**Source** : **[https://github.wsgc.com/eCommerce-DevOps/edam-common-config](https://github.wsgc.com/eCommerce-DevOps/edam-common-config)**  
**Destination**: **/apps/edam/config**

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
2.  Select Coast : 'east'
3.  Select 'ui.apps.common.config' from drop down for project/type
4.  Provide version Eg:  '1.0.2'
5.  Enter AEM admin password
6.  Click 'Run Job Now' button
7.  Verify logs and wait until job get finished 
8.  It takes ~ 2 min
9.  Enter URL  on the browser, enter admin credentials
10.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/[crx/packmgr/index.jsp](https://rundeck.wsgc.com/rundeck/project/wsgc/jobs/deploy/uat/edam/primary)
11.  Verify the installed version for config, it should show version eg: '1.0.2' (ui.apps.common.config-1.0.2.zip)
12.  Goto /crx/de, it should enable the crx/de to explore
13.  open /apps/edam/config, it should show the config files 

**![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_14-38-40.png?version=1&modificationDate=1613687921030&api=v2)**

**8\. EDAM config - Environment:**
----------------------------------

This step installs required environment specific config for EDAM

**Source**  
**UAT** : **[https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-east](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-west)**  
**UAT Destination**: **/apps/edam/config.edam-east.uat**  
This step installs required environment specific config for EDAM

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
2.  Select Coast 'east' 
3.  Select 'ui.uat.east.apps.config.uat' from drop down for project/type
4.  Provide version Eg:  '1.0.10'
5.  Enter admin password
6.  Click 'Run Job Now' button
7.  Verify logs and wait until job get finished 
8.  It takes ~ 2 min
9.  Enter URL, on the browser:
10.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/[crx/packmgr/index.jsp](https://rundeck.wsgc.com/rundeck/project/wsgc/jobs/deploy/uat/edam/primary)
11.  Verify the installed version for config, it should show version eg: '1.0.10' , ui.uat.east.apps.config-1.0.9.zip
12.  Goto /crx/de, open /apps/edam/config.edam-east.uat, it should show the config files 

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_14-41-10.png?version=1&modificationDate=1613688070770&api=v2)

**9\. EDAM Config - oak index:**
--------------------------------

**Source** : **[https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/oak-index](https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/oak-index)**  
**Destination**: **/oak:index/edam-freeTextSearchIndex**  
This step installs required oak indexes for EDAM

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
2.  Select coast ‘east’
3.  Select ‘oak-index’ from drop down for project
4.  Provide version Eg: ‘1.0.2’
5.  Enter admin password
6.  Click ‘Run Job Now’ button
7.  Verify logs and wait until job get finished 
8.  It takes ~1 min
9.  Enter following URLs on the browser
10.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
11.  Verify the installed version for oak-index, it should show version Eg:  ‘1.0.2’ (ui.oak.index-1.0.2.zip)
12.  Goto crx/de, navigate to the following path /oak:index/edam-freeTextSearchIndex/indexRules
13.  You should see the custom indexes

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_14-44-24.png?version=1&modificationDate=1613688264373&api=v2)
---------------------------------------------------------------------------------------------

**10\. EDAM Config - ACLs:**
----------------------------

**Source** **UAT**:  
**MG : [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-east/mg](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/pb)**  
**RJ: [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-east/rj](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/ws)****  
**WE: [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-east/we](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/ws)****  
**Destination**: **/home/groups**  
This step installs required ACLs for EDAM

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
3.  Select coast=“east”
4.  Provide version Eg:‘1.0.9’
5.  Select ‘ui.uat.mg.acls’ from drop down for project type **MG,** select ‘[ui.uat.rj](http://ui.uat.ws/).acls’ from drop down for project type **RJ,** select ‘[ui.uat.rj](http://ui.uat.ws/).acls’ from drop down for project type **WE**
6.  Enter admin password
7.  Click ‘Run Job Now’ button
8.  Verify logs and wait until job get finished 
9.  It takes ~ 10 min
10.  Enter the following URL based on the environment on the browser
11.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
12.  Verify the installed version for ui.uat.mg.acls-1.0.9.zip  for **MG ,** [ui.uat.rj](http://ui.uat.ws).acls-1.0.0.zip for **RJ and** [ui.uat.we](http://ui.uat.ws).acls-1.0.0.zip for **WE**

**MG****![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_14-48-43.png?version=1&modificationDate=1613688523747&api=v2)**

**RJ****![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_14-49-30.png?version=1&modificationDate=1613688570840&api=v2)**

**WE****![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_14-50-14.png?version=1&modificationDate=1613688614680&api=v2)**

**11\. EDAM App code :**
------------------------

**Source** : **[https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam](https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam)**  
**Destination**: **/crx/packmgr/index.jsp**  
**This step installs required App code - EDAM**

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Deploy-Edam-Uat-Code](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Deploy-Edam-Uat-Code)
2.  Select coast: east
3.  Provide version Eg: ‘1.0.16’
4.  Enter admin password
5.  Click ‘Run Job Now’ button
6.  Verify logs and wait until job get finished 
7.  It takes ~ 3 min
8.  Enter the followig URL based on the environment on the browser
9.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
10.  Verify the installed version for config, it should show version Eg: ‘1.0.16’

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_14-53-43.png?version=1&modificationDate=1613688823477&api=v2)

**12\. EDAM AEM Restart:**
--------------------------

**This step restarts AEM** 

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Restart-Uat-Aem-Service](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Restart-Uat-Aem-Service)
3.  Select coast :“east”
4.  Click ‘Run Job Now’ button
5.  Verify logs and wait until job get finished 
6.  It takes ~ 10 min
7.  Enter URL the following URL based on the environment on the browser
8.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-19_3-38-2.png?version=1&modificationDate=1613686001907&api=v2)

**13\. Reinstall AEM ACS Commons:**
-----------------------------------

This step reinstalls required AEM ACS Commons on the existing AEM version

1.  Navigate  to [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
2.  Login with Admin credentials
3.  Search for "acs-aem-commons-content"  package manager and click on reinstall

Note: Please refer the following JIRA for RCA : [RM-23510](https://jira.wsgc.com/browse/RM-23510) - Getting issue details... STATUS

**14\. one time script execution to update permissions for existing content:**
------------------------------------------------------------------------------

**Source: [https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam/blob/release/core/src/main/java/com/wsgc/ecommerce/edam/core/servlets/UpdateOlderAssetsAclsServlet.java](https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam/blob/release/core/src/main/java/com/wsgc/ecommerce/edam/core/servlets/UpdateOlderAssetsAclsServlet.java)**

**Destination: /content/dam/west-elm**

Rundeck Job URL: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/7ff7ed86-28e3-4e3a-b311-ae09993d010a](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/7ff7ed86-28e3-4e3a-b311-ae09993d010a)

Steps to follow to execute the job:

Step 1:  Select the coast="east"

Step 2: provide the password

Step 3: Select the operation as "add"

Step 4: enter the path as "/content/dam/west-elm"

Step5: click the rundeck job

Step 6: Once the job run successfully login as either general user or merchant user, you have to see all the images irrespective of their status(like approved, killed, selected)

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-23_16-39-0.png?version=1&modificationDate=1614078460370&api=v2)

**Note : Please refer following JIRA more details:** **[RM-23552](https://jira.wsgc.com/browse/RM-23552) -** **Getting issue details...** **STATUS**

**15\. Post-Deployment Steps:**
-------------------------------

<div>

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" style="border-collapse: collapse; border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: initial; border-right-style: none; border-right-width: initial; border-bottom-color: initial; border-bottom-style: none; border-bottom-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial;">
 <colgroup><col style="width: 53px;"><col style="width: 78px;"><col style="width: 382px;"></colgroup>
 <tbody><tr>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal" align="center" style="text-align: center;"><b>S.No</b></p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal" align="center" style="text-align: center;"><b>Jira-id</b></p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal" align="center" style="text-align: center;"><b>Post Deployment
  Steps</b></p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">1</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">TRISUL-7</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">Detailed steps here - <a href="/display/PdM/Configure+SAML+Integration+on+EDAM+AEM+Environments">Configure
  SAML Integration on EDAM AEM Environments</a></p>
  </td>
 </tr>
</tbody></table>

</div>

**Validation Check list**: [EDAM 1.x - East - Validation Checklist](/display/PdM/EDAM+1.x+-+East+-+Validation+Checklist)
------------------------------------------------------------------------------------------------------------------------

 **Jenkins and RunDeck Jobs**
-----------------------------

*   [RunDeck: Install EDAM Common code](https://rundeck.wsgc.com/rundeck/project/wsgc/job/edit/install-edam-qa-common)
*   [Jenkins: Install EDAM Common code](https://ecombuild.wsgc.com/jenkins/job/install-edam-common/)
*   [RunDeck: Install EDAM code](https://ecombuild.wsgc.com/jenkins/job/deploy-edam-code/)
*   [Jenkins: Install EDAM code](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-qa-edam-code)
*   [RunDeck: Install EDAM Custom Config](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-qa-edam-custom-config)
*   [Jenkins: Install EDAM Custom Config](https://ecombuild.wsgc.com/jenkins/job/deploy-edam-custom-config/)

**Rollback Steps :**
====================

**As part of the rollback we are providing two option1, if by any chance option 1 fails then please use option 2.**

**Option 1** :

**Note : For the rollback please follow the below steps in the same order :**

**One time script execution to update permissions for existing content :**

**Source: [https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam/blob/release/core/src/main/java/com/wsgc/ecommerce/edam/core/servlets/UpdateOlderAssetsAclsServlet.java](https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam/blob/release/core/src/main/java/com/wsgc/ecommerce/edam/core/servlets/UpdateOlderAssetsAclsServlet.java)**

**Destination: /content/dam/west-elm**

Rundeck Job URL: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/7ff7ed86-28e3-4e3a-b311-ae09993d010a](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/7ff7ed86-28e3-4e3a-b311-ae09993d010a)

Steps to follow to execute the job:

Step 1:  Select the coast="east"

Step 2: provide the password

Step 3: Select the operation as remove

Step 4: enter the path as '/content/dam/west-elm'

Step5: click the rundeck job

Step 6: Once the job run successfully login as either general user or merchant user, you won't  see all the images irrespective of their status(like approved, killed, selected)

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-23_12-18-28.png?version=1&modificationDate=1614062826870&api=v2)

**EDAM App code :**

**Source** : **[https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam](https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam)**  
**Destination**: **/crx/packmgr/index.jsp**  
**This step uninstalls required App code - EDAM**

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced)
2.  Select coast: east
3.  Select the project as edam.ui.apps
4.  Provide version Eg: ‘1.0.16’ ,  this should be the latest release version that has been deployed in the instance
5.  Enter admin password
6.  Click ‘Run Job Now’ button
7.  Verify logs and wait until job get finished 
8.  It takes ~ 3 min
9.  Enter the followig URL based on the environment on the browser
10.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
11.  Verify the installed version for config, it should show version Eg: ‘1.0.15’ which should be a old version

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-23_12-52-23.png?version=1&modificationDate=1614064862247&api=v2)

**EDAM Config - ACLs**

**Source** **UAT**:  
**MG : [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-east/mg](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/pb)**  
**RJ: [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-east/rj](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/ws)****  
**WE: [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-east/we](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/ws)****  
**Destination**: **/home/groups**  
This step uninstalls required ACLs for EDAM

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced)
3.  Select coast=“east”
4.  Provide version Eg:‘1.0.9’
5.  Select ‘[ui.uat.we](http://ui.uat.mg).acls’ from drop down for project type **WE,** select ‘[ui.uat.rj](http://ui.uat.ws/).acls’ from drop down for project type **RJ,** select ‘[ui.uat.mg](http://ui.uat.ws/).acls’ from drop down for project type **MG \[For these ACLs, please follow the same order that mentioned in the step\]**
6.  Enter admin password
7.  Click ‘Run Job Now’ button
8.  Verify logs and wait until job get finished 
9.  It takes ~ 10 min
10.  Enter the following URL based on the environment on the browser
11.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
12.  Verify the installed version for  [ui.uat.we](http://ui.uat.ws).acls-1.0.8.zip for **WE** and for MG and RJ we won't see any packages, since we are doing this first time, so we won't see the packages.

 **MG****![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-23_13-5-33.png?version=1&modificationDate=1614065652693&api=v2)**

**RJ****![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_14-49-30.png?version=1&modificationDate=1613688570840&api=v2)**

**WE****![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-23_13-14-3.png?version=1&modificationDate=1614066161907&api=v2)**

**EDAM Config - oak index**

**Source** : **[https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/oak-index](https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/oak-index)**  
**Destination**: **/oak:index/edam-freeTextSearchIndex**  
This step uninstalls required oak indexes for EDAM

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced)
2.  Select coast ‘east’
3.  Select ‘oak-index’ from drop down for project
4.  Provide version Eg: ‘1.0.2’
5.  Enter admin password
6.  Click ‘Run Job Now’ button
7.  Verify logs and wait until job get finished 
8.  It takes ~1 min
9.  Enter following URLs on the browser
10.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
11.  Verify the installed version for oak-index, it should show version Eg:  ‘1.0.1’ (ui.oak.index-1.0.2.zip)
12.  Goto crx/de, navigate to the following path /oak:index/edam-freeTextSearchIndex/indexRules
13.  You should see the custom indexes

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-23_15-48-7.png?version=1&modificationDate=1614075407167&api=v2)
---------------------------------------------------------------------------------------------

**EDAM config - Environment**

**Source**  
**UAT** : **[https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-east](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-west)**  
**UAT Destination**: **/apps/edam/config.edam-east.uat**  
This step uninstalls required environment specific config for EDAM

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced)
2.  Select Coast 'east' 
3.  Select 'ui.uat.east.apps.config.uat' from drop down for project/type
4.  Provide version Eg:  '1.0.10'
5.  Enter admin password
6.  Click 'Run Job Now' button
7.  Verify logs and wait until job get finished 
8.  It takes ~ 2 min
9.  Enter URL, on the browser:
10.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/de/index.jsp
11.  Navigate to following folder /apps/edam/config.edam-east.rgs and delete config.edam.east.rgs\[This is the one manual step here, only required for the first time\]
12.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/[crx/packmgr/index.jsp](https://rundeck.wsgc.com/rundeck/project/wsgc/jobs/deploy/uat/edam/primary)
13.  Verify the installed version for config, it should show version eg: '1.0.09' , ui.uat.east.apps.config-1.0.9.zip
14.  Goto /crx/de, open /apps/edam/config.edam-east.uat, it should show the config files 

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-23_15-50-54.png?version=1&modificationDate=1614075574557&api=v2)

**EDAM config - common**

This step uninstalls required common  config for EDAM  
**Source** : **[https://github.wsgc.com/eCommerce-DevOps/edam-common-config](https://github.wsgc.com/eCommerce-DevOps/edam-common-config)**  
**Destination**: **/apps/edam/config**

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/2800d819-d92e-47e2-b52e-63b08360fced)
2.  Select Coast : 'east'
3.  Select 'ui.apps.common.config' from drop down for project/type
4.  Provide version Eg:  '1.0.2'
5.  Enter AEM admin password
6.  Click 'Run Job Now' button
7.  Verify logs and wait until job get finished 
8.  It takes ~ 2 min
9.  Enter URL  on the browser, enter admin credentials
10.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/[crx/packmgr/index.jsp](https://rundeck.wsgc.com/rundeck/project/wsgc/jobs/deploy/uat/edam/primary)
11.  Verify the installed version for config, it should show version eg: '1.0.2' (ui.apps.common.config-1.0.2.zip)
12.  Goto /crx/de, it should enable the crx/de to explore
13.  open /apps/edam/config, it should show the config files 

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-23_16-17-45.png?version=1&modificationDate=1614077185397&api=v2)

**Stop AEM Server :** 

**Source: [https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/stop](https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/start)**  
This step stop the AEM server

Rundeck Job URL:  
UAT : [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/c896c5ea-8736-46cf-bb03-77265dd16316](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/c896c5ea-8736-46cf-bb03-77265dd16316)

1.  Go to Rundeck job:
2.  Select 'coast:east'
3.  Click 'Run Job Now' button
4.  Verify logs and wait until job get finished 
5.  It takes ~5 min
6.  Verify by entering following  URL  on the browser.
7.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com):4501/

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-19_2-54-21.png?version=1&modificationDate=1613683381030&api=v2)

**Change run-mode**

This step includes to update run mode and install ICC profiles

**Rundeck job URL:**

**UAT :[https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/abc01b93-15ed-4890-ae56-76539b9e4930](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/abc01b93-15ed-4890-ae56-76539b9e4930)**

Steps to follow : A rundeck job to be triggered for this step.

1.  Go to Rundeck job: 
2.  Select Coast : we
3.  env: 'uat1'
4.  Click 'Run Job Now'
5.  Verify logs and wait until job get finished 
6.  It takes ~5 min

**![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-19_2-49-13.png?version=1&modificationDate=1613683072920&api=v2)**

**Start AEM Server**

**Source: [https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/start](https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/start)**  
This step starts the AEM server in primary mode

1.  Go to Rundeck job:
2.  Select 'coast:east'
3.  Click 'Run Job Now' button
4.  Verify logs and wait until job get finished 
5.  It takes ~10 min
6.  Verify by entering following  URL  on the browser.
7.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com):4501/

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-18_12-51-44.png?version=1&modificationDate=1613683800570&api=v2)

### **install ui.apps.uat.config**:

This step installs required environment specific config for EDAM

**Source**  
**UAT** : **[https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-east](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-west)**  
**UAT Destination**: **/apps/edam/config.edam-we.uat**  
This step installs required environment specific config for EDAM

1.  Go to Rundeck job: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
2.  Select Coast 'east' 
3.  Select 'ui.apps.uat.config' from drop down for project/type
4.  Provide version Eg:  '1.0.5'
5.  Enter admin password
6.  Click 'Run Job Now' button
7.  Verify logs and wait until job get finished 
8.  It takes ~ 2 min
9.  Enter URL, on the browser:
10.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/[crx/packmgr/index.jsp](https://rundeck.wsgc.com/rundeck/project/wsgc/jobs/deploy/uat/edam/primary)
11.  Verify the installed version for config, it should show version eg: '1.0.5' , ui.apps.uat.config-1.0.5.zip
12.  Goto /crx/de, open /apps/edam/config.edam-we.uat, it should show the config file

![](https://confluence.wsgc.com/download/attachments/284238171/image2021-2-24_16-21-58.png?version=1&modificationDate=1614163838413&api=v2)

**Install ui.uat.acls :** 

**Source** **UAT**:**  
**WE: [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-east/we](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/ws)****  
**Destination**: **/home/groups**  
This step installs required ACLs for EDAM

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
3.  Select coast=“east”
4.  Provide version :10.4
5.  Select ‘[ui.uat.](http://ui.uat.mg)acls’ from drop down for project type
6.  Enter admin password
7.  Click ‘Run Job Now’ button
8.  Verify logs and wait until job get finished 
9.  It takes ~ 10 min
10.  Enter the following URL based on the environment on the browser
11.  UAT: [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
12.  Verify the installed version for [ui.uat](http://ui.uat.mg).acls-1.0.4.zip   **WE**

**Reinstall edam.ui.apps-<version>.zip:**
-----------------------------------------

This step reinstalls required AEM ACS Commons on the existing AEM version

1.  Navigate  to [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
2.  Login with Admin credentials
3.  Search for "edam.ui.apps-<version>.zip"  package manager and click on reinstall.  Package name example: **edam.ui.apps-1.0.18.zip**

**Clear JS and CSS Cache :**

This step clears JS and CSS cache at AEM level.

1.  Please hit the following URL in the browser:
2.  [aemsac-vicn001.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/libs/granite/ui/content/dumplibs.html
3.  Provide the credentials
4.  once login then click on "Click here for rebuilding all libraries."
5.  Then you will go navigate to different window
6.  first click on invalidate caches, this step takes ~ 3 minutes
7.  Then click Rebuild libraries, this step takes ~ 30 minutes.

**option 2**:

Restore from VM backup snapshot (step #1 of deployment - [Phase-1.x East Coast Go-Live - EDAM Deployment/Rollback Steps for UAT#1.TakeSnapshotofEastCoastEDAMServerVM](/pages/viewpage.action?pageId=284238192#Phase1.xEastCoastGoLiveEDAMDeployment/RollbackStepsforUAT-1.TakeSnapshotofEastCoastEDAMServerVM):)

**Current UAT and Production package installed versions list**

<div>

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" style="border-collapse: collapse; border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: initial; border-right-style: none; border-right-width: initial; border-bottom-color: initial; border-bottom-style: none; border-bottom-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial;">
 <colgroup><col><col><col></colgroup>
 <tbody><tr>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal" align="center" style="text-align: center;"><b>Package Name</b></p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal" align="center" style="text-align: center;"><b>UAT</b></p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal" align="center" style="text-align: center;"><b>PROD</b></p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <h3 id="Phase1.xEastCoastGoLiveEDAMDeployment/RollbackStepsforUAT-edam.ui.apps">edam.ui.apps</h3>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <h3 id="Phase1.xEastCoastGoLiveEDAMDeployment/RollbackStepsforUAT-ui.oak.index">ui.oak.index</h3>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <h3 id="Phase1.xEastCoastGoLiveEDAMDeployment/RollbackStepsforUAT-ui.apps.common.config">ui.apps.common.config</h3>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <h3 id="Phase1.xEastCoastGoLiveEDAMDeployment/RollbackStepsforUAT-ui.rep.namespaces">ui.rep.namespaces</h3>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <h3 id="Phase1.xEastCoastGoLiveEDAMDeployment/RollbackStepsforUAT-ui.system.user">ui.system.user</h3>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
 </tr>
</tbody></table>

</div>