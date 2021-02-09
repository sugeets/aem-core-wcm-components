
    
# EDAM 1.a - Configuration Guide
    
<div class="3D&quot;Section1&quot;">
        
<span style="">Configs for restricting me=
tadata edit of an asset in QA, UAT, PROD</span>The following document conta=
ins the list of configurations that are utilized for EDAM 1.a project.

**Story :**

[TRISUL-348](3D"https://jira.wsgc.com/browse/TRISUL-348") :&nbsp;<span style="">WS Rollout - Create and Configure Groups/Privileges on Dev</span>

<span style=""><span style="">ThirdPartyContributorConfig for WS DEV environment :&nbsp;</span></span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~wstpUsers&lt;=
/td&gt;
</td></tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;3rd-part=
y-group folder for WS&nbsp;Third Party Users in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~wstpUs=
ers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path=
</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/williams-sonoma</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.groups</span></td>
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

[TRISUL](3D"https://jira.wsgc.com/browse/TRISUL-348")[-573](3D"https://jira.wsgc.com/browse/TRIS=)&nbsp;:&nbsp;<span= style="">WS Rollout - Create and Configure Groups/P=
rivileges for all envs</span=>

<span style=""><span style="">ThirdPartyContributorConfig for WS QA, WS UAT and WS PROD environments =
:</span></span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~wstpUsers&lt;=
/td&gt;
</td></tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;3rd-part=
y-group folder for WS&nbsp;Third Party Users in QA, UAT and PRODUCTION envi=
ronment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~wstpUs=
ers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Prod)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path=
</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/williams-sonoma</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/williams-sonoma</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/williams-sonoma</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
<td class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
<td class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_W=
S_3rdPartyContributor</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_UAT_=
WS_3rdPartyContributor</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_WS_3=
rdPartyContributor</span></td>
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

<span style=""><span style="">ThirdPartyContributorConfig for&nbsp;</span>PB Main in Dev environment =
:</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbMainTpUs=
ers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photogra=
phers folder for PB Main Photographers in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbMain=
TpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path=
</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/main</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.groups</span></td>
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

<span style=""><span style="">ThirdPartyContributorConfig for&nbsp;</span>PB KIDS in Dev environment =
:</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbKidsTpUs=
ers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photogra=
phers folder for PB Kids Photographers in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbKids=
TpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path=
</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/kids</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_DEV_=
PK_Photographers</span></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_D=
EV_PK_Production</span></p></td>
</tr>
</tbody>
</table>
</div>
<br>

<span style=""><span style="">ThirdPartyContributorConfig for&nbsp;</span>PB TEEN&nbsp;in Dev environ=
ment :</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbTeenTpUs=
ers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photogra=
phers folder for PB Teen Photographers in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbTeen=
TpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path=
</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/teen</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_DEV_=
PT_Photographers</span></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_D=
EV_PT_Production</span></p></td>
</tr>
</tbody>
</table>
</div>
<br>

<span style="">Dam metadata update listener confi=
g for Dev environment :</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.listeners.DamMetadataUpdateListener</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for Approved Asset Viewers=
.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "<span style="">Dam metada=
ta update listener config</span>" and click on it.

Following are config param name and corresponding values for WE,PB Main,=
 Kids, Teen brands.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">approved.asset.viewers</td>
<td class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=3DAPR_EDAM_DEV_WE_MERCH=
ANTS,APR_EDAM_DEV_WE_GENERAL,APR_EDAM_DEV_WE_VENDORS<br>/content/dam/potter=
y-barn/main=3D<span style="">APR_EDAM_DEV_PB_GeneralUse=
rs</span>,APR_EDAM_DEV_PB_FRANCHISE<br>/content/dam/pottery-barn/kids=3D<sp= an="" style="">APR_EDAM_DEV_PK_GeneralUsers,<span s="tyle=3D&quot;color:">APR_EDAM_DEV_PK_Franchise</span><br>/content/da=
m/pottery-barn/teen=3D<span style="">APR_EDAM_DEV_PT_Ge=
neralUsers</span>,<span style="">APR_EDAM_DEV_PT_Franch=
ise</span></sp=></p></td>
</tr>
</tbody>
</table>
</div>
<br>

Configs for restricting metadata edit of an asset in DEV environment :
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.listeners.RestrictEditMetaData</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for Approved Asset Viewers=
.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "<span style="">RestrictEd=
itMetaData</span>" and click on it.

Following are config param name and corresponding values for PB.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Dev)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">editRestri=
ctGroups</span></td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_D=
EV_PB_PRSocial</span></p><p><span style="">APR_EDAM_DEV=
_PT_PRSocial</span></p><p><span style="">APR_EDAM_DEV_P=
K_PRSocial</span></p></td>
</tr>
</tbody>
</table>
</div>
<br>

**Story :**

