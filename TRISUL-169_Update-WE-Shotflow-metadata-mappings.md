
    
# TRISUL-169:Update WE Shotflow metadata mappings
    
<div class="3D&quot;Section1&quot;">
        
**<span class="3D&quot;ui-dialog-title&quot;">Wsi xmp metadata mapping configuration:</span>**

- <span class="3D&quot;ui-dialog-title&quot;">This configuration is required for Updating WE Shotflow metadata mappings.</span>
- Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr).
- Search for "Wsi xmp metadata mapping configuration" and click on it.
    
    <div class="3D&quot;table-wrap&quot;">
    <table class="3D&quot;confluenceTable&quot;">
    <colgroup>
    <col>
    <col>
    </colgroup>
    <tbody>
    <tr>
    <th class="3D&quot;confluenceTh&quot;">Config Param</th>
    <th class="3D&quot;confluenceTh&quot;">Config Value</th>
    </tr>
    <tr>
    <td class="3D&quot;confluenceTd&quot;">metadataMappingConfigJson</td>
    <td class="3D&quot;confluenceTd&quot;">[{"basePath":"\/content\/dam\/west-elm","mappings":[{"fieldMaps":[{"inKey":"ArtDirector","outKey":"art-director"},{"inKey":"DigitalTech","outKey":"digital-tech"},{"inKey":"Class","outKey":"class"},{"inKey":"Division","outKey":"category"},{"inKey":"Photographer","outKey":"photographer"},{"inKey":"SKU","outKey":"skus"},{"inKey":"SKUColor","outKey":"color"},{"inKey":"SKUDescription","outKey":"product-name"},{"inKey":"Stylist","outKey":"stylist"},{"inKey":"Type","outKey":"asset-type","valueMap":{"SILO":"silo","Silo":"silo","Silo side":"silo","Silo front":"silo","Silo detail":"closeup","Silo 3\/4":"silo","Silo back":"silo","PDI":"pdi","PDI Solo Hero":"pdi","PDI Solo V2":"pdi","PDI Detail":"closeup","PDI Detail 2":"closeup","PDI Group":"pdi","PDI Group Detail":"closeup","GROUP PDI":"pdi","Group PDI":"pdi","LPDI":"pdi","LPDI Solo Hero":"pdi","LPDI Solo V2":"pdi","LPDI Detail":"closeup","LPDI Detail 2":"closeup","LPDI Group":"pdi","LPDI Group Detail":"closeup","PL":"lifestyle","PL Main V1":"lifestyle","PL Main V2":"lifestyle","PL Editorial":"lifestyle","PL Reportage V1":"lifestyle","PL Reportage V2":"lifestyle","PL Reportage V3":"lifestyle","PL Reportage V4":"lifestyle","PL Reportage V5":"lifestyle","PL Reportage V6":"lifestyle","PL Reportage V7":"lifestyle","PL Reportage V8":"lifestyle","PL Reportage V9":"lifestyle","_blank":"other","_default":"other"}},{"inKey":"Season","multiValuemap":{"HO17":{"season":"holiday","year":"2017"},"HO18":{"season":"holiday","year":"2018"},"HO19":{"season":"holiday","year":"2019"},"HO20":{"season":"holiday","year":"2020"},"HO21":{"season":"holiday","year":"2022"},"SP17":{"season":"spring","year":"2017"},"SP18":{"season":"spring","year":"2018"},"SP19":{"season":"spring","year":"2019"},"SP20":{"season":"spring","year":"2020"},"SP21":{"season":"spring","year":"2021"},"SU17":{"season":"summer","year":"2017"},"SU18":{"season":"summer","year":"2018"},"SU19":{"season":"summer","year":"2019"},"SU20":{"season":"summer","year":"2020"},"SU21":{"season":"summer","year":"2021"},"WI17":{"season":"winter","year":"2017"},"WI18":{"season":"winter","year":"2018"},"WI19":{"season":"winter","year":"2019"}," WI20":{"season":"winter","year":"2020"},"WI21":{"season":"winter","year":"2021"},"SP22":{"season":"spring","year":"2022"},"SU22":{"season":"summer","year":"2022"},"WI22":{"season":"winter","year":"2022"}},"outKey":"multi"}],"input":"http:\/\/shotflow1.com\/westelm.namespace\/","output":"http:\/\/content.wsgc.com\/2019\/DigitalAssets"}]}]</td>
    </tr>
    </tbody>
    </table>
    </div>

<br>

<br>
    </div>



