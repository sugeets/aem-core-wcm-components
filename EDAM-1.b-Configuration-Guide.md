
    
# EDAM 1.b - Configuration Guide
    
<div class="3D&quot;Section1&quot;">
        
<br>

The following document contains the list of configurations that are util=
ized for EDAM 1.b project. Below is an example for reference ONLY.
> 
> 
> **Story :**
> 
> **<span style=""> <span class="3D&quot;jira-issue" resolved"="" data-jira-key="3D&quot;TRISUL-859&quot;"> [<im= g="" class="3D&quot;icon&quot;" src="3D&quot;https://jira.wsgc.com/secure/viewavatar?size=3Dxsma=">TRISUL-859</im=>]() - <span class="3D&quot;summary&quot;">MG &amp; RJ Rollout - High Resolution Threshold</span> <s= pan="" class="3D&quot;aui-lozenge" aui-lozenge-subtle="" aui-lozenge-success="" jira-macro-single-issue-export-pdf"="">Closed</s=></span> </span>**
> 
> **
> <p><strong><span style="">Config Name : High Resolut=
> ion listener config</span></strong></p>
> <div class="3D&quot;table-wrap&quot;">
> <table class="3D&quot;wrapped" confluencetable"="" style="">
> <colgroup>
> <col>
> </colgroup>
> <tbody>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
> dam.core.listeners.HighResolutionImageListener</td>
> </tr>
> </tbody>
> </table>
> </div>
> <p>  
> </p>
> <p>Following custom configuration's are required for setting high resolutio=
> n threshold values for an asset.</p>
> <p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
> /configMgr)  
> Search for "<span style="">High Resol=
> ution listener config</span>" and click on it.</p>
> <p>Following are config param name and corresponding values for MG and RJ.&lt;=
> /p&gt;
> </p><div class="3D&quot;table-wrap&quot;">
> <table class="3D&quot;wrapped" confluencetable"="">
> <colgroup>
> <col>
> <col>
> </colgroup>
> <thead>
> <tr>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Param</span></p></th>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value</span></p></th>
> </tr>
> </thead>
> <tbody>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;">high.resolution.thre=
> shold</td>
> <td style="" class="3D&quot;confluenceTd&quot;"><p>/content/dam/reju=
> venation=3D2000</p><p>/content/dam/mark-and-graham=3D2000</p><p>/content/da=
> m/west-elm=3D2000</p></td>
> </tr>
> </tbody>
> </table>
> </div>
> <p class="3D&quot;auto-cursor-target&quot;"><strong>Story :</strong></p>
> <p class="3D&quot;auto-cursor-target&quot;"><strong> <span class="3D&quot;jira-issue" resolved=" data-jira-key=3D" trisul-885"=""> [![](3D"https://jira.w=)TRISUL-885](3D"https://jira.wsgc.com/browse/TRI=) - <span class="3D&quot;summary&quot;">MG Rollout - Setup G=
> roups and Permissions</span> <span class="3D&quot;aui-lozenge" aui-lozenge-subtle="aui-lozenge-success" jira-macro-single-issue-export-pdf"="">Closed</span> </span> &nbsp;</strong></p><strong>
> <p class="3D&quot;auto-cursor-target&quot;"><strong><span style="">MG Rollout - Setup Groups and Permissions</span></strong></p>
> <p class="3D&quot;auto-cursor-target&quot;"><span style=""><span= style="">ThirdPartyContributorConfig for MG DEV env=
> ironment :</span=></span></p>
> <p>  
> </p>
> <div class="3D&quot;table-wrap&quot;">
> <table class="3D&quot;wrapped" confluencetable"="" style="">
> <colgroup>
> <col>
> </colgroup>
> <tbody>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
> dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~mgtpUsers&lt;=
> /td&gt;
> </td></tr>
> </tbody>
> </table>
> </div>
> <p>  
> </p>
> <p>Following custom configuration's are required for creating&nbsp;3rd-part=
> y-group folder for MG Third Party Users in Dev environment.</p>
> <p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
> /configMgr)  
> Search for "ThirdPartyContributorConfigServiceFactory~mgtpUs=
> ers" and click on it.</p>
> <p>Following are config param names and corresponding values.</p>
> <div class="3D&quot;table-wrap&quot;">
> <table class="3D&quot;wrapped" confluencetable"="">
> <colgroup>
> <col>
> <col>
> </colgroup>
> <thead>
> <tr>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Param</span></p></th>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(Dev)</span></p></th>
> </tr>
> </thead>
> <tbody>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">brand.path</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;">/content/dam/mark-an=
> d-graham</td>
> </tr>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">third.party.folder</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
> </tr>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">third.party.groups</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;">APR_EDAM_DEV_MG_3rdP=
> artyContributor</td>
> </tr>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;">other.allowed.groups=
> </td>
> <td style="" class="3D&quot;confluenceTd&quot;">APR_EDAM_DEV_MG_Prod=
> uction</td>
> </tr>
> </tbody>
> </table>
> </div>
> <p>  
> </p>
> <p><strong>Configs for restricting metadata edit of an asset in DEV environ=
> ment :</strong></p>
> <div class="3D&quot;table-wrap&quot;">
> <table style="" class="3D&quot;confluenceTable&quot;">
> <colgroup>
> <col>
> </colgroup>
> <tbody>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
> dam.core.listeners.RestrictEditMetaData</td>
> </tr>
> </tbody>
> </table>
> </div>
> <p>  
> </p>
> <p>Following custom configuration's are required for Users to restrict edit=
>  metadata properties.</p>
> <p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
> /configMgr)  
> Search for "<span style="">RestrictEd=
> itMetaData</span>" and click on it.</p>
> <p>Following are config param name and corresponding values for MG.</p>
> <div class="3D&quot;table-wrap&quot;">
> <table class="3D&quot;confluenceTable&quot;">
> <colgroup>
> <col>
> <col>
> </colgroup>
> <thead>
> <tr>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Param</span></p></th>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(Dev)</span></p></th>
> </tr>
> </thead>
> <tbody>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">editRestrictGroups</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;"><p>APR_EDAM_DEV_MG_V=
> endor</p></td>
> </tr>
> </tbody>
> </table>
> </div>
> <p><strong>Story :</strong></p>
> <p> <span class="3D&quot;jira-issue" resolved"="" data-jira-key="3D&quot;TRISUL-886&quot;"> [<im= g="" class="3D&quot;icon&quot;" src="3D&quot;https://jira.wsgc.com/secure/viewavatar?size=3Dxsma=">TRISUL-886</im=>]() - <span class="3D&quot;summary&quot;">RJ Rollout - Setup Groups and Permissions</span> <span cl="ass=3D&quot;aui-lozenge" aui-lozenge-subtle="" aui-lozenge-success="" jira-macro-single-issue-export-pdf"="">Closed</span> </span> </p>
> <p><strong><span style="">RJ Rollout - Setup Groups =
> and Permissions</span></strong></p>
> <p class="3D&quot;auto-cursor-target&quot;"><span style=""><span= style="">ThirdPartyContributorConfig for RJ DEV env=
> ironment :</span=></span></p>
> <p>  
> </p>
> <div class="3D&quot;table-wrap&quot;">
> <table class="3D&quot;wrapped" confluencetable"="" style="">
> <colgroup>
> <col>
> </colgroup>
> <tbody>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;">com.wsgc.ecommerce.e=
> dam.core.services.impl.ThirdPartyContributorConfigServiceFactory~rjtpUsers&lt;=
> /td&gt;
> </td></tr>
> </tbody>
> </table>
> </div>
> <p>  
> </p>
> <p>Following custom configuration's are required for creating&nbsp;3rd-part=
> y-group folder for RJ Third Party Users in Dev environment.</p>
> <p>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console=
> /configMgr)  
> Search for "ThirdPartyContributorConfigServiceFactory~rjtpUs=
> ers" and click on it.</p>
> <p>Following are config param names and corresponding values.</p>
> <div class="3D&quot;table-wrap&quot;">
> <table class="3D&quot;wrapped" confluencetable"="">
> <colgroup>
> <col>
> <col>
> </colgroup>
> <thead>
> <tr>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Param</span></p></th>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(Dev)</span></p></th>
> </tr>
> </thead>
> <tbody>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">brand.path</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;">/content/dam/rejuven=
> ation</td>
> </tr>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">third.party.folder</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;">3rd-party-group</td>
> </tr>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">third.party.groups</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;">APR_EDAM_DEV_RJ_3rdP=
> artyContributor</td>
> </tr>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;">other.allowed.groups=
> </td>
> <td style="" class="3D&quot;confluenceTd&quot;">APR_EDAM_DEV_RJ_Prod=
> uction</td>
> </tr>
> </tbody>
> </table>
> </div>
> </strong>**

**<strong>
    </strong>**</div> **<strong>
&#13;&#10;&#13;&#10;&#13;&#10;</strong>**