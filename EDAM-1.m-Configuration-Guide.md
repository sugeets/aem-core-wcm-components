
    
# EDAM 1.m - Configuration Guide
    
<div class="3D&quot;Section1&quot;">
        
<br>

The following document contains the list of configurations that are util=
ized for EDAM 1.m project. Below is an example for reference ONLY.
> 
> 
> <span style=""><u>*<strong>EXAMPLE</strong>=> *</u></span>
> 
> <span style=""><u>**[TRISUL ID here]**</u></span>
> 
> **
> <p><span style=""><strong>MCP Service Configurati=
> on(</strong><strong>com.wsgc.ecommerce.edam.core.services.impl.McpAuthServi=
> ceImpl):</strong></span></p>
> <ul>
> <li><span style="">This custom configuration cont=
> ains MCP Service Configuration mapping for Authorizing Token locally for pr=
> e-validated tokens.</span></li>
> <li><span style="">Navigate to AEM web console (i=
> .e. [hostname]:[portnumber]/system/console/configMgr)</span></li>
> <li><span style="">Search for "MCP Service Config=
> uration" and click on it.</span></li>
> <li><p><span style="">Following are config param =
> descriptions for&nbsp;MCP Service Configuration &nbsp;-</span>  
> <span sty="le=3D&quot;color:">mcp.accesstoken.scopes &nbsp;contains a lis=
> t of authorization scopes.</span>  
> <span style="">oauth.accesstoken contains the most recent access token validated agains=
> t OAuth server with valid authorization scope matching. This is a run-time =
> value.</span>  
> <span style="">oauth.accesstoken=
> .expiry&nbsp;contains the expiry epoch of the last verified access token an=
> d this value can't be configured by user and its run time value.</span></p>=
> </li>
> </ul>
> <div class="3D&quot;table-wrap&quot;">
> <table class="3D&quot;relative-table" confluencetable"="" style="">
> <colgroup>
> <col style="">
> <col style="">
> <col style="">
> <col>
> <col>
> <col style="">
> <col style="">
> </colgroup>
> <thead>
> <tr>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">&nbsp;Config Param</span></p></th>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(Dev)</span></p></th>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(QA)</span></p></th>
> <th colspan="3D&quot;1&quot;" class="3D&quot;confluenceTh&quot;"><span style="">Config Value(RGS)</span></th>
> <th colspan="3D&quot;1&quot;" class="3D&quot;confluenceTh&quot;"><span style="">Config Value(PERF)</span></th>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(UAT)</span></p></th>
> <th style="" class="3D&quot;confluenceTh&quot;"><p><span style="" lor:="">Config Value(PROD)</span></p></th>
> </tr>
> </thead>
> <tbody>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">mcp.accesstoken.scopes</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;"><p><span style="" lor:="">ROLE_APR_MCP_NON_PROD_USERS</span></p></td>
> <td style="" class="3D&quot;confluenceTd&quot;"><p><span style="" lor:="">ROLE_APR_MCP_NON_PROD_USERS</span></p></td>
> <td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">ROLE_APR_MCP_NON_PROD_USERS</span></td>
> <td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">ROLE_APR_MCP_NON_PROD_USERS</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;"><p><span style="" lor:="">ROLE_APR_MCP_NON_PROD_USERS</span></p></td>
> <td style="" class="3D&quot;confluenceTd&quot;"><p><span style="" lor:="">ROLE_APR_MCP_PROD_USERS</span></p></td>
> </tr>
> <tr>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">oauth.accesstoken</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">NA &lt;no value provided&gt;</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">NA &lt;no value provided&gt;</span></td>
> <td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">NA &lt;no value provided&gt;</span></td>
> <td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">NA &lt;no value provided&gt;</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">NA &lt;no value provided&gt;</span></td>
> <td style="" class="3D&quot;confluenceTd&quot;"><span style="" :="">NA &lt;no value provided&gt;</span></td>
> </tr>
> <tr>
> <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><p><sp= an="" style="">oauth.accesstoken.expiry</sp=></p>
> </td><td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><p><sp= an="" style="">NA &lt;no value provided&gt;</sp=></p></td>
> <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">NA &lt;no value provided&gt;</span></td>
> <td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">NA &lt;no value provided&gt;</span></td>
> <td colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">NA &lt;no value provided&gt;</span></td>
> <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><p><sp= an="" style="">NA &lt;no value provided&gt;</sp=></p></td>
> <td style="" colspan="3D&quot;1&quot;" class="3D&quot;confluenceTd&quot;"><span style="">NA &lt;no value provided&gt;</span></td>
> </tr>
> </tbody>
> </table>
> </div>> **

****</div> **&#13;&#10;&#13;&#10;&#13;&#10;**