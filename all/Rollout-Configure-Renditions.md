
# Rollout - Configure Renditions
    
<div class="3D&quot;Section1&quot;">
        
TRISUL-351 668697 PB Rollout - Configure Renditions  
TRISUL-345 668685 WS Rollout - Configure Renditions  
TRISUL-848 682611 MG &amp; RJ Rollout - Configure Renditions
<div class="3D&quot;table-wrap&quot;">
<table class="3D&quot;confluenceTable&quot;">
<colgroup>
<col>
<col>
<col>
<col>
<col>
</colgroup>
<tbody>
<tr>
<td class="3D&quot;confluenceTd&quot;"><strong>WS Rendition Sizes</strong></td>
<td class="3D&quot;confluenceTd&quot;"><strong>PB Rendition Formats</strong></td>
<td class="3D&quot;confluenceTd&quot;"><strong>MG &amp; RJ Rendition Names</strong>
</td><td class="3D&quot;confluenceTd&quot;"><strong><span style="">Rendition Names</span></strong></td>
<td class="3D&quot;confluenceTd&quot;"><br></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">2000 x 2000 px</td>
<td class="3D&quot;confluenceTd&quot;">2000 x 2000 px</td>
<td class="3D&quot;confluenceTd&quot;">2000 x 2000 px</td>
<td class="3D&quot;confluenceTd&quot;"><span style="">cq5dam.thumbnail.2000.2000.jpeg</span></td>
<td class="3D&quot;confluenceTd&quot;"><br></td>
</tr>
<tr>
<td class="3D&quot;confluenceTd&quot;">450 x 450 px</td>
<td class="3D&quot;confluenceTd&quot;">450 x 450 px</td>
<td class="3D&quot;confluenceTd&quot;">450 x 450 px</td>
<td class="3D&quot;confluenceTd&quot;"><span style="">cq5dam.thumbnail.450.450.jpeg</span></td>
<td class="3D&quot;confluenceTd&quot;"><br></td>
</tr>
</tbody>
</table>
</div>

If an asset gets uploaded to edam then dam update workflow should be triggered and should create above mentioned renditions for that brand.


1. If the renditions are not getting created after asset gets uploaded to edam brand folder then check commands (Check below for**Brand specific commands**section) for that brand are properly deployed.
1. If the commands are proper then check that the workflow in synced after  deploy.&nbsp;

**Steps to sync workflow :**

Open&nbsp;[http://domain:port/editor.html/conf/global/settings/workflow/models/dam/update_asset.html](3D"http://localhost:4502/system/console/configMgr")

Then look for '**Sync**' button at top right corner of above console.

Then Click on **Sync** button to Sync changes and then the button name would be changed to **Synced**.

<br>

- **Brand specific commands&nbsp;:**

Open&nbsp;[http://domain:port/editor.html/conf/global/settings/workflow/models/dam/update_asset.html](3D"http://localhost:4502/system/console/configMgr")

Search with brand name. Ex for WS : **Williams Sonoma**

Then click **EPS Thumbnails** step of that brand&nbsp;

Then click on wrench icon&nbsp;

Then click on arguments and then verify below commands .

- For WS , PB, MG and RJ :&nbsp;

convert -alpha off ./${filename}[0] -colorspace sRGB -profile "/etc/ImageMagick-6/sRGB2014.icc" -quality 90 -resize "2000x2000"^&gt; cq5dam.thumbnail.2000.2000.jpeg

convert -alpha off ./${filename}[0] -colorspace sRGB -profile "/etc/ImageMagick-6/sRGB2014.icc" -quality 90 -resize "450x450"^&gt; cq5dam.thumbnail.450.450.jpeg

<br>
    </div>

