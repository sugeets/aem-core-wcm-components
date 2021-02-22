   
# Toubleshooting TRISUL-305 : Admin View - Customize Download Dialog with Rendition Picker, Presets, permissions
    
<div class="3D&quot;Section1&quot;">
        
### Enterprise Digital Asset Management AEM servers:

- [aemash-vccn001.wsgc.com:4501]&nbsp;[Primary]


- [aemsac-vccn002.wsgc.com:4502]&nbsp;[Standby]

### Accessing URLs :
#### Frontend :
/conf/global/settings/dam/renditionprofileconfiguration/renditionProfileConfigurationList.html
#### Backend :&nbsp;
/bin/download/rendition/profile&nbsp;[GET, POST, PUT, DELETE]

/bin/download/rendition/profile/all [GET, PUT, DELETE]

/bin/download/rendition/profile/allowedgroups&nbsp;[GET]
### Loggers :&nbsp;
com.wsgc.ecommerce.edam.core.servlets.DownloadRenditionProfilesServlet<b>com.wsgc.ecommerce.edam.core.servlets.DownloadRenditionProfilesAllServlet<br>com.wsgc.ecommerce.edam.core.servlets.DownloadRenditionProfilesAllowedGroupsServlet  
com.wsgc.ecommerce.edam.core.services.impl.DownloadRenditionProfileServiceImpl  
com.wsgc.ecommerce.edam.core.services.impl.DownloadRenditionProfilesAllServiceImpl  
com.wsgc.ecommerce.edam.core.services.impl.DownloadRenditionProfilesAllowedGroupsServiceImpl  
com.wsgc.ecommerce.edam.core.utilities.OsgiUiConfigurationUtilities</b>
### Exception :&nbsp;
DownloadRenditionProfilesException
### Servlet Error Response :&nbsp;
> 
> <pre>{<br>"statusCode" : &lt;&lt;HTTP Status Code &gt;&gt;,<br>"status" : &amp;> lt;&lt;SUCCESS or ERROR&gt;&gt;,<br>"description" : &lt;&lt;Description of >> the error caused&gt;&gt;<br>}</pre>

#### Status Code :&nbsp;

- 500 - Internal server error while processing the request.
- 412 - Request body or query parameter need complete details.

#### Status :&nbsp;

- SUCCESS - Response body served without any error
- ERROR - Error occurred during serving the response body.

### Troubleshooting Profile :&nbsp;
Troubleshooting techniques for&nbsp;/conf/global/settings/dam/renditionprofileconfiguration/renditionProfileConfigurationList.html
##### #1 : Output format options are missing in the Drop-down.
<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;"><img src="https://github.com/sugeets/aem-core-wcm-components/blob/master/all/test.png" /></span>

Check List :&nbsp;

a. Check the "<span style="">Download Renditions Profile Admin View Configuration</span>"&nbsp;=E2=86=92 "Output Format Opti=
ons:".

<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;">![](3D"e94=)</span>
##### #2 : Color Profile options are missing in the Drop-down.
<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;">![](3D"033=)</span>

Check List :&nbsp;

a. Check the "<span style="">Download Renditions Profile Admin View Configuration</span>"&nbsp;=E2=86=92 "Color Profile Options:".

<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;">![](3D"729=)</span>
##### #3 : <span style="">Allowed G=&#13;&#10;roups For Approved Assets</span>&nbsp;options are missing in the Drop-down.=&#13;&#10;
<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;">![](3D"1fa=)</span>

Check List :&nbsp;

a. Check the "<span style="">Download Renditions Profile Admin View Configuration</span>"&nbsp;=E2=86=92 "<span style="" or:="">Allowed Groups For Approved Assets</span>:".

<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;">![](3D"9fd=)</span>

b. Check the given groups are available in AEM&nbsp;[/security/groups.html]

<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;">![](3D"01b=)</span>
##### #4 :&nbsp;<span style="">Al=&#13;&#10;lowed Groups For unApproved Assets</span>&nbsp;options are missing in the D=&#13;&#10;rop-down.
<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;">![](3D"594=)</span>

Check List :&nbsp;

a. Check the "<span style="">Download Renditions Profile Admin View Configuration</span>"&nbsp;=E2=86=92 "<span style="" or:="">Allowed Groups For Approved Assets</span>:".

<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;">![](3D"4ac=)</span>

b. Check the given groups are available in AEM&nbsp;[/security/groups.html]

<span class="3D&quot;confluence-embedded-file-wrapper" confluence-embedded-manu="al-size&quot;">![](3D"ab9=)</span>
##### #5 : Servlet=&#13;&#10; error and descriptions&nbsp;

- Profile doesn't exist with the name : Xxxxx
- Profile path should not be NULL or Blank !
- Profile already exists with the Name :&nbsp;Xxxxx
- Profile NAME and UUID is mandatory for update!!
- PayLoad or File Type is not supported !
- Profile with name Original can not be deleted.
- Profile to delete with the Xxxxx doesn't exist !!
- Profile name should not be NULL or Blank !

<br>
    </div>



