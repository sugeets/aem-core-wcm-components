# TRISUL-178 : Metadata values - self service admin Configuration
**Metadata schema update exclusion of dropdown property names config&nbsp;(<span style="">com.wsgc.ecommerce.edam.core.listeners.MetadataDropdownsSyncListener</span>):**

    
- This custom&nbsp;Metadata schema update exclusion of dropdown property names configuration contains Metadata schema drop-down property names.
    
- The synchronization does not happen between metadata schema editor to search&nbsp;facets for all CRUD operations on the configured drop-down properties.
    
- Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console/configMgr)
    
- Search for "Metadata schema update exclusion of dropdown property names config" and click on it.
    
- <span style="">Provide multiple properties click on the + icon and add.</span>

<div style="margin-top: 0cm; margin-right: 0cm; margin-bottom: 0.0001pt; margin-left: 0cm; font-size: 16px; font-family: &quot;Times New Roman&quot;, serif;">
    <ul style="margin-bottom: 0cm; list-style-type: disc; margin-left: 26px;">
        <li style="margin-top: 0cm; margin-right: 0cm; margin-bottom: 0.0001pt; margin-left: 0cm; font-size: 16px; font-family: &quot;Times New Roman&quot;, serif;">Following are config param descriptions -<br><strong>dropdown.property.names</strong> contain a list of drop-down property names.<br><strong><span style="">Example</span></strong><span style="">: &nbsp;jcr:content/metadata/wsi:status</span></li>
    </ul>
</div>
<table style="width: 839.25pt; border-collapse: collapse; border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: initial; border-right-style: none; border-right-width: initial; border-bottom-color: initial; border-bottom-style: none; border-bottom-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial;">
    <thead>
        <tr>
            <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
                <span style="color: rgb(122, 134, 154);">&nbsp;Config Param</span>
            </td>
            <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
                <span style="color: rgb(122, 134, 154);">Config Value(Dev)</span>
            </td>
            <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
                <span style="color: rgb(122, 134, 154);">Config Value(QA)</span>
            </td>
            <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
                <span style="color: rgb(122, 134, 154);">Config Value(UAT)</span>
            </td>
            <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
                <span style="color: rgb(122, 134, 154);">Config Value(PROD)</span>
            </td>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
                <span style="color: rgb(34, 34, 34);">dropdown.property.names</span>
            </td>
            <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">  
</td>
            <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">  
</td>
            <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">  
</td>
            <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">  
</td>
        </tr>
    </tbody>
</table>