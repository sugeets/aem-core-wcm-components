
    
# TRISUL-305 : Admin View - Customize Download Dialog with Rendition =&#13;&#10;Picker, Presets, permissions
    
<div class="3D&quot;Section1&quot;">
        
**Admin view download rendition profiles config&nbsp;(com.=
wsgc.ecommerce.edam.core.services.impl.DownloadRenditionProfileAdminViewCon=
figServiceImpl** **):**

- **Profiles Storage Path**: This is to set the configura=
    tion of&nbsp;Profile Storage Path Value.

- **Allowed Groups For Approved Assets**: This is to set&amp;nbs=
    p;Allowed Groups List Values for Approved Assets with label. Pattren would =
    be &lt;&lt;Group Label&gt;&gt;|&lt;&lt;Group Name&gt;&gt;
- **Allowed Groups For unApproved Assets**: This is to set&amp;n=
    bsp;Allowed Groups List Values for UnApproved Assets with label. Pattren wo=
    uld be &lt;&lt;Group Label&gt;&gt;|&lt;&lt;Group Name&gt;&gt;
- **ImageMagick Help Document Link**: This is to set&nbsp;Im=
    agemagick help document link
- **Output Format Options**: This is to set&nbsp;Output Form=
    at List
- **Color Profile Options**: This is to set&nbsp;Output Colo=
    r Profile List and configured with the path. Pattren would be &lt;&lt;Color=
     Profile Label&gt;&gt;|&lt;&lt;Color Profile Path&gt;&gt;

