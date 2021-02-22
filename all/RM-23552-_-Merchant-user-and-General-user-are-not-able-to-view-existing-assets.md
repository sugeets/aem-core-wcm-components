 
    


    
# RM-23552 : Merchant user and General user are not able to view exis=&#13;&#10;ting assets
    
<div class="3D&quot;Section1&quot;">
        
**Exception** :

19.02.2021 23:02:15.059 *ERROR* [0:0:0:0:0:0:0:1 [1613755935012] POST /bin/edam/updateAcls HTTP/1.1] com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet Error while adding ACLs at asset path :/content/dam/west-elm  
com.wsgc.ecommerce.edam.core.exceptions.AclException: Exception while granting privilege on path :/content/dam/west-elm/7517848_2.jpg and principal name :APR_EDAM_QA_WE_MERCHANT,APR_EDAM_QA_WE_GENERA  
at com.wsgc.ecommerce.edam.core.services.impl.EdamAclServiceImpl.permissionsUpdate(EdamAclServiceImpl.java:202) [com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT]  
at com.wsgc.ecommerce.edam.core.services.impl.EdamAclServiceImpl.addPermissions(EdamAclServiceImpl.java:127) [com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT]  
at com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet.updateAclPermission(UpdateOlderAssetsAclsServlet.java:104) [com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT]  
at com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet.doPost(UpdateOlderAssetsAclsServlet.java:82) [com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT]  
at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) [org.apache.sling.api:2.20.0]  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342) [org.apache.sling.api:2.20.0]  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374) [org.apache.sling.api:2.20.0]  
at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) [org.apache.sling.engine:2.6.18]  
at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) [org.apache.sling.engine:2.6.18]  
at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) [org.apache.sling.engine:2.6.18]  
at com.day.cq.wcm.core.impl.WCMDebugFilter.doFilter(WCMDebugFilter.java:156) [com.day.cq.wcm.cq-wcm-core:5.12.102]  
at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) [org.apache.sling.engine:2.6.18]  
at com.day.cq.wcm.core.impl.WCMComponentFilter.filterRootInclude(WCMComponentFilter.java:375) [com.day.cq.wcm.cq-wcm-core:5.12.102]  
at com.day.cq.wcm.core.impl.WCMComponentFilter.doFilter(WCMComponentFilter.java:190) [com.day.cq.wcm.cq-wcm-core:5.12.102]  
Caused by: com.wsgc.ecommerce.edam.core.exceptions.AclException: User principal APR_EDAM_QA_WE_MERCHANTS1,APR_EDAM_QA_WE_GENERAL1 is not present or current service user edamSystemService session cannot edit it  
at com.wsgc.ecommerce.edam.core.services.impl.EdamAclServiceImpl.permissionsUpdate(EdamAclServiceImpl.java:191) [com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT]  
... 134 common frames omitted

<br>

**Solution** :

Here issue is with group names are not correct and not available in server. Please provide correct group names and associated brand Path.

<span style="">Go to [host]:[port]/system/console/configMgr. search for "EDAM Utility Configuration" and click on it and add or update "BrandPath and group Names"&nbsp; field.</span>

<br>

**Exception** :

19.02.2021 23:13:42.808 *ERROR* [0:0:0:0:0:0:0:1 [1613756622805] POST /bin/edam/updateAcls HTTP/1.1] org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught Throwable  
java.lang.ArrayIndexOutOfBoundsException: 1  
at com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet.lambda$doPost$2(UpdateOlderAssetsAclsServlet.java:77) [com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT]  
at java.util.stream.Collectors.lambda$toMap$58(Collectors.java:1321)  
at java.util.stream.ReduceOps$3ReducingSink.accept(ReduceOps.java:169)  
at java.util.stream.ReferencePipeline$3$1.accept(ReferencePipeline.java:193)  
at java.util.Spliterators$ArraySpliterator.forEachRemaining(Spliterators.java:948)  
at java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:482)  
at java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:472)  
at java.util.stream.ReduceOps$ReduceOp.evaluateSequential(ReduceOps.java:708)  
at java.util.stream.AbstractPipeline.evaluate(AbstractPipeline.java:234)  
at java.util.stream.ReferencePipeline.collect(ReferencePipeline.java:499)  
at com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet.doPost(UpdateOl=
derAssetsAclsServlet.java:77) [com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT]<br>at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) [org.apache.sling.api:2.20.0]  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342) [org.apache.sling.api:2.20.0]  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374) [org.apache.sling.api:2.20.0]  
at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) [org.apache.sling.engine:2.6.18]  
at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) [org.apache.sling.engine:2.6.18]  
at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) [org.apache.sling.engine:2.6.18]  
at com.day.cq.wcm.core.impl.WCMDebugFilter.doFilter(WCMDebugFilter.java:156) [com.day.cq.wcm.cq-wcm-core:5.12.102]  
at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) [org.apache.sling.engine:2.6.18]  
at com.day.cq.wcm.core.impl.WCMComponentFilter.filterRootInclude(WCMComponentFilter.java:375) [com.day.cq.wcm.cq-wcm-core:5.12.102]<br=>at com.day.cq.wcm.core.impl.WCMComponentFilter.doFilter(WCMComponentFilter.java:190) [com.day.cq.wcm.cq-wcm-core:5.12.102]</br>

<br>

**Solution** :

Here issue is with config properties. Please check given data is correct or not like below format.

Example:&nbsp; /content/dam/west-elm=3DAPR_EDAM_QA_WE_MERCHANTS,APR_EDAM_QA_WE_GENERAL

<span style="">Go to [host]:[port]/system/console/configMgr. search for "EDAM Utility Configuration" and click on it and add or update "BrandPath and group Names"&nbsp; field.</span>

<br>
    </div>