[TRISUL](3D"https://jira.wsgc.com/browse/TRISUL-348")[-574](3D"https://jira.wsgc.com/browse/TRIS=)&nbsp;:&nbsp;<span= style="">PB Rollout - Create and Configure Groups/P=
rivileges for all the environments</span=>

<span style=""><span style="">ThirdPartyContributorConfig for PB Main QA,&nbsp;PB Main UAT and&nbsp;P=
B Main PROD environments :</span></span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbMainTpUs=
ers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photogra=
phers folder for PB Main Photographers in QA, UAT and PROD environments.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbMain=
TpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Prod)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path=
</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/main</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/main</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/main</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.groups</span></td>
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

<span style=""><span style="">ThirdPartyContributorConfig for PB Kids QA,&nbsp;PB&nbsp;Kids UAT and&amp;n=
bsp;PB&nbsp;Kids PROD environments :</span></span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbKidsTpUs=
ers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photogra=
phers folder for PB Kids Photographers in QA, UAT and PROD environments.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbKids=
TpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Prod)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path=
</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/kids</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/kids</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/kids</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_P=
K_Photographers</span></td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_UAT_PK_Photographers</td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_PK_P=
hotographers</span></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_P=
K_Production</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_UAT_=
PK_Production</span></td>
<td class="3D&quot;confluenceTd&quot;">APR_EDAM_PK_Production<span style="" inhe="rit;&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span></td>
</tr>
</tbody>
</table>
</div>
<br>

<span style=""><span style="">ThirdPartyContributorConfig for PB Teen QA,&nbsp;PB&nbsp;Teen UAT and&amp;n=
bsp;PB&nbsp;Teen PROD environments :</span></span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~pbMainTpUs=
ers</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for creating&nbsp;photogra=
phers folder for PB Teen Photographers in QA, UAT and PROD environments.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "ThirdPartyContributorConfigServiceFactory~pbTeen=
TpUsers" and click on it.

Following are config param names and corresponding values.
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(Prod)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">brand.path=
</span></td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/teen</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/teen</td>
<td class="3D&quot;confluenceTd&quot;">/content/dam/pottery-barn/teen</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.folder</span></td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
<td class="3D&quot;confluenceTd&quot;">photographers</td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">third.part=
y.groups</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_P=
T_Photographers</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_UAT_=
PT_Photographers</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_PT_P=
hotographers</span></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">other.allowed.groups</td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_QA_P=
T_Production</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_UAT_=
PT_Production</span></td>
<td class="3D&quot;confluenceTd&quot;"><span style="">APR_EDAM_PT_P=
roduction</span></td>
</tr>
</tbody>
</table>
</div>
<br>

<span style="">Dam metadata update listener confi=
g for QA, UAT, PROD environments :</span>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.listeners.DamMetadataUpdateListener</td>
</tr>
</tbody>
</table>
</div>
Following custom configuration's are required for Approved Asset Viewers=
.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "<span style="">Dam metada=
ta update listener config</span>" and click on it.

Following are config param name and corresponding values for WE,PB Main,=
 Kids, Teen brands in QA,UAT and PROD environment
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(QA)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">approved.asset.viewers</td>
<td class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=3DAPR_EDAM_QA_WE_MERCHA=
NTS,APR_EDAM_QA_WE_GENERAL,APR_EDAM_QA_WE_VENDORS<br>/content/dam/pottery-b=
arn/main=3D<span style="">APR_EDAM_QA_PB_GeneralUsers,APR_EDAM_QA_PB_FRANCHISE<br>/content/dam/pottery-barn/kids=3D<span st="yle=3D&quot;color:">APR_EDAM_QA_PK_GeneralUsers</span>,&nbsp;<span s="tyle=3D&quot;color:">APR_EDAM_QA_PK_Franchise</span><br>/content/dam=
/pottery-barn/teen=3D<span style="">APR_EDAM_QA_PT_Gene=
ralUsers</span>,<span style="">APR_EDAM_QA_PT_Franchise=
</span></span></p></td>
</tr>
</tbody>
</table>
</div>
<span style="">UAT&nbsp;<u>*<strong>:</strong>*</u></span>

