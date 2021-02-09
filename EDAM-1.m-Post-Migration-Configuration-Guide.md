
    
# EDAM 1.m - Post Migration - Configuration Guide
    
<div class="3D&quot;Section1&quot;">
        
<span style=""><u>**TRISUL-377 -=
WS DAM - Post-Migration Workflow Process&nbsp;**</u></span>

<span style="">**WS Legacy Asset Migtati=
on Utility Configuration - com.wsgc.ecommerce.edam.core.processors.WsiLegac=
yToEdamPostProcessor** **:**</span>

- <span style="">This custom configuration cont=
    ains&nbsp;WS Legacy Asset Migtation Utility Configuration mapping for Legac=
    y DAM assets metadata properties to EDAM assets metadata properties  
    </span>
- <span style="">Navigate to AEM web console (i=
    .e. [hostname]:[portnumber]/system/console/configMgr)</span>
- <span style="">Search for "**WS Legacy =
    Asset Migtation Utility Configuration**" and click on it.</span>
- <span style="">Following is config param d=
    escriptions for&nbsp;**com.wsgc.ecommerce.edam.core.processors.WsiLeg=
    acyToEdamPostProcessor**&nbsp; -</span>

<span style="">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&amp;=
nbsp;&nbsp;&nbsp;&nbsp; **metadataMappingConfigJson** -&nbsp; =
contains a list of mappings of metadata properties of Legacy DAM assets to =
EDAM metadata properties.&nbsp;&nbsp;&nbsp;&nbsp;</span>

<span style="">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&amp;=
nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span style="">F</span><span style=""><span style="" r="gb(122,134,154);&quot;">ollowing is the value that needs to be configured :</span></span>
<pre>[<br>{<br>"inputMeta": "wsm:Year",<br>"inputType": "String",<br>"outpu=
tMeta": "wsi:year",<br>"outputType": "String",<br>"outputMulti": "no",<br>"=
defaultValue":""<br>},<br>{<br>"inputMeta": "wsm:Season",<br>"inputType": "=
String",<br>"outputMeta": "wsi:season",<br>"outputType": "String",<br>"outp=
utMulti": "no",<br>"defaultValue":""<br>},<br>{<br>"inputMeta": "wsm:Channe=
l",<br>"inputType": "String",<br>"outputMeta": "wsi:channels",<br>"outputTy=
pe": "String",<br>"outputMulti": "yes",<br>"defaultValue":""<br>},<br>{<br>=
"inputMeta": "wsm:ImageRole",<br>"inputType": "String",<br>"outputMeta": "w=
si:asset-type",<br>"outputType": "String",<br>"outputMulti": "no",<br>"defa=
ultValue":""<br>},<br>{<br>"inputMeta": "dc:description",<br>"inputType": "=
String",<br>"outputMeta": "wsi:iptcDescription",<br>"outputType": "String",=
<br>"outputMulti": "no",<br>"defaultValue":""<br>},<br>{<br>"inputMeta": "d=
c:subject",<br>"inputType": "String",<br>"outputMeta": "dc:subject",<br>"ou=
tputType": "String",<br>"outputMulti": "yes",<br>"defaultValue":""<br>},<br=>{<br>"inputMeta": "wsm:Skus",<br>"inputType": "String",<br>"outputMeta": "=
wsi:skus",<br>"outputType": "String",<br>"outputMulti": "yes",<br>"defaultV=
alue":""<br>},<br>{<br>"inputMeta": "wsm:Spread",<br>"inputType": "String",=
<br>"outputMeta": "wsi:spread",<br>"outputType": "String",<br>"outputMulti"=
: "no",<br>"defaultValue":""<br>},<br>{<br>"inputMeta": "wsm:Approved",<br>=
"inputType": "String",<br>"outputMeta": "wsi:status",<br>"outputType": "Str=
ing",<br>"outputMulti": "no",<br>"defaultValue":"approved"<br>},<br>{<br>"i=
nputMeta": "wsm:state",<br>"inputType": "String",<br>"outputMeta": "wsi:wor=
kflow-status",<br>"outputType": "String",<br>"outputMulti": "no",<br>"defau=
ltValue":""<br>},<br>{<br>"inputMeta": "wsm:Model",<br>"inputType": "String=
",<br>"outputMeta": "wsi:model",<br>"outputType": "String",<br>"outputMulti=
": "yes",<br>"defaultValue":""<br>},<br>{<br>"inputMeta": "dc:creator",<br>=
"inputType": "String",<br>"outputMeta": "wsi:photographer",<br>"outputType"=
: "String",<br>"outputMulti": "yes",<br>"defaultValue":""<br>},<br>{<br>"in=
putMeta": "wsm:digitechname",<br>"inputType": "String",<br>"outputMeta": "w=
si:digital-tech",<br>"outputType": "String",<br>"outputMulti": "yes",<br>"d=
efaultValue":""<br>},<br>{<br>"inputMeta": "photoshop:City",<br>"inputType"=
: "String",<br>"outputMeta": "wsi:location",<br>"outputType": "String",<br>=
"outputMulti": "no",<br>"defaultValue":""<br>},<br>{<br>"inputMeta": "xmp:C=
reateDate",<br>"inputType": "Date",<br>"outputMeta": "photoshop:DateCreated=
",<br>"outputType": "Date",<br>"outputMulti": "no",<br>"defaultValue":""<br=>}<br>]</br=></br=></pre>
<span style="">**Above configuration is =
the common configuration which is same across all the environments.**</span>

****</div> **&#13;&#10;&#13;&#10;&#13;&#10;**