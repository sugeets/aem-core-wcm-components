  

Phase-1.X AEM Set-up and EDAM Deployment Steps for West Coast UAT
=================================================================

*   [1. AEM Set-up:](#test)
*   [2\. AEM Start-up:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [3\. EDAM config - common:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [4\. EDAM config - Environment:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [5\. EDAM Config - oak index:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [6\. EDAM Config - system user:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [7\. EDAM Config - namespaces:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [8\. EDAM Config - ACLs:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [9\. EDAM App code :](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [10\. EDAM AEM Restart:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [11\. AEM Service Pack upgrade:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [12\. EDAM AEM Restart:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [13\. AEM ACS Commons upgrade:](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [14\. Post-Deployment Steps: (Execution Time - 30 mins)](#Phase1.XAEMSetupandEDAMDeploymentStepsf)
*   [Validation Checklist: EDAM 1.x - West- Validation Checklist](#Phase1.XAEMSetupandEDAMDeploymentStepsf)

· [Rollback Step](#Phase1.XAEMSetupandEDAMDeploymentStepsf)



**1. AEM Set-up:**
------------------

This step installs ImageMagick 6.7.8.9-16, Installs JDK, install icc profile from , integrates AEM 6.5 with AppDynamics  & Kibana (file beat) and enable Apache(httpd) & show logs on port 38667

**Sources : [https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config](https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config)** **[https://github.wsgc.com/eCommerce-DevOps/aem-edam-uat-config](https://github.wsgc.com/eCommerce-DevOps/aem-edam-uat-config)**

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-install](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-install)
3.  Select Coast : west
4.  env: 'uat2'
5.  Click 'Run Job Now'
6.  Verify logs and wait until job get finished 
7.  It takes ~10 min

![](aemwestuat/image001.png?raw=true)

**2\. AEM Start-up:**
---------------------

**Source: [https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/start](https://github.wsgc.com/eCommerce-DevOps/aem-edam-common-config/blob/master/src/main/resources/apps/aemscripts/start)**  
This step starts the AEM server in primary mode

1.  Go to Rundeck job:
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/wsgc-deploy-uat-edam-primary-start](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/wsgc-deploy-uat-edam-primary-start)
3.  Select 'coast:west '
4.  Click 'Run Job Now' button
5.  Verify logs and wait until job get finished 
6.  It takes ~10 min
7.  Verify by entering following  URL  on the browser.
8.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com):4501/

![](aemwestuat/image002.png?raw=true)

**3\. EDAM config - common:**
-----------------------------

This step installs required common  config for EDAM  
**Source** : [https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/ui-apps-config](https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/ui-apps-config)  
**Destination**: **/apps/edam/config**

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
3.  Select Coast : 'west'
4.  Select 'ui.apps.common.config' from drop down for project/type
5.  Provide version Eg:  '1.0.2'
6.  Enter AEM admin password
7.  Click 'Run Job Now' button
8.  Verify logs and wait until job get finished 
9.  It takes ~ 2 min
10.  Enter URL  on the browser, enter admin credentials
11.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/[crx/packmgr/index.jsp](https://rundeck.wsgc.com/rundeck/project/wsgc/jobs/deploy/uat/edam/primary)
12.  Verify the installed version for config, it should show version eg: '1.0.2' (ui.apps.common.config-1.0.2.zip)
13.  Goto /crx/de, it should enable the crx/de to explore
14.  open /apps/edam/config, it should show the config files 

**![](aemwestuat/image003.png?raw=true)**

**4\. EDAM config - Environment:**
----------------------------------

This step installs required environment specific (run mode) config for EDAM

**Source**  
**UAT** : **[https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-west](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-apps-config/edam-west)**  
**UAT Destination**: **/apps/edam/config.edam-west.uat**  
This step installs required environment specific (run mode) config for EDAM

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
3.  Select Coast 'west' 
4.  Select 'ui.uat.west.apps.config.uat' from drop down for project/type
5.  Provide version Eg:  '1.0.10'
6.  Enter admin password
7.  Click 'Run Job Now' button
8.  Verify logs and wait until job get finished 
9.  It takes ~ 2 min
10.  Enter URL, on the browser:
11.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/[crx/packmgr/index.jsp](https://rundeck.wsgc.com/rundeck/project/wsgc/jobs/deploy/uat/edam/primary)
12.  Verify the installed version for config, it should show version eg: '1.0.10' , ui.uat.west.apps.config-1.0.9.zip
13.  Goto /crx/de, open /apps/edam/config.edam-west.uat, it should show the config files 

#test
![](aemwestuat/image004.png?raw=true)

**5\. EDAM Config - oak index:**
--------------------------------

**Source** : **[https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/oak-index](https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/oak-index)**  
**Destination**: **/oak:index/edam-freeTextSearchIndex**  
This step installs required oak indexes for EDAM

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
3.  Select coast ‘west’
4.  Select ‘oak-index’ from drop down for project
5.  Provide version Eg: ‘1.0.2’
6.  Enter admin password
7.  Click ‘Run Job Now’ button
8.  Verify logs and wait until job get finished 
9.  It takes ~1 min
10.  Enter following URLs on the browser
11.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
12.  Verify the installed version for oak-index, it should show version Eg:  ‘1.0.2’ (ui.oak.index-1.0.2.zip)
13.  Goto crx/de, navigate to the following path /oak:index/edam-freeTextSearchIndex/indexRules
14.  You should see the custom indexes

![](aemwestuat/image005.png?raw=true)  
**6\. EDAM Config - system user:**
-----------------------------------------------------------------

  
**Source** : **[https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/system-user](https://github.wsgc.com/eCommerce-DevOps/edam-common-config/tree/release/edam/system-user)**  
**Destination**: **/home/users/system/OVJR6UwbRfW3d5tmLavM**  
This step installs required system user for EDAM

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
3.  Select coast =“west”
4.  Provide version Eg: ‘1.0.2’
5.  Select ‘system-user’ from drop down for project
6.  Enter admin password
7.  Click ‘Run Job Now’ button
8.  Verify logs and wait until job get finished 
9.  It takes ~ 2 min
10.  Enter following URL on the browser based the environment:
11.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
12.  Verify the installed version for system-user, it should show version Eg; ‘1.0.2’
13.  Goto /useradmin, search for ‘edamSystemUser’
14.  Select the edamSystemUser & click permissions tab
15.  Validate all permissions are available

![](aemwestuat/image006.png?raw=true)  
**7\. EDAM Config - namespaces:**
----------------------------------------------------------------

  
**Source** : **[https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam](https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam)**  
**Destination**: **/apps/edam/install**  
**This step installs required namespaces for EDAM**

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
3.  Select coast=“west”
4.  Select ‘ui.rep.namespaces’ from drop down for project
5.  Provide version Eg: ‘1.0.2’
6.  Enter admin password
7.  Click ‘Run Job Now’ button
8.  Verify logs and wait until job get finished 
9.  It takes ~ 2 min
10.  Enter following URL on the browser based on the environment
11.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
12.  Verify the installed version for namespaces, it should show version Eg: ‘1.0.2’
13.  Goto /crx/de and open /jcr:system/rep:namespaces
14.  It should show wsi namespaces

![](aemwestuat/image007.png?raw=true)  
**8\. EDAM Config - ACLs:**
----------------------------------------------------------

  
**Source** **UAT**:  
**PB : [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/pb](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/pb)**  
**WS: [https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/ws](https://github.wsgc.com/eCommerce-DevOps/edam-uat-config/tree/release/edam/ui-acls/edam-west/ws)**  
**Destination**: **/home/groups**  
This step installs required ACLs for EDAM

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-custom-primary)
3.  Select coast=“west”
4.  Provide version Eg:‘1.0.9’
5.  Select ‘ui.uat.pb.acls’ from drop down for project type **PB** or select ‘[ui.uat.ws](http://ui.uat.ws/).acls’ from drop down for project type **WS**
6.  Enter admin password
7.  Click ‘Run Job Now’ button
8.  Verify logs and wait until job get finished 
9.  It takes ~ 2 min
10.  Enter the following URL based on the environment on the browser
11.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
12.  Verify the installed version for ui.uat.pb.acls-1.0.9.zip  for **PB**  and
13.  [ui.uat.ws](http://ui.uat.ws).acls-1.0.9.zip for **WS**

  
**PB:**

![](aemwestuat/image008.png?raw=true)  
**WS**

**![](aemwestuat/image009.png?raw=true)**

**9\. EDAM App code :**
-----------------------

  
**Source** : **[https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam](https://github.wsgc.com/eCommerce-Bedrock/enterprise-dam)**  
**Destination**: **/apps/edam/install**  
**This step installs required App code - EDAM**

1.  Go to Rundeck job: 
2.  UAT : [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Deploy-Edam-Uat-Code](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Deploy-Edam-Uat-Code)
3.  Select coast: west
4.  Provide version Eg: ‘1.0.16’
5.  Enter admin password
6.  Click ‘Run Job Now’ button
7.  Verify logs and wait until job get finished 
8.  It takes ~ 3 min
9.  Enter the followig URL based on the environment on the browser
10.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
11.  Verify the installed version for config, it should show version Eg: ‘1.0.16’

![](aemwestuat/image010.png?raw=true)

**10\. EDAM AEM Restart:**
--------------------------

**This step restarts AEM** 

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Restart-Uat-Aem-Service](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Restart-Uat-Aem-Service)
3.  Select coast :“west”
4.  Click ‘Run Job Now’ button
5.  Verify logs and wait until job get finished 
6.  It takes ~ 10 min
7.  Enter URL the following URL based on the environment on the browser
8.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/

![](aemwestuat/image011.png?raw=true)  
**11\. AEM Service Pack upgrade:**
-----------------------------------------------------------------

  
**Source : [https://artifactory.wsgc.com/artifactory/ext-release-local/com/adobe/aem/6.5.2/](https://artifactory.wsgc.com/artifactory/ext-release-local/com/adobe/aem/6.5.2/)**  
**Destination** : **/libs**  
This step installs required service pack to the existing AEM version

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-uat-sp-upgrade](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-uat-sp-upgrade)
3.  Select coast : ‘west’
4.  Enter version as “AEM-6.5.2-SP2.zip” as in aritfactory
5.  Click ‘Run Job Now’ button
6.  Verify logs and wait until job get finished 
7.  It takes ~10 min
8.  Enter the following URL based on environment on the browser
9.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/welcome
10.  Verify the version, it should show 6.5.2.0

![](aemwestuat/image012.png?raw=true)

**12\. EDAM AEM Restart:**
--------------------------

  
**This step restarts AEM**   
**Follow same steps that mentioned in step-1013. AEM ACS Commons upgrade:**  
**Source : [https://artifactory.wsgc.com/artifactory/ext-release-local/com/adobe/aem/6.5.2/](https://artifactory.wsgc.com/artifactory/ext-release-local/com/adobe/aem/6.5.2/)**  
**Destination** :**/etc**  
This step installs required service pack to the existing AEM version

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Restart-Uat-Aem-Service](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/Restart-Uat-Aem-Service)
3.  Select coast :“west”
4.  Click ‘Run Job Now’ button
5.  Verify logs and wait until job get finished 
6.  It takes ~ 10 min
7.  Enter URL the following URL based on the environment on the browser
8.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/

![](aemwestuat/image013.png?raw=true)
----------------------------

**13\. AEM ACS Commons upgrade:**
---------------------------------

**Source :**  
**[https://artifactory.wsgc.com/artifactory/ext-release-local/com/adobe/aem/6.5.2/](https://artifactory.wsgc.com/artifactory/ext-release-local/com/adobe/aem/6.5.2/)**  
**Destination** :**/etc**  
This step installs required AEM ACS Commons

1.  Go to Rundeck job: 
2.  UAT: [https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-uat-sp-upgrade](https://rundeck.wsgc.com/rundeck/project/wsgc/job/show/deploy-uat-edam-uat-sp-upgrade)
3.  Select coast: 'west'
4.  Select version as acs-aem-commons-4-4-0 from the drop down
5.  Click 'Run Job Now' button
6.  Verify logs and wait until job get finished 
7.  It takes  ~3 min
8.  Enter the following URL based on the environment on the browser
9.  UAT: [aemsac-vicn003.wsgc.com](http://aemsac-vicn003.wsgc.com/):4501/crx/packmgr/index.jsp
10.  Verify the three ACS Commons packages

![](aemwestuat/image014.png?raw=true)  
**14\. Post-Deployment Steps: (Execution Time - 30 mins)**
-----------------------------------------------------------------------------------------

**S.No**

**Jira-id**

**User Story**

**Post Deployment Steps**

2

TRISUL-7

Duo Security SAML SSO Setup

Detailed steps here - [Configure SAML Integration on EDAM AEM Environments](../../../../../../display/PdM/Configure+SAML+Integration+on+EDAM+AEM+Environments)

3

NA

Sync Workflow

1.  WorkflowGo to /editor.html/conf/global/settings/workflow/models/dam/update\_asset.html and click 'Sync'
2.  Go to /conf/global/settings/workflow/models/dam/ws\_legacy\_to\_edam\_post\_migration\_workflow and 'Sync'

**Validation Checklist: [EDAM 1.x - West- Validation Checklist](../../../../../../display/PdM/EDAM+1.x+-+West-+Validation+Checklist)**
--------------------------------------------------------------------------------------------------------------------------------------

**Rollback Step**
=================

Restore from VM backup snapshot (step #1 of deployment - [Phase-1.X AEM Set-up and EDAM Deployment Steps for West Coast UAT](https://confluence.wsgc.com/pages/viewpage.action?pageId=284238230#Phase1.xWSMigrationonWestCoastEDAMDeployment/RollbackStepsforUAT-1.TakeSnapshotofWestCoastEDAMServerVM):)