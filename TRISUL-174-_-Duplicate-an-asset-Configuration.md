
    
# TRISUL-174 : Duplicate an asset - Configuration
    
<div class="3D&quot;Section1&quot;">
        
<span style="">**Duplicate button access configuration&nbsp;(com.wsgc.ecommerce.edam.core.services.impl.DuplicateButtonAccessConfigServiceImpl** **):**</span>

- <span style="">This custom&nbsp;Duplicate button access configuration contains a duplicate button viewer brand names and user groups.</span>
- <span style="">Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)</span>
- <span style="">Search for "Duplicate button access configuration" and click on it.</span>
- <span style="">Following are config param descriptions for&nbsp;Duplicate button access configuration &nbsp;-</span>  
    <span style="">brandAndUserGroupNames&nbsp;contain a list of duplicate button viewer&nbsp;brand name and&nbsp;user groups.  
    
    <span style="">buttonLabel contains a duplicate button label.</span></span>

<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;relative-table"  style="">
<colgroup>
<col style="">
<col style="">
<col style="">
<col style="">
<col style="">
</colgroup>
<thead>
<tr>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" >&nbsp;Config Param</span></p></th>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" >Config Value(Dev)</span></p></th>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" >Config Value(QA)</span></p></th>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" >Config Value(UAT)</span></p></th>
<th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" >Config Value(PROD)</span></p></th>
</tr>
</thead>
<tbody>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;"><span style=""><span style="">brandAndUserGroupNames</span></span></td>
<td style="" class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=</p><p>APR_EDAM_DEV_Admins,</p><p>APR_EDAM_DEV_WE_PRODUCTION</p>
</td><td style="" class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=</p><p>APR_EDAM_QA_Admins,</p><p>APR_EDAM_QA_WE_PRODUCTION</p></td>
<td style="" class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=</p><p>APR_EDAM_UAT_Admins,</p><p>APR_EDAM_UAT_WE_PRODUCTION</p>
</td><td style="" class="3D&quot;confluenceTd&quot;"><p>/content/dam/west-elm=</p><p>APR_EDAM_WE_ADMINS,</p><p>APR_EDAM_WE_PRODUCTION</p></td>
</tr>
<tr>
<td style="" class="3D&quot;confluenceTd&quot;"><span style=""><span style="">buttonLabel</span></span></td>
<td style="" class="3D&quot;confluenceTd&quot;"><p>Duplicate</p>
</td><td style="" class="3D&quot;confluenceTd&quot;"><p>Duplicate</p></td>
<td style="" class="3D&quot;confluenceTd&quot;"><p>Duplicate</p>
</td><td style="" class="3D&quot;confluenceTd&quot;"><p>Duplicate</p></td>
</tr>

</tbody>
</table>
</div>
    </div>


