# TRISUL-176 : Reporting - export metadata based on search results&#13;&#10;
<div class="Section1">
   &#13;&#10;        
   <p>**Metadata based on user asset search export properties config&nbsp;(com.wsgc.ecommerce.edam.core.service.config.ExportMetaDataConfig&#13;&#10;****).**</p>
   &#13;&#10;
   <p><br></p>
   &#13;&#10;
   <ul>
      &#13;&#10;
      <li>This custom export metadata based on user search results, configuration contains Metadata property names and export file name and sheet name.</li>
      &#13;&#10;
      <li>Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)</li>
      &#13;&#10;
      <li>Search for "Configuration for Metadata Exporter" and click on it.</li>
      &#13;&#10;
      <li>Provide "<span style="">File Name</span>" and "Sheet Name" and&nbsp;<span style="">multiple properties click on the + icon and add.</span></li>
      &#13;&#10;
      <li>
         <p>Following are config param descriptions -<br>"Metadata properties to export"&nbsp; contains path and property names.<br><span style="">Example:&nbsp;<span style="">Brand Path = property path from asset. Provide multiple properties =&#13;&#10;with comma.</span></span><span style="">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; </span></p>
      </li>
      &#13;&#10;
      <li><span style="">&nbsp;/content/dam/west-elm=<span style="">jcr:content/metadata/dc:title,</span><span style=""><span>&nbsp;</span>jcr:content/metadata/dam:size</span></span></li>
      &#13;&#10;
      <li><span style="">/content/dam/potterybarn=</span><span style="">jcr:content/metadata/dc:title,</span><span style="">&nbsp;jcr:content/metadata/dam:size</span></li>
      &#13;&#10;
   </ul>
   &#13;&#10;
   <div >
      &#13;&#10;
      <table class="3D&quot;relative-table" style="">
         &#13;&#10;
         <colgroup>
            &#13;&#10;
            <col style="">
            &#13;&#10;
            <col style="">
            &#13;&#10;
            <col style="">
            &#13;&#10;
            <col style="">
            &#13;&#10;
            <col style="">
            &#13;&#10;
            <col style="">
            &#13;&#10;
            <col style="">
            &#13;&#10;
         </colgroup>
         &#13;&#10;
         <thead>
            &#13;&#10;
            <tr>
               &#13;&#10;
               <th style="" class="3D&quot;confluenceTh&quot;">
                  <p><span style="" >&nbsp;Config Param</span></p>
               </th>
               &#13;&#10;
               <th style="" class="3D&quot;confluenceTh&quot;">
                  <p><span style="" >Config Value(Dev)</span></p>
               </th>
               &#13;&#10;
               <th style="" class="3D&quot;confluenceTh&quot;">
                  <p><span style="" >Config Value(QA)</span></p>
               </th>
               &#13;&#10;
               <th style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTh&quot;">
                  <p><span style="">Config Value(RGS)</span></p>
               </th>
               &#13;&#10;
               <th style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTh&quot;">
                  <p><span style="">Config Value(PERF)</span></p>
               </th>
               &#13;&#10;
               <th style="" class="3D&quot;confluenceTh&quot;">
                  <p><span style="" >Config Value(UAT)</span></p>
               </th>
               &#13;&#10;
               <th style="" class="3D&quot;confluenceTh&quot;">
                  <p><span style="" >Config Value(PROD)</span></p>
               </th>
               &#13;&#10;
            </tr>
            &#13;&#10;
         </thead>
         &#13;&#10;
         <tbody>
            &#13;&#10;
            <tr>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;"><span style="" >File Name</span></td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;"><span style="" >NA<span>&nbsp;</span></span></td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;"><span style="" >NA<span>&nbsp;</span></span></td>
               &#13;&#10;
               <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">NA<span>&nbsp;</span></span></td>
               &#13;&#10;
               <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">NA<span>&nbsp;</span></span></td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;"><span style="" >NA<span>&nbsp;</span></span></td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;"><span style="" >NA<span>&nbsp;</span></span></td>
               &#13;&#10;
            </tr>
            &#13;&#10;
            <tr>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;"><span style="" >Sheet Name</span></td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;"><span style="" >NA</span></td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;"><span style="" >NA</span></td>
               &#13;&#10;
               <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">NA<br>&#13;&#10;</td>
               <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;">NA<br>&#13;&#10;</td>
               <td style="" class="3D&quot;confluenceTd&quot;">
                  <p>NA<br></p>
               </td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;">
                  <p>NA<br></p>
               </td>
               &#13;&#10;
            </tr>
            &#13;&#10;
            <tr>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;">Metadata properties to export</td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;">
                  <p><span style="">/content/dam/west-elm=<span style="">jcr:content/metadata/dc:title</span></span></p>
               </td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;">
                  <p><br></p>
               </td>
               &#13;&#10;
               <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><br>&#13;&#10;</td>
               <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><br>&#13;&#10;</td>
               <td style="" class="3D&quot;confluenceTd&quot;">
                  <p><br></p>
               </td>
               &#13;&#10;
               <td style="" class="3D&quot;confluenceTd&quot;">
                  <p><br></p>
               </td>
               &#13;&#10;
            </tr>
          
   </div>
    
</div>
&#13;&#10;&#13;&#10;&#13;&#10;&#13;&#10;