**<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(UAT)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">approved.asset.viewers</td>
<td class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=3DAPR_EDAM_UAT_WE_MERCH=
ANTS,APR_EDAM_UAT_WE_GENERAL,APR_EDAM_UAT_WE_VENDORS  
/content/dam/potter=
y-barn/main=3D<span style="">APR_EDAM_UAT_PB_GeneralUse=
rs</span>,APR_EDAM_UAT_PB_FRANCHISE  
/content/dam/pottery-barn/kids=3D<sp= an="" style="">APR_EDAM_UAT_PK_GeneralUsers,<span s="tyle=3D&quot;color:">APR_EDAM_UAT_PK_Franchise</span>  
/content/da=
m/pottery-barn/teen=3D<span style="">APR_EDAM_UAT_PT_Ge=
neralUsers</span>,<span style="">APR_EDAM_UAT_PT_Franch=
ise</span></sp=></p></td>
</tr>
</tbody>
</table>
</div>
<p>  
</p>
<p><span style=""><em>PROD</em><u><em><strong> :&lt;=
/strong&gt;</strong></em></u></span></p><strong>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(PROD)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">approved.asset.viewers</td>
<td class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=3DAPR_EDAM_WE_MERCHANTS=
_USERS,APR_EDAM_WE_GENERAL_USERS,APR_EDAM_WE_VENDORS_USERS  
/content/dam/=
pottery-barn/main=3D<span style="">APR_EDAM_PB_GeneralU=
sers</span>,APR_EDAM_PB_FRANCHISE  
/content/dam/pottery-barn/kids=3D<span= style="">APR_EDAM_PK_GeneralUsers,<span style="">APR_EDAM_PK_Franchise</span>  
/content/dam/potter=
y-barn/teen=3D<span style="">APR_EDAM_PT_GeneralUsers,<span style="">APR_EDAM_PT_Franchise</span></span></span=></p>
</td></tr>
</tbody>
</table>
</div>
<p>  
</p>
<p>Configs for restricting metadata edit of an asset in QA, UAT, PROD :</p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.listeners.RestrictEditMetaData</td>
</tr>
</tbody>
</table>
</div>
<p>Following custom configuration's are required for Approved Asset Viewers=
.</p>
<p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "<span style="">RestrictEd=
itMetaData</span>" and click on it.</p>
<p>Following are config param name and corresponding values for PB.</p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;">  
</th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(QA)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(UAT)</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value(PROD)</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">editRestri=
ctGroups</span></td>
<td class="3D&quot;confluenceTd&quot;">  
</td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_Q=
A_PB_PRSocial</span></p><p><span style="">APR_EDAM_QA_P=
T_PRSocial</span></p><p><span style="">APR_EDAM_QA_PK_P=
RSocial</span></p></td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_U=
AT_PB_PRSocial</span></p><p><span style="">APR_EDAM_UAT=
_PT_PRSocial</span></p><p><span style="">APR_EDAM_UAT_P=
K_PRSocial</span></p></td>
<td class="3D&quot;confluenceTd&quot;"><p><span style="">APR_EDAM_P=
B_PRSocial</span></p><p><span style="">APR_EDAM_PT_PRSo=
cial</span></p><p><span style="">APR_EDAM_PK_PRSocial</span></p></td>
</tr>
</tbody>
</table>
</div>
<p>  
</p>
<p><strong>Story :</strong></p>
<p>TRISUL-352 : PB Rollout - High Resolution Threshold</p>
<p>TRISUL-346 :&nbsp;WS Rollout - High Resolution Threshold</p>
<p><strong><span style="">Config Name : High Resolut=
ion listener config</span></strong></p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.listeners.HighResolutionImageListener</td>
</tr>
</tbody>
</table>
</div>
<p>Following custom configuration's are required for setting high resolutio=
n threshold values for an asset.</p>
<p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "<span style="">High Resol=
ution listener config</span>" and click on it.</p>
<p>Following are config param name and corresponding values for PB.</p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">high.resolution.threshold</td>
<td class="3D&quot;confluenceTd&quot;"><p>/content/dam/pottery-barn=3D4800</p><p>/conte=
nt/dam/williams-sonoma=3D2000</p><p>/content/dam/west-elm=3D2000</p></td>
</tr>
</tbody>
</table>
</div>
<p>  
</p>
<p><strong>Story :</strong></p>
<p>TRISUL-350 : PB Rollout - Metadata Cascading &amp; Retrofit WSI Schema
</p><p>TRISUL-344 : WS Rollout - Metadata Cascading &amp; Retrofit WSI Schema
</p><p><span style="">SummaryTab Configurations :</span>=
</p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="" style="">
<colgroup>
<col>
</colgroup>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
dam.core.services.impl.SummaryTabService</td>
</tr>
</tbody>
</table>
</div>
<p>Following custom configuration's are required for enabling Summary tab f=
unctionality of an asset.</p>
<p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
/configMgr)  
Search for "<span style="">SummaryTab=
 Configurations</span>" and click on it.</p>
<p>Following are config param name and corresponding values.</p>
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;wrapped" confluencetable"="">
<colgroup>
<col>
<col>
</colgroup>
<tbody>
<tr>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Param</span></th>
<th class="3D&quot;confluenceTh&quot;"><span style="">Config =
Value</span></th>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;"><span style="">SummaryTab=
</span></td>
<td class="3D&quot;confluenceTd&quot;"><p>wsi:brand=3DBrand#Creative  
wsi:asset-type=
=3DAsset Type#Creative  
wsi:year=3DYear#Creative  
wsi:season=3DSeason#C=
reative  
wsi:spread=3DSpread#Creative  
wsi:crop=3DCrop#Creative  
wsi:=
skus=3DSKUs#Product  
wsi:group-ids=3DGroup IDs#Product  
wsi:collection=
=3DCollection#Product  
wsi:product-type=3DProduct Type#Product  
wsi:sta=
tus=3DApproval Status#Process  
wsi:isHighResolution=3DIs High Resolution&lt;=
br&gt;wsi:product-name=3DProduct Name#Product</p></td>
</tr>
</tbody>
</table>
</div>
    </strong>**</div> **<strong>
&#13;&#10;&#13;&#10;&#13;&#10;</strong>**