<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;relative-table" confluencetable"="" style="">
<colgroup>
<col style="">
<col style="">
<col style="">
<col style="">
<col style="">
</colgroup>
<thead>
<tr>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">&nbsp;Config Param</span></p></th>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(Dev)</span></p></th>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(QA)</span></p></th>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(UAT)</span></p></th>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(PROD)</span></p></th>
</tr>
</thead>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;">Profiles Storage Pat=
h:</td>
<td style="" class="3D&quot;confluenceTd&quot;"><p>"/etc/edam/rendit=
ion/profiles"</p></td>
<td style="" class="3D&quot;confluenceTd&quot;"><p>"/etc/edam/rendit=
ion/profiles"</p></td>
<td style="" class="3D&quot;confluenceTd&quot;"><p>"/etc/edam/rendit=
ion/profiles"</p></td>
<td style="" class="3D&quot;confluenceTd&quot;">"/etc/edam/rendition=
/profiles"</td>
</tr>
<tr>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">Allowed Groups For Approved Assets=
:</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["MG:Production|APR_EDAM_DEV_MG_Pr=
oduction", "MG:Merchants|APR_EDAM_DEV_MG_Merchants", "MG:Creative|APR_EDAM_=
DEV_MG_Creative","MG:Marketing|APR_EDAM_DEV_MG_Marketing", "MG:GeneralUsers=
|APR_EDAM_DEV_MG_GeneralUsers", "MG:3rdPartyContributor|APR_EDAM_DEV_MG_3rd=
PartyContributor", "MG:Vendor|APR_EDAM_DEV_MG_Vendor", "WS:Production|APR_E=
DAM_DEV_WS_Production", "WS:Merchants|APR_EDAM_DEV_WS_Merchants", "WS:Gener=
alUsers|APR_EDAM_DEV_WS_GeneralUsers", "WS:3rdPartyContributor|APR_EDAM_DEV=
_WS_3rdPartyContributor", "WS:Vendors|APR_EDAM_DEV_WS_Vendors", "RJ:Product=
ion|APR_EDAM_DEV_RJ_Production", "RJ:Merchants|APR_EDAM_DEV_RJ_Merchants", =
"RJ:GeneralUsers|APR_EDAM_DEV_RJ_GeneralUsers", "RJ:Marketing|APR_EDAM_DEV_=
RJ_Marketing", "RJ:DT|APR_EDAM_DEV_RJ_DT", "RJ:RT|APR_EDAM_DEV_RJ_RT", "RJ:=
ViewOnly|APR_EDAM_DEV_RJ_ViewOnly", "RJ:3rdPartyContributor|APR_EDAM_DEV_RJ=
_3rdPartyContributor", "RJ:Vendor|APR_EDAM_DEV_RJ_Vendor", "PB:Production|A=
PR_EDAM_DEV_PB_Production", "PB:Merchants|APR_EDAM_DEV_PB_Merchants", "PB:S=
eparators|APR_EDAM_DEV_PB_Separators", "PB:PRSocial|APR_EDAM_DEV_PB_PRSocia=
l", "PB:Photographers|APR_EDAM_DEV_PB_Photographers", "PB:GeneralUsers|APR_=
EDAM_DEV_PB_GeneralUsers", "PB:Franchise|APR_EDAM_DEV_PB_Franchise", "PK:Pr=
oduction|APR_EDAM_DEV_PK_Production", "PK:Merchants|APR_EDAM_DEV_PK_Merchan=
ts", "PK:Separators|APR_EDAM_DEV_PK_Separators", "PK:PRSocial|APR_EDAM_DEV_=
PK_PRSocial", "PK:Photographers|APR_EDAM_DEV_PK_Photographers", "PK:General=
Users|APR_EDAM_DEV_PK_GeneralUsers", "PK:Franchise|APR_EDAM_DEV_PK_Franchis=
e", "PT:Production|APR_EDAM_DEV_PT_Production", "PT:Merchants|APR_EDAM_DEV_=
PT_Merchants", "PT:Separators|APR_EDAM_DEV_PT_Separators", "PT:PRSocial|APR=
_EDAM_DEV_PT_PRSocial", "PT:Photographers|APR_EDAM_DEV_PT_Photographers", "=
PT:GeneralUsers|APR_EDAM_DEV_PT_GeneralUsers", "PT:Franchise|APR_EDAM_DEV_P=
T_Franchise", "WE:ReadOnly|APR_EDAM_DEV_WE_ReadOnly", "WE:Production|APR_ED=
AM_DEV_WE_Production", "WE:Merchants|APR_EDAM_DEV_WE_Merchants", "WE:Separa=
tors|APR_EDAM_DEV_WE_Separators", "WE:PRSocial|APR_EDAM_DEV_WE_PRSocial", "=
WE:Photographers|APR_EDAM_DEV_WE_Photographers", "WE:GeneralUsers|APR_EDAM_=
DEV_WE_GeneralUsers", "WE:Franchise|APR_EDAM_DEV_WE_Franchise"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["MG:Production|APR_EDAM_QA_MG_Pro=
duction", "MG:Merchants|APR_EDAM_QA_MG_Merchants", "MG:Creative|APR_EDAM_QA=
_MG_Creative", "MG:Marketing|APR_EDAM_QA_MG_Marketing", "MG:GeneralUsers|AP=
R_EDAM_QA_MG_GeneralUsers", "MG:3rdPartyContributor|APR_EDAM_QA_MG_3rdParty=
Contributor", "MG:Vendor|APR_EDAM_QA_MG_Vendor", "WS:Production|APR_EDAM_QA=
_WS_Production", "WS:Merchants|APR_EDAM_QA_WS_Merchants", "WS:GeneralUsers|=
APR_EDAM_QA_WS_GeneralUsers", "WS:3rdPartyContributor|APR_EDAM_QA_WS_3rdPar=
tyContributor", "WS:Vendors|APR_EDAM_QA_WS_Vendors", "RJ:Production|APR_EDA=
M_QA_RJ_Production", "RJ:Merchants|APR_EDAM_QA_RJ_Merchants", "RJ:GeneralUs=
ers|APR_EDAM_QA_RJ_GeneralUsers", "RJ:Marketing|APR_EDAM_QA_RJ_Marketing", =
"RJ:DT|APR_EDAM_QA_RJ_DT", "RJ:RT|APR_EDAM_QA_RJ_RT", "RJ:ViewOnly|APR_EDAM=
_QA_RJ_ViewOnly", "RJ:3rdPartyContributor|APR_EDAM_QA_RJ_3rdPartyContributo=
r", "RJ:Vendor|APR_EDAM_QA_RJ_Vendor", "PB:Production|APR_EDAM_QA_PB_Produc=
tion", "PB:Merchants|APR_EDAM_QA_PB_Merchants", "PB:Separators|APR_EDAM_QA_=
PB_Separators", "PB:PRSocial|APR_EDAM_QA_PB_PRSocial", "PB:Photographers|AP=
R_EDAM_QA_PB_Photographers", "PB:GeneralUsers|APR_EDAM_QA_PB_GeneralUsers",=
 "PB:Franchise|APR_EDAM_QA_PB_Franchise", "PK:Production|APR_EDAM_QA_PK_Pro=
duction", "PK:Merchants|APR_EDAM_QA_PK_Merchants", "PK:Separators|APR_EDAM_=
QA_PK_Separators", "PK:PRSocial|APR_EDAM_QA_PK_PRSocial", "PK:Photographers=
|APR_EDAM_QA_PK_Photographers", "PK:GeneralUsers|APR_EDAM_QA_PK_GeneralUser=
s", "PK:Franchise|APR_EDAM_QA_PK_Franchise", "PT:Production|APR_EDAM_QA_PT_=
Production", "PT:Merchants|APR_EDAM_QA_PT_Merchants", "PT:Separators|APR_ED=
AM_QA_PT_Separators", "PT:PRSocial|APR_EDAM_QA_PT_PRSocial", "PT:Photograph=
ers|APR_EDAM_QA_PT_Photographers", "PT:GeneralUsers|APR_EDAM_QA_PT_GeneralU=
sers", "PT:Franchise|APR_EDAM_QA_PT_Franchise", "WE:ReadOnly|APR_EDAM_QA_WE=
_ReadOnly", "WE:Production|APR_EDAM_QA_WE_Production", "WE:Merchants|APR_ED=
AM_QA_WE_Merchants", "WE:Separators|APR_EDAM_QA_WE_Separators", "WE:PRSocia=
l|APR_EDAM_QA_WE_PRSocial", "WE:Photographers|APR_EDAM_QA_WE_Photographers"=
, "WE:GeneralUsers|APR_EDAM_QA_WE_GeneralUsers", "WE:Franchise|APR_EDAM_QA_=
WE_Franchise"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["MG:Production|APR_EDAM_UAT_MG_Pr=
oduction", "MG:Merchants|APR_EDAM_UAT_MG_Merchants", "MG:Creative|APR_EDAM_=
UAT_MG_Creative", "MG:Marketing|APR_EDAM_UAT_MG_Marketing", "MG:GeneralUser=
s|APR_EDAM_UAT_MG_GeneralUsers", "MG:3rdPartyContributor|APR_EDAM_UAT_MG_3r=
dPartyContributor", "MG:Vendor|APR_EDAM_UAT_MG_Vendor", "WS:Production|APR_=
EDAM_UAT_WS_Production", "WS:Merchants|APR_EDAM_UAT_WS_Merchants", "WS:Gene=
ralUsers|APR_EDAM_UAT_WS_GeneralUsers", "WS:3rdPartyContributor|APR_EDAM_UA=
T_WS_3rdPartyContributor", "WS:Vendors|APR_EDAM_UAT_WS_Vendors", "RJ:Produc=
tion|APR_EDAM_UAT_RJ_Production", "RJ:Merchants|APR_EDAM_UAT_RJ_Merchants",=
 "RJ:GeneralUsers|APR_EDAM_UAT_RJ_GeneralUsers", "RJ:Marketing|APR_EDAM_UAT=
_RJ_Marketing", "RJ:DT|APR_EDAM_UAT_RJ_DT", "RJ:RT|APR_EDAM_UAT_RJ_RT", "RJ=
:ViewOnly|APR_EDAM_UAT_RJ_ViewOnly", "RJ:3rdPartyContributor|APR_EDAM_UAT_R=
J_3rdPartyContributor", "RJ:Vendor|APR_EDAM_UAT_RJ_Vendor", "PB:Production|=
APR_EDAM_UAT_PB_Production", "PB:Merchants|APR_EDAM_UAT_PB_Merchants", "PB:=
Separators|APR_EDAM_UAT_PB_Separators", "PB:PRSocial|APR_EDAM_UAT_PB_PRSoci=
al", "PB:Photographers|APR_EDAM_UAT_PB_Photographers", "PB:GeneralUsers|APR=
_EDAM_UAT_PB_GeneralUsers", "PB:Franchise|APR_EDAM_UAT_PB_Franchise", "PK:P=
roduction|APR_EDAM_UAT_PK_Production", "PK:Merchants|APR_EDAM_UAT_PK_Mercha=
nts", "PK:Separators|APR_EDAM_UAT_PK_Separators", "PK:PRSocial|APR_EDAM_UAT=
_PK_PRSocial", "PK:Photographers|APR_EDAM_UAT_PK_Photographers", "PK:Genera=
lUsers|APR_EDAM_UAT_PK_GeneralUsers", "PK:Franchise|APR_EDAM_UAT_PK_Franchi=
se", "PT:Production|APR_EDAM_UAT_PT_Production", "PT:Merchants|APR_EDAM_UAT=
_PT_Merchants", "PT:Separators|APR_EDAM_UAT_PT_Separators", "PT:PRSocial|AP=
R_EDAM_UAT_PT_PRSocial", "PT:Photographers|APR_EDAM_UAT_PT_Photographers", =
"PT:GeneralUsers|APR_EDAM_UAT_PT_GeneralUsers", "PT:Franchise|APR_EDAM_UAT_=
PT_Franchise", "WE:ReadOnly|APR_EDAM_UAT_WE_ReadOnly", "WE:Production|APR_E=
DAM_UAT_WE_Production", "WE:Merchants|APR_EDAM_UAT_WE_Merchants", "WE:Separ=
ators|APR_EDAM_UAT_WE_Separators", "WE:PRSocial|APR_EDAM_UAT_WE_PRSocial", =
"WE:Photographers|APR_EDAM_UAT_WE_Photographers", "WE:GeneralUsers|APR_EDAM=
_UAT_WE_GeneralUsers", "WE:Franchise|APR_EDAM_UAT_WE_Franchise"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["MG:Production|APR_EDAMMG_Product=
ion", "MG:Merchants|APR_EDAMMG_Merchants", "MG:Creative|APR_EDAMMG_Creative=
", "MG:Marketing|APR_EDAMMG_Marketing", "MG:GeneralUsers|APR_EDAMMG_General=
Users", "MG:3rdPartyContributor|APR_EDAMMG_3rdPartyContributor", "MG:Vendor=
|APR_EDAMMG_Vendor", "WS:Production|APR_EDAMWS_Production", "WS:Merchants|A=
PR_EDAMWS_Merchants", "WS:GeneralUsers|APR_EDAMWS_GeneralUsers", "WS:3rdPar=
tyContributor|APR_EDAMWS_3rdPartyContributor", "WS:Vendors|APR_EDAMWS_Vendo=
rs", "RJ:Production|APR_EDAMRJ_Production", "RJ:Merchants|APR_EDAMRJ_Mercha=
nts", "RJ:GeneralUsers|APR_EDAMRJ_GeneralUsers", "RJ:Marketing|APR_EDAMRJ_M=
arketing", "RJ:DT|APR_EDAMRJ_DT", "RJ:RT|APR_EDAMRJ_RT", "RJ:ViewOnly|APR_E=
DAMRJ_ViewOnly", "RJ:3rdPartyContributor|APR_EDAMRJ_3rdPartyContributor", "=
RJ:Vendor|APR_EDAMRJ_Vendor", "PB:Production|APR_EDAMPB_Production", "PB:Me=
rchants|APR_EDAMPB_Merchants", "PB:Separators|APR_EDAMPB_Separators", "PB:P=
RSocial|APR_EDAMPB_PRSocial", "PB:Photographers|APR_EDAMPB_Photographers", =
"PB:GeneralUsers|APR_EDAMPB_GeneralUsers", "PB:Franchise|APR_EDAMPB_Franchi=
se", "PK:Production|APR_EDAMPK_Production", "PK:Merchants|APR_EDAMPK_Mercha=
nts", "PK:Separators|APR_EDAMPK_Separators", "PK:PRSocial|APR_EDAMPK_PRSoci=
al", "PK:Photographers|APR_EDAMPK_Photographers", "PK:GeneralUsers|APR_EDAM=
PK_GeneralUsers", "PK:Franchise|APR_EDAMPK_Franchise", "PT:Production|APR_E=
DAMPT_Production", "PT:Merchants|APR_EDAMPT_Merchants", "PT:Separators|APR_=
EDAMPT_Separators", "PT:PRSocial|APR_EDAMPT_PRSocial", "PT:Photographers|AP=
R_EDAMPT_Photographers", "PT:GeneralUsers|APR_EDAMPT_GeneralUsers", "PT:Fra=
nchise|APR_EDAMPT_Franchise", "WE:ReadOnly|APR_EDAMWE_ReadOnly", "WE:Produc=
tion|APR_EDAMWE_Production", "WE:Merchants|APR_EDAMWE_Merchants", "WE:Separ=
ators|APR_EDAMWE_Separators", "WE:PRSocial|APR_EDAMWE_PRSocial", "WE:Photog=
raphers|APR_EDAMWE_Photographers", "WE:GeneralUsers|APR_EDAMWE_GeneralUsers=
", "WE:Franchise|APR_EDAMWE_Franchise"]</td>
</tr>
<tr>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">Allowed Groups For unApproved Asse=
ts:</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["MG:Production|APR_EDAM_DEV_MG_Pr=
oduction", "MG:Merchants|APR_EDAM_DEV_MG_Merchants", "MG:Creative|APR_EDAM_=
DEV_MG_Creative","MG:Marketing|APR_EDAM_DEV_MG_Marketing", "MG:GeneralUsers=
|APR_EDAM_DEV_MG_GeneralUsers", "MG:3rdPartyContributor|APR_EDAM_DEV_MG_3rd=
PartyContributor", "MG:Vendor|APR_EDAM_DEV_MG_Vendor", "WS:Production|APR_E=
DAM_DEV_WS_Production", "WS:Merchants|APR_EDAM_DEV_WS_Merchants", "WS:Gener=
alUsers|APR_EDAM_DEV_WS_GeneralUsers", "WS:3rdPartyContributor|APR_EDAM_DEV=
_WS_3rdPartyContributor", "WS:Vendors|APR_EDAM_DEV_WS_Vendors", "RJ:Product=
ion|APR_EDAM_DEV_RJ_Production", "RJ:Merchants|APR_EDAM_DEV_RJ_Merchants", =
"RJ:GeneralUsers|APR_EDAM_DEV_RJ_GeneralUsers", "RJ:Marketing|APR_EDAM_DEV_=
RJ_Marketing", "RJ:DT|APR_EDAM_DEV_RJ_DT", "RJ:RT|APR_EDAM_DEV_RJ_RT", "RJ:=
ViewOnly|APR_EDAM_DEV_RJ_ViewOnly", "RJ:3rdPartyContributor|APR_EDAM_DEV_RJ=
_3rdPartyContributor", "RJ:Vendor|APR_EDAM_DEV_RJ_Vendor", "PB:Production|A=
PR_EDAM_DEV_PB_Production", "PB:Merchants|APR_EDAM_DEV_PB_Merchants", "PB:S=
eparators|APR_EDAM_DEV_PB_Separators", "PB:PRSocial|APR_EDAM_DEV_PB_PRSocia=
l", "PB:Photographers|APR_EDAM_DEV_PB_Photographers", "PB:GeneralUsers|APR_=
EDAM_DEV_PB_GeneralUsers", "PB:Franchise|APR_EDAM_DEV_PB_Franchise", "PK:Pr=
oduction|APR_EDAM_DEV_PK_Production", "PK:Merchants|APR_EDAM_DEV_PK_Merchan=
ts", "PK:Separators|APR_EDAM_DEV_PK_Separators", "PK:PRSocial|APR_EDAM_DEV_=
PK_PRSocial", "PK:Photographers|APR_EDAM_DEV_PK_Photographers", "PK:General=
Users|APR_EDAM_DEV_PK_GeneralUsers", "PK:Franchise|APR_EDAM_DEV_PK_Franchis=
e", "PT:Production|APR_EDAM_DEV_PT_Production", "PT:Merchants|APR_EDAM_DEV_=
PT_Merchants", "PT:Separators|APR_EDAM_DEV_PT_Separators", "PT:PRSocial|APR=
_EDAM_DEV_PT_PRSocial", "PT:Photographers|APR_EDAM_DEV_PT_Photographers", "=
PT:GeneralUsers|APR_EDAM_DEV_PT_GeneralUsers", "PT:Franchise|APR_EDAM_DEV_P=
T_Franchise", "WE:ReadOnly|APR_EDAM_DEV_WE_ReadOnly", "WE:Production|APR_ED=
AM_DEV_WE_Production", "WE:Merchants|APR_EDAM_DEV_WE_Merchants", "WE:Separa=
tors|APR_EDAM_DEV_WE_Separators", "WE:PRSocial|APR_EDAM_DEV_WE_PRSocial", "=
WE:Photographers|APR_EDAM_DEV_WE_Photographers", "WE:GeneralUsers|APR_EDAM_=
DEV_WE_GeneralUsers", "WE:Franchise|APR_EDAM_DEV_WE_Franchise"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["MG:Production|APR_EDAM_QA_MG_Pro=
duction", "MG:Merchants|APR_EDAM_QA_MG_Merchants", "MG:Creative|APR_EDAM_QA=
_MG_Creative", "MG:Marketing|APR_EDAM_QA_MG_Marketing", "MG:GeneralUsers|AP=
R_EDAM_QA_MG_GeneralUsers", "MG:3rdPartyContributor|APR_EDAM_QA_MG_3rdParty=
Contributor", "MG:Vendor|APR_EDAM_QA_MG_Vendor", "WS:Production|APR_EDAM_QA=
_WS_Production", "WS:Merchants|APR_EDAM_QA_WS_Merchants", "WS:GeneralUsers|=
APR_EDAM_QA_WS_GeneralUsers", "WS:3rdPartyContributor|APR_EDAM_QA_WS_3rdPar=
tyContributor", "WS:Vendors|APR_EDAM_QA_WS_Vendors", "RJ:Production|APR_EDA=
M_QA_RJ_Production", "RJ:Merchants|APR_EDAM_QA_RJ_Merchants", "RJ:GeneralUs=
ers|APR_EDAM_QA_RJ_GeneralUsers", "RJ:Marketing|APR_EDAM_QA_RJ_Marketing", =
"RJ:DT|APR_EDAM_QA_RJ_DT", "RJ:RT|APR_EDAM_QA_RJ_RT", "RJ:ViewOnly|APR_EDAM=
_QA_RJ_ViewOnly", "RJ:3rdPartyContributor|APR_EDAM_QA_RJ_3rdPartyContributo=
r", "RJ:Vendor|APR_EDAM_QA_RJ_Vendor", "PB:Production|APR_EDAM_QA_PB_Produc=
tion", "PB:Merchants|APR_EDAM_QA_PB_Merchants", "PB:Separators|APR_EDAM_QA_=
PB_Separators", "PB:PRSocial|APR_EDAM_QA_PB_PRSocial", "PB:Photographers|AP=
R_EDAM_QA_PB_Photographers", "PB:GeneralUsers|APR_EDAM_QA_PB_GeneralUsers",=
 "PB:Franchise|APR_EDAM_QA_PB_Franchise", "PK:Production|APR_EDAM_QA_PK_Pro=
duction", "PK:Merchants|APR_EDAM_QA_PK_Merchants", "PK:Separators|APR_EDAM_=
QA_PK_Separators", "PK:PRSocial|APR_EDAM_QA_PK_PRSocial", "PK:Photographers=
|APR_EDAM_QA_PK_Photographers", "PK:GeneralUsers|APR_EDAM_QA_PK_GeneralUser=
s", "PK:Franchise|APR_EDAM_QA_PK_Franchise", "PT:Production|APR_EDAM_QA_PT_=
Production", "PT:Merchants|APR_EDAM_QA_PT_Merchants", "PT:Separators|APR_ED=
AM_QA_PT_Separators", "PT:PRSocial|APR_EDAM_QA_PT_PRSocial", "PT:Photograph=
ers|APR_EDAM_QA_PT_Photographers", "PT:GeneralUsers|APR_EDAM_QA_PT_GeneralU=
sers", "PT:Franchise|APR_EDAM_QA_PT_Franchise", "WE:ReadOnly|APR_EDAM_QA_WE=
_ReadOnly", "WE:Production|APR_EDAM_QA_WE_Production", "WE:Merchants|APR_ED=
AM_QA_WE_Merchants", "WE:Separators|APR_EDAM_QA_WE_Separators", "WE:PRSocia=
l|APR_EDAM_QA_WE_PRSocial", "WE:Photographers|APR_EDAM_QA_WE_Photographers"=
, "WE:GeneralUsers|APR_EDAM_QA_WE_GeneralUsers", "WE:Franchise|APR_EDAM_QA_=
WE_Franchise"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["MG:Production|APR_EDAM_UAT_MG_Pr=
oduction", "MG:Merchants|APR_EDAM_UAT_MG_Merchants", "MG:Creative|APR_EDAM_=
UAT_MG_Creative", "MG:Marketing|APR_EDAM_UAT_MG_Marketing", "MG:GeneralUser=
s|APR_EDAM_UAT_MG_GeneralUsers", "MG:3rdPartyContributor|APR_EDAM_UAT_MG_3r=
dPartyContributor", "MG:Vendor|APR_EDAM_UAT_MG_Vendor", "WS:Production|APR_=
EDAM_UAT_WS_Production", "WS:Merchants|APR_EDAM_UAT_WS_Merchants", "WS:Gene=
ralUsers|APR_EDAM_UAT_WS_GeneralUsers", "WS:3rdPartyContributor|APR_EDAM_UA=
T_WS_3rdPartyContributor", "WS:Vendors|APR_EDAM_UAT_WS_Vendors", "RJ:Produc=
tion|APR_EDAM_UAT_RJ_Production", "RJ:Merchants|APR_EDAM_UAT_RJ_Merchants",=
 "RJ:GeneralUsers|APR_EDAM_UAT_RJ_GeneralUsers", "RJ:Marketing|APR_EDAM_UAT=
_RJ_Marketing", "RJ:DT|APR_EDAM_UAT_RJ_DT", "RJ:RT|APR_EDAM_UAT_RJ_RT", "RJ=
:ViewOnly|APR_EDAM_UAT_RJ_ViewOnly", "RJ:3rdPartyContributor|APR_EDAM_UAT_R=
J_3rdPartyContributor", "RJ:Vendor|APR_EDAM_UAT_RJ_Vendor", "PB:Production|=
APR_EDAM_UAT_PB_Production", "PB:Merchants|APR_EDAM_UAT_PB_Merchants", "PB:=
Separators|APR_EDAM_UAT_PB_Separators", "PB:PRSocial|APR_EDAM_UAT_PB_PRSoci=
al", "PB:Photographers|APR_EDAM_UAT_PB_Photographers", "PB:GeneralUsers|APR=
_EDAM_UAT_PB_GeneralUsers", "PB:Franchise|APR_EDAM_UAT_PB_Franchise", "PK:P=
roduction|APR_EDAM_UAT_PK_Production", "PK:Merchants|APR_EDAM_UAT_PK_Mercha=
nts", "PK:Separators|APR_EDAM_UAT_PK_Separators", "PK:PRSocial|APR_EDAM_UAT=
_PK_PRSocial", "PK:Photographers|APR_EDAM_UAT_PK_Photographers", "PK:Genera=
lUsers|APR_EDAM_UAT_PK_GeneralUsers", "PK:Franchise|APR_EDAM_UAT_PK_Franchi=
se", "PT:Production|APR_EDAM_UAT_PT_Production", "PT:Merchants|APR_EDAM_UAT=
_PT_Merchants", "PT:Separators|APR_EDAM_UAT_PT_Separators", "PT:PRSocial|AP=
R_EDAM_UAT_PT_PRSocial", "PT:Photographers|APR_EDAM_UAT_PT_Photographers", =
"PT:GeneralUsers|APR_EDAM_UAT_PT_GeneralUsers", "PT:Franchise|APR_EDAM_UAT_=
PT_Franchise", "WE:ReadOnly|APR_EDAM_UAT_WE_ReadOnly", "WE:Production|APR_E=
DAM_UAT_WE_Production", "WE:Merchants|APR_EDAM_UAT_WE_Merchants", "WE:Separ=
ators|APR_EDAM_UAT_WE_Separators", "WE:PRSocial|APR_EDAM_UAT_WE_PRSocial", =
"WE:Photographers|APR_EDAM_UAT_WE_Photographers", "WE:GeneralUsers|APR_EDAM=
_UAT_WE_GeneralUsers", "WE:Franchise|APR_EDAM_UAT_WE_Franchise"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["MG:Production|APR_EDAMMG_Product=
ion", "MG:Merchants|APR_EDAMMG_Merchants", "MG:Creative|APR_EDAMMG_Creative=
", "MG:Marketing|APR_EDAMMG_Marketing", "MG:GeneralUsers|APR_EDAMMG_General=
Users", "MG:3rdPartyContributor|APR_EDAMMG_3rdPartyContributor", "MG:Vendor=
|APR_EDAMMG_Vendor", "WS:Production|APR_EDAMWS_Production", "WS:Merchants|A=
PR_EDAMWS_Merchants", "WS:GeneralUsers|APR_EDAMWS_GeneralUsers", "WS:3rdPar=
tyContributor|APR_EDAMWS_3rdPartyContributor", "WS:Vendors|APR_EDAMWS_Vendo=
rs", "RJ:Production|APR_EDAMRJ_Production", "RJ:Merchants|APR_EDAMRJ_Mercha=
nts", "RJ:GeneralUsers|APR_EDAMRJ_GeneralUsers", "RJ:Marketing|APR_EDAMRJ_M=
arketing", "RJ:DT|APR_EDAMRJ_DT", "RJ:RT|APR_EDAMRJ_RT", "RJ:ViewOnly|APR_E=
DAMRJ_ViewOnly", "RJ:3rdPartyContributor|APR_EDAMRJ_3rdPartyContributor", "=
RJ:Vendor|APR_EDAMRJ_Vendor", "PB:Production|APR_EDAMPB_Production", "PB:Me=
rchants|APR_EDAMPB_Merchants", "PB:Separators|APR_EDAMPB_Separators", "PB:P=
RSocial|APR_EDAMPB_PRSocial", "PB:Photographers|APR_EDAMPB_Photographers", =
"PB:GeneralUsers|APR_EDAMPB_GeneralUsers", "PB:Franchise|APR_EDAMPB_Franchi=
se", "PK:Production|APR_EDAMPK_Production", "PK:Merchants|APR_EDAMPK_Mercha=
nts", "PK:Separators|APR_EDAMPK_Separators", "PK:PRSocial|APR_EDAMPK_PRSoci=
al", "PK:Photographers|APR_EDAMPK_Photographers", "PK:GeneralUsers|APR_EDAM=
PK_GeneralUsers", "PK:Franchise|APR_EDAMPK_Franchise", "PT:Production|APR_E=
DAMPT_Production", "PT:Merchants|APR_EDAMPT_Merchants", "PT:Separators|APR_=
EDAMPT_Separators", "PT:PRSocial|APR_EDAMPT_PRSocial", "PT:Photographers|AP=
R_EDAMPT_Photographers", "PT:GeneralUsers|APR_EDAMPT_GeneralUsers", "PT:Fra=
nchise|APR_EDAMPT_Franchise", "WE:ReadOnly|APR_EDAMWE_ReadOnly", "WE:Produc=
tion|APR_EDAMWE_Production", "WE:Merchants|APR_EDAMWE_Merchants", "WE:Separ=
ators|APR_EDAMWE_Separators", "WE:PRSocial|APR_EDAMWE_PRSocial", "WE:Photog=
raphers|APR_EDAMWE_Photographers", "WE:GeneralUsers|APR_EDAMWE_GeneralUsers=
", "WE:Franchise|APR_EDAMWE_Franchise"]</td>
</tr>
<tr>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">ImageMagick Help Document Link:
</td><td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">"<a href="3D&quot;https://imagemagick.or=" g="" script="" command-line-tools.php"="" class="3D&quot;external-link&quot;" rel="3D&quot;nofollow&quot;">h=
ttps://imagemagick.org/script/command-line-tools.php</a>"</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">"<a href="3D&quot;https://imagemagick.or=" g="" script="" command-line-tools.php"="" class="3D&quot;external-link&quot;" rel="3D&quot;nofollow&quot;">h=
ttps://imagemagick.org/script/command-line-tools.php</a>"</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">"<a href="3D&quot;https://imagemagick.or=" g="" script="" command-line-tools.php"="" class="3D&quot;external-link&quot;" rel="3D&quot;nofollow&quot;">h=
ttps://imagemagick.org/script/command-line-tools.php</a>"</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">"<a href="3D&quot;https://imagemagick.or=" g="" script="" command-line-tools.php"="" class="3D&quot;external-link&quot;" rel="3D&quot;nofollow&quot;">h=
ttps://imagemagick.org/script/command-line-tools.php</a>"</td>
</tr>
<tr>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">Output Format Options:</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["JPEG"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["JPEG"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["JPEG"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["JPEG"]</td>
</tr>
<tr>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">Color Profile Options:</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["ICC\ 2014|/etc/ImageMagick-6/sRG=
B2014.icc"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["ICC\ 2014|/etc/ImageMagick-6/sRG=
B2014.icc"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["ICC\ 2014|/etc/ImageMagick-6/sRG=
B2014.icc"]</td>
<td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">["ICC\ 2014|/etc/ImageMagick-6/sRG=
B2014.icc"]</td>
</tr>
</tbody>
</table>
</div>
    </div>



