
    
# EDAM 1.a - Configuration Guide
    
<div class="3D&quot;Section1&quot;">
        
<span style="">Configs for restricting metadata edit of an asset in QA, UAT, PROD</span>The following document contains the list of configurations that are utilized for EDAM 1.a project.

**Story :**

[TRISUL-348](3D"https://jira.wsgc.com/browse/TRISUL-348") :&nbsp;<span style="">WS Rollout - Create and Configure Groups/Privileges on Dev</span>

<span style=""><span style="">ThirdPartyContributorConfig for WS DEV environment :&nbsp;</span></span>
<div class="">
<table class="3D&quot;wrapped" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.services.impl.ThirdPartyContributorConfigServiceFactory~wstpUsers

</td></tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;3rd-party-group folder for WS&nbsp;Third Party Users in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~wstpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/williams-sonoma</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.groups</span></td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_DEV_WS_3rdPartyContributor</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_DEV_WS_PRODUCTION</td>
</tr>
</tbody>
</table>
</div>
<br>

[TRISUL-573](3D"https://jira.wsgc.com/browse/TRISUL-573) WS Rollout - Create and Configure Groups/Privileges for all envs</span>

<span style=""><span style="">ThirdPartyContributorConfig for WS QA, WS UAT and WS PROD environments :</span></span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.services.impl.ThirdPartyContributorConfigServiceFactory~wstpUsers
</td></tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;3rd-party-group folder for WS&nbsp;Third Party Users in QA, UAT and PRODUCTION environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~wstpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(Prod)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/williams-sonoma</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/williams-sonoma</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/williams-sonoma</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
<td class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
<td class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_WS_3rdPartyContributor</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_UAT_WS_3rdPartyContributor</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_WS_3rdPartyContributor</span></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_QA_WS_PRODUCTION</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_UAT_WS_PRODUCTION</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_WS_PRODUCTION</td>
</tr>
</tbody>
</table>
</div>
<br>

**Story :**

[TRISUL-354](3D"https://jira.wsgc.com/browse/TRISUL-354") :&nbsp;<span style="">PB Rollout - Create and Configure Groups/Privileges for Dev</span>

<span style=""><span style="">ThirdPartyContributorConfig for&nbsp;</span>PB Main in Dev environment :</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbMainTpUsers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photographers folder for PB Main Photographers in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbMainTpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/main</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.groups</span></td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_DEV_PB_PHOTOGRAPHERS</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_DEV_PB_PRODUCTION</td>
</tr>
</tbody>
</table>
</div>
<br>

<span style=""><span style="">ThirdPartyContributorConfig for&nbsp;</span>PB KIDS in Dev environment :</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbKidsTpUsers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photographers folder for PB Kids Photographers in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbKidsTpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/kids</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_DEV_PK_Photographers</span></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_DEV_PK_Production</span></p></td>
</tr>
</tbody>
</table>
</div>
<br>

<span style=""><span style="">ThirdPartyContributorConfig for&nbsp;</span>PB TEEN&nbsp;in Dev environment :</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbTeenTpUs=
ers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photographers folder for PB Teen Photographers in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbTeenTpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/teen</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_DEV_PT_Photographers</span></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_DEV_PT_Production</span></p></td>
</tr>
</tbody>
</table>
</div>
<br>

<span style="">Dam metadata update listener config for Dev environment :</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.listeners.DamMetadataUpdateListener</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for Approved Asset Viewers.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "<span style="">Dam metadata update listener config</span>" and click on it.

Following are config param name and corresponding values for WE,PB Main, Kids, Teen brands.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
</col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class=""><span style="">Config Value(Dev)</span></th>
</tr>
<tr>
<td class="">approved.asset.viewers</td>
<td class=""><p>/content/dam/west-elm=APR_EDAM_DEV_WE_MERCHANTS,APR_EDAM_DEV_WE_GENERAL,APR_EDAM_DEV_WE_VENDORS<br>/content/dam/pottery-barn/main=<span style="">APR_EDAM_DEV_PB_GeneralUsers</span>,APR_EDAM_DEV_PB_FRANCHISE<br>/content/dam/pottery-barn/kids=<span style="">APR_EDAM_DEV_PK_GeneralUsers,<span style="">APR_EDAM_DEV_PK_Franchise</span><br>/content/dam/pottery-barn/teen=<span style="">APR_EDAM_DEV_PT_GeneralUsers</span>,<span style="">APR_EDAM_DEV_PT_Franchise</span></p></td>
</tr>
</tbody>
</table>
</div>
<br>

Configs for restricting metadata edit of an asset in DEV environment :
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped"  style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.listeners.RestrictEditMetaData</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for Approved Asset Viewers.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "<span style="">RestrictEditMetaData</span>" and click on it.

Following are config param name and corresponding values for PB.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">editRestrictGroups</span></td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_DEV_PB_PRSocial</span></p><p><span style="">APR_EDAM_DEV_PT_PRSocial</span></p><p><span style="">APR_EDAM_DEV_PK_PRSocial</span></p></td>
</tr>
</tbody>
</table>
</div>
<br>

**Story :**

[TRISUL-574]("3Dhttps://jira.wsgc.com/browse/TRISUL-574)&nbsp;:&nbsp;<span style="">PB Rollout - Create and Configure Groups/Privileges for all the environments</span>

<span style=""><span style="">ThirdPartyContributorConfig for PB Main QA,&nbsp;PB Main UAT and&nbsp;PB Main PROD environments :</span></span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbMainTpUsers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photographers folder for PB Main Photographers in QA, UAT and PROD environments.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbMainTpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(Prod)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/main</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/main</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/main</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.groups</span></td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_QA_PB_PHOTOGRAPHERS</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_UAT_PB_PHOTOGRAPHERS</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_PB_PHOTOGRAPHERS</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_QA_PB_PRODUCTION</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_UAT_PB_PRODUCTION</td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_PB_PRODUCTION</td>
</tr>
</tbody>
</table>
</div>
<br>

<span style=""><span style="">ThirdPartyContributorConfig for PB Kids QA,&nbsp;PB&nbsp;Kids UAT and&amp;nbsp;PB&nbsp;Kids PROD environments :</span></span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped"  style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbKidsTpUs=
ers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photographers folder for PB Kids Photographers in QA, UAT and PROD environments.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbKidsTpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(Prod)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/kids</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/kids</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/kids</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_PK_Photographers</span></td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_UAT_PK_Photographers</td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_PK_Photographers</span></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_PK_Production</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_UAT_PK_Production</span></td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_PK_Production<span style="">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span></td>
</tr>
</tbody>
</table>
</div>
<br>

<span style=""><span style="">ThirdPartyContributorConfig for PB Teen QA,&nbsp;PB&nbsp;Teen UAT and&amp;nbsp;PB&nbsp;Teen PROD environments :</span></span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped"  style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbMainTpUsers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photographers folder for PB Teen Photographers in QA, UAT and PROD environments.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbTeenTpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(Prod)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/teen</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/teen</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/teen</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.party.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_PT_Photographers</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_UAT_PT_Photographers</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_PT_Photographers</span></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_PT_Production</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_UAT_PT_Production</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_PT_Production</span></td>
</tr>
</tbody>
</table>
</div>
<br>

<span style="">Dam metadata update listener config for QA, UAT, PROD environments :</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped"  style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.dam.core.listeners.DamMetadataUpdateListener</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for Approved Asset Viewers.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "<span style="">Dam metadata update listener config</span>" and click on it.

Following are config param name and corresponding values for WE,PB Main, Kids, Teen brands in QA,UAT and PROD environment
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(QA)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">approved.asset.viewers</td>
<td class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=APR_EDAM_QA_WE_MERCHANTS,APR_EDAM_QA_WE_GENERAL,APR_EDAM_QA_WE_VENDORS<br>/content/dam/pottery-barn/main=<span style="">APR_EDAM_QA_PB_GeneralUsers,APR_EDAM_QA_PB_FRANCHISE<br>/content/dam/pottery-barn/kids=<span style="">APR_EDAM_QA_PK_GeneralUsers</span>,&nbsp;<span style="">APR_EDAM_QA_PK_Franchise</span><br>/content/dam/pottery-barn/teen=<span style="">APR_EDAM_QA_PT_GeneralUsers</span>,<span style="">APR_EDAM_QA_PT_Franchise</span></span></p></td>
</tr>
</tbody>
</table>
</div>
<span style="">UAT&nbsp;<u><strong>:</strong></u></span>

<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(UAT)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">approved.asset.viewers</td>
<td class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=APR_EDAM_UAT_WE_MERCH=
ANTS,APR_EDAM_UAT_WE_GENERAL,APR_EDAM_UAT_WE_VENDORS  
/content/dam/pottery-barn/main=<span style="">APR_EDAM_UAT_PB_GeneralUsers</span>,APR_EDAM_UAT_PB_FRANCHISE  
/content/dam/pottery-barn/kids=<span style="">APR_EDAM_UAT_PK_GeneralUsers</span>,<span style="">APR_EDAM_UAT_PK_Franchise</span>  
/content/dam/pottery-barn/teen=<span style="">APR_EDAM_UAT_PT_GeneralUsers</span>,<span style="">APR_EDAM_UAT_PT_Franchise</span></p></td>
</tr>
</tbody>
</table>
</div>
<p>  
</p>
<p><span style=""><em>PROD</em><u><em> :</em></u></span></p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(PROD)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">approved.asset.viewers</td>
<td class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=APR_EDAM_WE_MERCHANTS_USERS,APR_EDAM_WE_GENERAL_USERS,APR_EDAM_WE_VENDORS_USERS  
/content/dam/pottery-barn/main=<span style="">APR_EDAM_PB_GeneralUsers</span>,APR_EDAM_PB_FRANCHISE  
/content/dam/pottery-barn/kids=<span style="">APR_EDAM_PK_GeneralUsers,<span style="">APR_EDAM_PK_Franchise</span>  
/content/dam/pottery-barn/teen=<span style="">APR_EDAM_PT_GeneralUsers,<span style="">APR_EDAM_PT_Franchise</span></span></span></p>
</td></tr>
</tbody>
</table>
</div>
<p>  
</p>
<p>Configs for restricting metadata edit of an asset in QA, UAT, PROD :</p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped"  style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.listeners.RestrictEditMetaData</td>
</tr>
</tbody>
</table>
</div>
<p>Following custom configuration's are required for Approved Asset Viewers.</p>
<p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "<span style="">RestrictEditMetaData</span>" and click on it.</p>
<p>Following are config param name and corresponding values for PB.</p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;">  
</th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value(PROD)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">editRestrictGroups</span></td>
<td class="3D&quot;confluenceTd&quot;">  
</td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_QA_PB_PRSocial</span></p><p><span style="">APR_EDAM_QA_PT_PRSocial</span></p><p><span style="">APR_EDAM_QA_PK_PRSocial</span></p></td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_UAT_PB_PRSocial</span></p><p><span style="">APR_EDAM_UAT_PT_PRSocial</span></p><p><span style="">APR_EDAM_UAT_PK_PRSocial</span></p></td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_PB_PRSocial</span></p><p><span style="">APR_EDAM_PT_PRSocial</span></p><p><span style="">APR_EDAM_PK_PRSocial</span></p></td>
</tr>
</tbody>
</table>
</div>
<p>  
</p>
<p><strong>Story :</strong></p>
<p>TRISUL-352 : PB Rollout - High Resolution Threshold</p>
<p>TRISUL-346 :&nbsp;WS Rollout - High Resolution Threshold</p>
<p><strong><span style="">Config Name : High Resolution listener config</span></strong></p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped"  style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.listeners.HighResolutionImageListener</td>
</tr>
</tbody>
</table>
</div>
<p>Following custom configuration's are required for setting high resolution threshold values for an asset.</p>
<p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "<span style="">High Resolution listener config</span>" and click on it.</p>
<p>Following are config param name and corresponding values for PB.</p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">high.resolution.threshold</td>
<td class="3D&quot;confluenceTd&quot;"><p>/content/dam/pottery-barn=4800</p><p>/content/dam/williams-sonoma=2000</p><p>/content/dam/west-elm=2000</p></td>
</tr>
</tbody>
</table>
</div>
<p>  
</p>
<p><strong>Story :</strong></p>
<p>TRISUL-350 : PB Rollout - Metadata Cascading &amp; Retrofit WSI Schema
</p><p>TRISUL-344 : WS Rollout - Metadata Cascading &amp; Retrofit WSI Schema
</p><p><span style="">SummaryTab Configurations :</span></p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped"  style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.edam.core.services.impl.SummaryTabService</td>
</tr>
</tbody>
</table>
</div>
<p>Following custom configuration's are required for enabling Summary tab functionality of an asset.</p>
<p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)  
Search for "<span style="">SummaryTab Configurations</span>" and click on it.</p>
<p>Following are config param name and corresponding values.</p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" >
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config Value</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">SummaryTab
</span></td>
<td class="3D&quot;confluenceTd&quot;"><p>
wsi:brand=Brand#Creative  
wsi:asset-type=Asset Type#Creative  
wsi:year=Year#Creative  
wsi:season=Season#Creative  
wsi:spread=Spread#Creative  
wsi:crop=Crop#Creative  
wsi:skus=SKUs#Product  
wsi:group-ids=Group IDs#Product  
wsi:collection=Collection#Product  
wsi:product-type=Product Type#Product  
wsi:status=Approval Status#Process  
wsi:isHighResolution=Is High Resolution&lt;br&gt;wsi:product-name=Product Name#Product</p></td>
</tr>
</tbody>
</table>
</div>
   </div> ** **<strong>
</strong>**