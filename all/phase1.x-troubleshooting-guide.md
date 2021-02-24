
Troubleshooting Guide 1.x
=========================

*   [TRISUL-176 - Export metadata based on search results - Reporting](#trisul-176--export-metadata-based-on-search-results---reporting)
*   [TRISUL-663 : bulk edit of Metadata for any number of Assets](#trisul-663--bulk-edit-of-metadata-for-any-number-of-assets)
*   [Rollout - High Resolution Threshold](#rollout---high-resolution-threshold)
*   [Rollout - Configure Renditions](#rollout---configure-renditions)
*   [TRISUL-570 : Global Nav - Tabs per Brand to navigate to appropriate server/root folder](#trisul-570--global-nav---tabs-per-brand-to-navigate-to-appropriate-serverroot-folder)
*   [TRISUL-305 : Admin View - Customize Download Dialog with Rendition Picker, Presets, permissions](#trisul-305-admin-view---customize-download-dialog-with-rendition-picker-presets-permissions)
*   [TRISUL-362 : PB & WS Rollout - Set-up Duo Login](#trisul-362--pb--ws-rollout---set-up-duo-login)
*   [TRISUL-178 : Metadata values self service admin](#trisul-178--metadata-values-self-service-admin)
*   [TRISUL-571 & TRISUL-705 : User View - Customize Download Dialog with Rendition Picker, Presets, permissions](#trisul-571--trisul-705--user-view---customize-download-dialog-with-rendition-picker-presets-permissions)
*   [TRISUL-350, TRISUL-344 - Retrofit WSI Schema](#trisul-350-trisul-344---retrofit-wsi-schema)
*   [TRISUL-344 Trisul-350 Trisul-857 Trisul-858 Applying Rules Metadata Cascading](#trisul-344-trisul-350-trisul-857-trisul-858-applying-rules-metadata-cascading)
*   [TRISUL-885 TRISUL-886 Setup Groups and Permissions](#trisul-885-trisul-886-setup-groups-and-permissions)
*   [TRISUL-661 : Add "Keywords" Metadata to "Overview" section](#trisul-661--add-keywords-metadata-to-overview-section)
*   [RM-23552 : Merchant user and General user are not able to view existing assets](#rm-23552--merchant-user-and-general-user-are-not-able-to-view-existing-assets)
*   [Guide for Asset Migration from Legacy to EDAM](#guide-for-asset-migration-from-legacy-to-edam)

### TRISUL-176 - **Export metadata based on search results - Reporting**

1\. After selecting an asset If “Export Metadata” button is not visible then there is an issue with deployment or code is not available.  
2\. After clicking on the "Export Metadata" if you see any dialog saying that "Please provide configuration for Metadata Exporter" means need to provide configuration.  
    Go to \[host\]:\[port\]/system/console/configMgr. search for "Configuration for Metadata Exporter" and click on it.  
3\. Update the properties "File Name", "Sheet Name" and "Metadata properties to export" then click on Save.  
Exception:  
                org.apache.sling.servlets.post.impl.operations.ModifyOperation Exception during response processing.  
                org.apache.sling.api.resource.PersistenceException: Unable to create node at /bin/edam  
                at org.apache.sling.jcr.resource.internal.helper.jcr.JcrResourceProvider.create(JcrResourceProvider.java:480) \[org.apache.sling.jcr.resource:3.0.18\]  
                at org.apache.sling.resourceresolver.impl.providers.stateful.AuthenticatedResourceProvider.create(AuthenticatedResourceProvider.java:182)  
Solution:  
               Go to \[host\]:\[port\]/system/console/components find out the "MetadataExportServlet" and check component is active or not.  
               if component is not in active state then check the references.

Exception:

          15.02.2021 14:30:49.769 \*ERROR\* \[0:0:0:0:0:0:0:1 \[1613379649766\] POST /bin/edam/exportmetadata HTTP/1.1\] org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught Throwable  
          java.lang.ArrayIndexOutOfBoundsException: 0  
          at java.util.Arrays$ArrayList.get(Arrays.java:3841)  
          at com.wsgc.ecommerce.edam.core.servlets.MetadataExportServlet.lambda$getPathsBasedOnConfiguredProperties$3(MetadataExportServlet.java:211)                                     \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
         at java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:174)  
         at java.util.HashMap$EntrySpliterator.tryAdvance(HashMap.java:1720)  
         at java.util.stream.ReferencePipeline.forEachWithCancel(ReferencePipeline.java:126)  
         at java.util.stream.AbstractPipeline.copyIntoWithCancel(AbstractPipeline.java:499)  
         at java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:486)  
         at java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:472)  
         at java.util.stream.FindOps$FindOp.evaluateSequential(FindOps.java:152)  
        at java.util.stream.AbstractPipeline.evaluate(AbstractPipeline.java:234)  
        at java.util.stream.ReferencePipeline.findFirst(ReferencePipeline.java:464)  
        at com.wsgc.ecommerce.edam.core.servlets.MetadataExportServlet.getPathsBasedOnConfiguredProperties(MetadataExportServlet.java:212) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
        at com.wsgc.ecommerce.edam.core.servlets.MetadataExportServlet.doPost(MetadataExportServlet.java:85) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
        at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) \[org.apache.sling.api:2.20.0\]  
        at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342) \[org.apache.sling.api:2.20.0\]  
        at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374) \[org.apache.sling.api:2.20.0\]  
        at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) \[org.apache.sling.engine:2.6.18\]

Solution:

      Please check the request header, Selected assets path list must contains asset path.

### TRISUL-663 : bulk edit of Metadata for any number of Assets

Exception :  
          15.02.2021 15:18:05.567 \*ERROR\* \[0:0:0:0:0:0:0:1 \[1613382485565\] POST /bin/edam/metadataeditor HTTP/1.1\] org.apache.sling.servlets.post.impl.operations.ModifyOperation Exception during  response processing.  
          org.apache.sling.api.resource.PersistenceException: Unable to create node at /bin/edam  
          at org.apache.sling.jcr.resource.internal.helper.jcr.JcrResourceProvider.create(JcrResourceProvider.java:480) \[org.apache.sling.jcr.resource:3.0.18\]  
          at org.apache.sling.resourceresolver.impl.providers.stateful.AuthenticatedResourceProvider.create(AuthenticatedResourceProvider.java:182) \[org.apache.sling.resourceresolver:1.6.8\]  
          at org.apache.sling.resourceresolver.impl.helper.ResourceResolverControl.create(ResourceResolverControl.java:379) \[org.apache.sling.resourceresolver:1.6.8\]  
          at org.apache.sling.resourceresolver.impl.ResourceResolverImpl.create(ResourceResolverImpl.java:971) \[org.apache.sling.resourceresolver:1.6.8\]  
          at org.apache.sling.servlets.post.impl.operations.AbstractCreateOperation.deepGetOrCreateResource(AbstractCreateOperation.java:598) \[org.apache.sling.servlets.post:2.3.26\]  
          at org.apache.sling.servlets.post.impl.operations.AbstractCreateOperation.processCreate(AbstractCreateOperation.java:146) \[org.apache.sling.servlets.post:2.3.26\]  
          at org.apache.sling.servlets.post.impl.operations.ModifyOperation.doRun(ModifyOperation.java:83) \[org.apache.sling.servlets.post:2.3.26\]  
          at org.apache.sling.servlets.post.impl.operations.AbstractPostOperation.run(AbstractPostOperation.java:99) \[org.apache.sling.servlets.post:2.3.26\]  
          at org.apache.sling.servlets.post.impl.SlingPostServlet.doPost(SlingPostServlet.java:228) \[org.apache.sling.servlets.post:2.3.26\]  
          at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) \[org.apache.sling.api:2.20.0\]  
          at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342) \[org.apache.sling.api:2.20.0\]  
          at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374) \[org.apache.sling.api:2.20.0\]  
          at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) \[org.apache.sling.engine:2.6.18\]  
          at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) \[org.apache.sling.engine:2.6.18\]  
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) \[org.apache.sling.engine:2.6.18\]  
          at com.day.cq.wcm.core.impl.WCMDebugFilter.doFilter(WCMDebugFilter.java:156) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
          at com.day.cq.wcm.core.impl.WCMComponentFilter.filterRootInclude(WCMComponentFilter.java:375) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
          at com.day.cq.wcm.core.impl.WCMComponentFilter.doFilter(WCMComponentFilter.java:190) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
          at com.day.cq.wcm.core.impl.page.PageLockFilter.doFilter(PageLockFilter.java:91) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]

Solution :

           Go to \[host\]:\[port\]/system/console/components find out the "AssetsMetadataEditorServlet" and check component is active or not.  
           if component is not in active state then check the references.

Exception :

          15.02.2021 15:30:44.608 \*ERROR\* \[0:0:0:0:0:0:0:1 \[1613383244606\] POST /bin/edam/metadataeditor HTTP/1.1\] org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught Throwable  
          java.lang.NullPointerException: null  
          at com.wsgc.ecommerce.edam.core.servlets.AssetsMetadataEditorServlet.lambda$getSelectedAssetsList$0(AssetsMetadataEditorServlet.java:149) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
          at java.util.Arrays$ArrayList.forEach(Arrays.java:3880)  
          at com.wsgc.ecommerce.edam.core.servlets.AssetsMetadataEditorServlet.getSelectedAssetsList(AssetsMetadataEditorServlet.java:147) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
          at com.wsgc.ecommerce.edam.core.servlets.AssetsMetadataEditorServlet.getAllSelectedAssetsSearchList(AssetsMetadataEditorServlet.java:133) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
          at com.wsgc.ecommerce.edam.core.servlets.AssetsMetadataEditorServlet.doPost(AssetsMetadataEditorServlet.java:82) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
          at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) \[org.apache.sling.api:2.20.0\]  
          at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342) \[org.apache.sling.api:2.20.0\]  
          at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374) \[org.apache.sling.api:2.20.0\]  
          at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) \[org.apache.sling.engine:2.6.18\]  
          at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) \[org.apache.sling.engine:2.6.18\]  
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) \[org.apache.sling.engine:2.6.18\]  
          at com.day.cq.wcm.core.impl.WCMDebugFilter.doFilter(WCMDebugFilter.java:156) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
          at com.day.cq.wcm.core.impl.WCMComponentFilter.filterRootInclude(WCMComponentFilter.java:375) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
          at com.day.cq.wcm.core.impl.WCMComponentFilter.doFilter(WCMComponentFilter.java:190) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
          at com.day.cq.wcm.core.impl.page.PageLockFilter.doFilter(PageLockFilter.java:91) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
          at com.day.cq.personalization.impl.TargetComponentFilter.doFilter(TargetComponentFilter.java:94) \[com.day.cq.cq-personalization:5.12.38\]   
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
          at org.apache.sling.engine.impl.SlingRequestProcessorImpl.processComponent(SlingRequestProcessorImpl.java:282) \[org.apache.sling.engine:2.6.18\]  
          at org.apache.sling.engine.impl.filter.RequestSlingFilterChain.render(RequestSlingFilterChain.java:49) \[org.apache.sling.engine:2.6.18\]  
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:76) \[org.apache.sling.engine:2.6.18\]  
          at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:78) \[org.apache.sling.engine:2.6.18\]  
          at com.day.cq.wcm.core.impl.warp.TimeWarpFilter.doFilter(TimeWarpFilter.java:109) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]

Solution :

        Please check the request header, Selected assets path list must available in dam. 

Exception:

      16.02.2021 12:48:39.237 \*ERROR\* \[0:0:0:0:0:0:0:1 \[1613459919225\] POST /bin/edam/bulkassetmetdata HTTP/1.1\] org.apache.sling.servlets.post.impl.operations.ModifyOperation Exception during  response processing.  
      org.apache.sling.api.resource.PersistenceException: Unable to create node at /bin/edam  
      at org.apache.sling.jcr.resource.internal.helper.jcr.JcrResourceProvider.create(JcrResourceProvider.java:480) \[org.apache.sling.jcr.resource:3.0.18\]  
      at org.apache.sling.resourceresolver.impl.providers.stateful.AuthenticatedResourceProvider.create(AuthenticatedResourceProvider.java:182) \[org.apache.sling.resourceresolver:1.6.8\]  
      at org.apache.sling.resourceresolver.impl.helper.ResourceResolverControl.create(ResourceResolverControl.java:379) \[org.apache.sling.resourceresolver:1.6.8\]  
      at org.apache.sling.resourceresolver.impl.ResourceResolverImpl.create(ResourceResolverImpl.java:971) \[org.apache.sling.resourceresolver:1.6.8\]  
      at org.apache.sling.servlets.post.impl.operations.AbstractCreateOperation.deepGetOrCreateResource(AbstractCreateOperation.java:598) \[org.apache.sling.servlets.post:2.3.26\]  
      at org.apache.sling.servlets.post.impl.operations.AbstractCreateOperation.processCreate(AbstractCreateOperation.java:146) \[org.apache.sling.servlets.post:2.3.26\]  
      at org.apache.sling.servlets.post.impl.operations.ModifyOperation.doRun(ModifyOperation.java:83) \[org.apache.sling.servlets.post:2.3.26\]  
      at org.apache.sling.servlets.post.impl.operations.AbstractPostOperation.run(AbstractPostOperation.java:99) \[org.apache.sling.servlets.post:2.3.26\]  
      at org.apache.sling.servlets.post.impl.SlingPostServlet.doPost(SlingPostServlet.java:228) \[org.apache.sling.servlets.post:2.3.26\]  
      at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) \[org.apache.sling.api:2.20.0\]  
      at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342) \[org.apache.sling.api:2.20.0\]  
      at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374) \[org.apache.sling.api:2.20.0\]  
      at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) \[org.apache.sling.engine:2.6.18\]  
      at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) \[org.apache.sling.engine:2.6.18\]  
      at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) \[org.apache.sling.engine:2.6.18\]  
      at com.day.cq.wcm.core.impl.WCMDebugFilter.doFilter(WCMDebugFilter.java:156) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
     at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
     at com.day.cq.wcm.core.impl.WCMComponentFilter.filterRootInclude(WCMComponentFilter.java:375) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
     at com.day.cq.wcm.core.impl.WCMComponentFilter.doFilter(WCMComponentFilter.java:190) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
     at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
    at com.day.cq.wcm.core.impl.page.PageLockFilter.doFilter(PageLockFilter.java:91) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
    at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
    at com.day.cq.personalization.impl.TargetComponentFilter.doFilter(TargetComponentFilter.java:94) \[com.day.cq.cq-personalization:5.12.38\]  
    at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
    at org.apache.sling.engine.impl.SlingRequestProcessorImpl.processComponent(SlingRequestProcessorImpl.java:282) \[org.apache.sling.engine:2.6.18\]  
    at org.apache.sling.engine.impl.filter.RequestSlingFilterChain.render(RequestSlingFilterChain.java:49) \[org.apache.sling.engine:2.6.18\]  
    at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:76) \[org.apache.sling.engine:2.6.18\]  
    at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:78) \[org.apache.sling.engine:2.6.18\]  
    at com.day.cq.wcm.core.impl.warp.TimeWarpFilter.doFilter(TimeWarpFilter.java:109) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]

Solution :

Go to \[host\]:\[port\]/system/console/components find out the "MetadataSchemaPropertyTypeServiceImpl" and check component is active or not.  
           if component is not in active state then check the references.

Exception :

    16.02.2021 13:12:27.315 \*ERROR\* \[0:0:0:0:0:0:0:1 \[1613461347311\] POST /bin/edam/bulkassetmetdata HTTP/1.1\] org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught Throwable  
com.wsgc.ecommerce.edam.core.exceptions.BulkAssetMetadataUpdateException: Error occured while reading schemaProperies map : /jcr:content/metadata/wsi:skus : null  
   at com.wsgc.ecommerce.edam.core.servlets.BulkAssetMetadataUpdateServlet.setPropertiesToNode(BulkAssetMetadataUpdateServlet.java:205) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
   at com.wsgc.ecommerce.edam.core.servlets.BulkAssetMetadataUpdateServlet.lambda$null$1(BulkAssetMetadataUpdateServlet.java:169) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
   at java.lang.Iterable.forEach(Iterable.java:75)  
  at com.wsgc.ecommerce.edam.core.servlets.BulkAssetMetadataUpdateServlet.lambda$setMetadataPropertiesToAssets$2(BulkAssetMetadataUpdateServlet.java:168) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
  at java.lang.Iterable.forEach(Iterable.java:75)  
  at com.wsgc.ecommerce.edam.core.servlets.BulkAssetMetadataUpdateServlet.setMetadataPropertiesToAssets(BulkAssetMetadataUpdateServlet.java:166) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
  at com.wsgc.ecommerce.edam.core.servlets.BulkAssetMetadataUpdateServlet.doPost(BulkAssetMetadataUpdateServlet.java:101) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
  at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) \[org.apache.sling.api:2.20.0\]  
  at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342) \[org.apache.sling.api:2.20.0\]  
  at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374) \[org.apache.sling.api:2.20.0\]  
  at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) \[org.apache.sling.engine:2.6.18\]  
  at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) \[org.apache.sling.engine:2.6.18\]  
  at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) \[org.apache.sling.engine:2.6.18\]  
  at com.day.cq.wcm.core.impl.WCMDebugFilter.doFilter(WCMDebugFilter.java:156) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
  at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
  at com.day.cq.wcm.core.impl.WCMComponentFilter.filterRootInclude(WCMComponentFilter.java:375) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
  at com.day.cq.wcm.core.impl.WCMComponentFilter.doFilter(WCMComponentFilter.java:190) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
  at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
  at com.day.cq.wcm.core.impl.page.PageLockFilter.doFilter(PageLockFilter.java:91) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
  at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
  at com.day.cq.personalization.impl.TargetComponentFilter.doFilter(TargetComponentFilter.java:94) \[com.day.cq.cq-personalization:5.12.38\]  
  at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
  at org.apache.sling.engine.impl.SlingRequestProcessorImpl.processComponent(SlingRequestProcessorImpl.java:282) \[org.apache.sling.engine:2.6.18\]  
  at org.apache.sling.engine.impl.filter.RequestSlingFilterChain.render(RequestSlingFilterChain.java:49) \[org.apache.sling.engine:2.6.18\]  
  at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:76) \[org.apache.sling.engine:2.6.18\]  
  at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:78) \[org.apache.sling.engine:2.6.18\]  
  at com.day.cq.wcm.core.impl.warp.TimeWarpFilter.doFilter(TimeWarpFilter.java:109) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]

Solution :

Please check metadataSchemaPropertyTypeService.getSchemaPropertyType() method. it must contain all WSI metadata properties.  

If requested property is not available in map then it will throw above exception.

### **Rollout - High Resolution Threshold**

TRISUL-859 682680 MG & RJ Rollout - High Resolution Threshold

TRISUL-352 668699 PB Rollout - High Resolution Threshold

TRISUL-346 668686 WS Rollout - High Resolution Threshold

1.  If ' **Is High Resolution** ' property is empty in asset ' **Summary'**  tab then check that the configs related to high resolution property authored as expected. Follow steps mentioned in High Resolution listener Configs section below.
2.  If 'Is High Resolution' property is suppose to be YES for an asset but it is not after upload,  then check that uploaded asset heigh or width greater than than authored value (ref : High Resolution listener Configs Section) of an asset
3.  If 'Is High Resolution' property is suppose to be No for an asset but it is not after upload,  then check that uploaded asset heigh or width lesser than authored value (ref : High Resolution listener Configs Section) of an asset

*   High Resolution listener Configs :

Open [http://domain:port/system/console/configMgr](http://localhost:4502/system/console/configMgr)

Search for 'High Resolution listener config'

Then check for below 

For WS : /content/dam/williams-sonoma=2000

For PB : /content/dam/pottery-barn=4800

For WE : /content/dam/west-elm=2000

For MG : /content/dam/mark-and-graham=2000

For RJ : /content/dam/rejuvenation=2000

### **Rollout - Configure Renditions**

TRISUL-351 668697 PB Rollout - Configure Renditions  
TRISUL-345 668685 WS Rollout - Configure Renditions  
TRISUL-848 682611 MG & RJ Rollout - Configure Renditions

<div>

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" style="border-collapse: collapse; border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: initial; border-right-style: none; border-right-width: initial; border-bottom-color: initial; border-bottom-style: none; border-bottom-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial;">
 <colgroup><col><col><col><col><col></colgroup>
 <tbody><tr style="page-break-inside: avoid;">
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">WS Rendition Sizes</p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">PB Rendition Formats</p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">MG &amp; RJ Rendition Names</p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal"><span style="color: rgb(23, 43, 77);">Rendition Names</span></p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">2000 x 2000 px</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">2000 x 2000 px</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">2000 x 2000 px</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal"><span style="color: rgb(23, 43, 77);">cq5dam.thumbnail.2000.2000.jpeg</span></p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">450 x 450 px</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">450 x 450 px</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">450 x 450 px</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal"><span style="color: rgb(23, 43, 77);">cq5dam.thumbnail.450.450.jpeg</span></p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
 </tr>
</tbody></table>

</div>

If an asset gets uploaded to edam then dam update workflow should be triggered and should create above mentioned renditions for that brand.

1.  If the renditions are not getting created after asset gets uploaded to edam brand folder then check commands (Check below for Brand specific commands section) for that brand are properly deployed.
2.  If the commands are proper then check that the workflow in synced after deploy. 

Steps to sync workflow :

Open [http://domain:port/editor.html/conf/global/settings/workflow/models/dam/update\_asset.html](http://localhost:4502/system/console/configMgr)

Then look for 'Sync' button at top right corner of above console.

Then Click on Sync button to Sync changes and then the button name would be changed to Synced.

*   Brand specific commands :

Open [http://domain:port/editor.html/conf/global/settings/workflow/models/dam/update\_asset.html](http://localhost:4502/system/console/configMgr)

Search with brand name. Ex for WS : Williams Sonoma

Then click EPS Thumbnails step of that brand 

Then click on wrench icon 

Then click on arguments and then verify below commands .

*   For WS , PB, MG and RJ : 

convert -alpha off ./${filename}\[0\] -colorspace sRGB -profile "/etc/ImageMagick-6/sRGB2014.icc" -quality 90 -resize "2000x2000"^> cq5dam.thumbnail.2000.2000.jpeg

convert -alpha off ./${filename}\[0\] -colorspace sRGB -profile "/etc/ImageMagick-6/sRGB2014.icc" -quality 90 -resize "450x450"^> cq5dam.thumbnail.450.450.jpeg

### TRISUL-570 : Global Nav - Tabs per Brand to navigate to appropriate server/root folder

Global Navigation Links Configuration -

Global Navigation Main Menu Text: Global Naviation Main Menu Text

Global Navigation Links List: Value Pattern would be <<BRAND PATH>>|<<BRAND NAME>>|<<BRAND LINK>> (getGlobalNavigationLinks)

Configuration Link :

https://<<Env Host>>:<<port>>/system/console/configMgr

Troubleshooting Navigation Links :

Issue #1 : Global menu text link is having issue

**Solution :**  Navigate the Configurations → "Global Navigation Links Configuration" → verify "Global Navigation Links List".

![](troubleshootingimages/image001.png?raw=true)

![](troubleshootingimages/image002.png?raw=true)

#2 Links label text having issue.

**Solution :**  Navigate the Configurations → "Global Navigation Links Configuration" → verify "Global Navigation Main Menu Text".

![](troubleshootingimages/image003.png?raw=true)

![](troubleshootingimages/image004.png?raw=true)

#3 Links are having issue.

**Solution :**  Navigate the Configurations → "Global Navigation Links Configuration" → verify "Global Navigation Links List".

![](troubleshootingimages/image005.png?raw=true)

![](troubleshootingimages/image006.png?raw=true)

#3 Below error thrown while access the pages.

com.wsgc.ecommerce.edam.core.exceptions.UtilitiesException: An error occured in getStringArrayOSGIConfig method of OSGIUIConfigurationUtilities : 

        at com.wsgc.ecommerce.edam.core.utilities.OsgiUiConfigurationUtilities.getStringArrayOSGIConfig(OsgiUiConfigurationUtilities.java:75)

        at org.apache.jsp.apps.granite.ui.components.shell.collectionpage.collectionpage\_jsp.\_jspService(collectionpage\_jsp.java:446)

        at org.apache.sling.scripting.jsp.jasper.runtime.HttpJspBase.service(HttpJspBase.java:70)

        at javax.servlet.http.HttpServlet.service(HttpServlet.java:725)

        at org.apache.sling.scripting.jsp.jasper.servlet.JspServletWrapper.service(JspServletWrapper.java:502)

        at org.apache.sling.scripting.jsp.jasper.servlet.JspServletWrapper.service(JspServletWrapper.java:449)

        at org.apache.sling.scripting.jsp.JspScriptEngineFactory.callJsp(JspScriptEngineFactory.java:342)

        at org.apache.sling.scripting.jsp.JspScriptEngineFactory.access$100(JspScriptEngineFactory.java:97)

        at org.apache.sling.scripting.jsp.JspScriptEngineFactory$JspScriptEngine.eval(JspScriptEngineFactory.java:603)

        at org.apache.sling.scripting.core.impl.DefaultSlingScript.call(DefaultSlingScript.java:388)

        at org.apache.sling.scripting.core.impl.DefaultSlingScript.eval(DefaultSlingScript.java:184)

        at org.apache.sling.scripting.core.impl.DefaultSlingScript.service(DefaultSlingScript.java:491)

        at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552)

        at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44)

        at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82)

        at com.day.cq.wcm.core.impl.WCMDeveloperModeFilter.doFilter(WCMDeveloperModeFilter.java:119)

        at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72)

**Solution :**  Navigate the Configurations → check for the configuration available or not "Global Navigation Links Configuration" 

### TRISUL-305 : Admin View - Customize Download Dialog with Rendition Picker, Presets, permissions

Accessing URLs :

Frontend :

/conf/global/settings/dam/renditionprofileconfiguration/renditionProfileConfigurationList.html

Backend : 

/bin/download/rendition/profile \[GET, POST, PUT, DELETE\]

/bin/download/rendition/profile/all \[GET, PUT, DELETE\]

/bin/download/rendition/profile/allowedgroups \[GET\]

Loggers : 

com.wsgc.ecommerce.edam.core.servlets.DownloadRenditionProfilesServlet  
com.wsgc.ecommerce.edam.core.servlets.DownloadRenditionProfilesAllServlet  
com.wsgc.ecommerce.edam.core.servlets.DownloadRenditionProfilesAllowedGroupsServlet  
com.wsgc.ecommerce.edam.core.services.impl.DownloadRenditionProfileServiceImpl  
com.wsgc.ecommerce.edam.core.services.impl.DownloadRenditionProfilesAllServiceImpl  
com.wsgc.ecommerce.edam.core.services.impl.DownloadRenditionProfilesAllowedGroupsServiceImpl  
com.wsgc.ecommerce.edam.core.utilities.OsgiUiConfigurationUtilities

Exception : 

DownloadRenditionProfilesException

Servlet Error Response : 

> {  
> "statusCode" : <<HTTP Status Code >>,  
> "status" : <<SUCCESS or ERROR>>,  
> "description" : <<Description of the error caused>>  
> }

Status Code : 

*   500 - Internal server error while processing the request.
*   412 - Request body or query parameter need complete details.

Status : 

*   SUCCESS - Response body served without any error
*   ERROR - Error occurred during serving the response body.

Troubleshooting Profile : 

Troubleshooting techniques for /conf/global/settings/dam/renditionprofileconfiguration/renditionProfileConfigurationList.html

#1 : Output format options are missing in the Drop-down.

![](troubleshootingimages/image007.png?raw=true)

Check List : 

a. Check the "Download Renditions Profile Admin View Configuration" → "Output Format Options:".

![](troubleshootingimages/image008.png?raw=true)

#2 : Color Profile options are missing in the Drop-down.

![](troubleshootingimages/image009.png?raw=true)

Check List : 

a. Check the "Download Renditions Profile Admin View Configuration" → "Color Profile Options:".

![](troubleshootingimages/image010.png?raw=true)

#3 :  Allowed Groups For Approved Assets options are missing in the Drop-down.

![](troubleshootingimages/image011.png?raw=true)

Check List : 

a. Check the "Download Renditions Profile Admin View Configuration" → "Allowed Groups For Approved Assets:".

![](troubleshootingimages/image012.png?raw=true)

b. Check the given groups are available in AEM \[/security/groups.html\]

![](troubleshootingimages/image013.png?raw=true)

#4 : Allowed Groups For unApproved Assets options are missing in the Drop-down.

![](troubleshootingimages/image014.png?raw=true)

Check List : 

a. Check the "Download Renditions Profile Admin View Configuration" → "Allowed Groups For Approved Assets:".

![](troubleshootingimages/image015.png?raw=true)

b. Check the given groups are available in AEM \[/security/groups.html\]

![](troubleshootingimages/image016.png?raw=true)

#5 : Servlet error and descriptions 

Profile doesn't exist with the name : Xxxxx

Profile path should not be NULL or Blank !

Profile already exists with the Name : Xxxxx

Profile NAME and UUID is mandatory for update!!

PayLoad or File Type is not supported !

Profile with name Original can not be deleted.

Profile to delete with the Xxxxx doesn't exist !!

Profile name should not be NULL or Blank !

### TRISUL-362 : PB & WS Rollout - Set-up Duo Login

[Configure SAML Integration on EDAM AEM Environments](https://confluence.wsgc.com/display/PdM/Configure+SAML+Integration+on+EDAM+AEM+Environments)

After successfully integrated EDAM with Duo.

Login to EDAM application using http://domain:port/assets.html/content/dam

Then you will be redirected to DUO for authentication 

then enter your credentials 

then you will be taken to http://domain:port/assets.html/content/dam if you are authenticated user.

1.  **Exception :**

HTTP ERROR 500  
Problem accessing /content/saml\_login. Reason:  
Server Error  
Caused by:  
com.wsgc.ecommerce.edam.core.exceptions.AuthenticationProcessorException: Could not impersonate user: null to system user: edamSystemService  
at com.wsgc.ecommerce.edam.core.processors.WsiThirdPartyUsersAuthenticationPostProcessor.postProcess(WsiThirdPartyUsersAuthenticationPostProcessor.java:148)  
at com.day.cq.compat.commonsauth.impl.AuthenticationInfoPostProcessorBridge.postProcess(AuthenticationInfoPostProcessorBridge.java:44)

Solution :

http://domain:port/system/console/configMgr

Search for 'Adobe Granite SAML 2.0 Authentication Handler'

Then check property '**IDP Certificate Alias**' is matched with  **alias**  column values of trust store from below console

http://domain:port/libs/granite/security/content/truststore.html

**2\. User able to login to EDAM but not able to see WS or PB brand folders under /content/dam/**

After login to edam, check that user is assigned to respective group in useradmin console

**Steps to check assigned groups for the user**

Access http://domain:port/useradmin

Then search for the user with user id and open it by double clicking.

then click on Groups tab

and then check that user has valid groups. If groups are not properly assigned then consult IDP team.

### TRISUL-178 : Metadata values self service admin

Exception:

\[main\] ERROR com.wsgc.ecommerce.edam.core.listeners.metadataDropdownsSynchException - Error while getting path from event with exception : Unable to get path from event  
javax.jcr.RepositoryException: Unable to get path from event  
at com.wsgc.ecommerce.edam.core.listeners.metadataDropdownsSynchException.onEvent(metadataDropdownsSynchException.java:194)  
at com.wsgc.ecommerce.edam.core.listeners.test.metadataDropdownsSynchExceptionTest.testOnEventWhenExceptionExpectNoOperation(metadataDropdownsSynchExceptionTest.java:282)  
at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)  
at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)  
at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)  
at java.lang.reflect.Method.invoke(Method.java:498)  
at org.junit.platform.commons.util.ReflectionUtils.invokeMethod(ReflectionUtils.java:389)  
at org.junit.jupiter.engine.execution.ExecutableInvoker.invoke(ExecutableInvoker.java:115)  
at org.junit.jupiter.engine.descriptor.TestMethodTestDescriptor.lambda$invokeTestMethod$6(TestMethodTestDescriptor.java:167)  
at org.junit.jupiter.engine.execution.ThrowableCollector.execute(ThrowableCollector.java:40)  
at org.junit.jupiter.engine.descriptor.TestMethodTestDescriptor.invokeTestMethod(TestMethodTestDescriptor.java:163)  
at org.junit.jupiter.engine.descriptor.TestMethodTestDescriptor.execute(TestMethodTestDescriptor.java:110)  
at org.junit.jupiter.engine.descriptor.TestMethodTestDescriptor.execute(TestMethodTestDescriptor.java:57)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestExecutor.lambda$execute$3(HierarchicalTestExecutor.java:83)  
at org.junit.platform.engine.support.hierarchical.SingleTestExecutor.executeSafely(SingleTestExecutor.java:66)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestExecutor.execute(HierarchicalTestExecutor.java:77)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestExecutor.lambda$null$2(HierarchicalTestExecutor.java:92)  
at java.util.stream.ForEachOps$ForEachOp$OfRef.accept(ForEachOps.java:184)  
at java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:175)  
at java.util.Iterator.forEachRemaining(Iterator.java:116)  
at java.util.Spliterators$IteratorSpliterator.forEachRemaining(Spliterators.java:1801)  
at java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:482)  
at java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:472)  
at java.util.stream.ForEachOps$ForEachOp.evaluateSequential(ForEachOps.java:151)  
at java.util.stream.ForEachOps$ForEachOp$OfRef.evaluateSequential(ForEachOps.java:174)  
at java.util.stream.AbstractPipeline.evaluate(AbstractPipeline.java:234)  
at java.util.stream.ReferencePipeline.forEach(ReferencePipeline.java:418)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestExecutor.lambda$execute$3(HierarchicalTestExecutor.java:92)  
at org.junit.platform.engine.support.hierarchical.SingleTestExecutor.executeSafely(SingleTestExecutor.java:66)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestExecutor.execute(HierarchicalTestExecutor.java:77)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestExecutor.lambda$null$2(HierarchicalTestExecutor.java:92)  
at java.util.stream.ForEachOps$ForEachOp$OfRef.accept(ForEachOps.java:184)  
at java.util.stream.ReferencePipeline$2$1.accept(ReferencePipeline.java:175)  
at java.util.Iterator.forEachRemaining(Iterator.java:116)  
at java.util.Spliterators$IteratorSpliterator.forEachRemaining(Spliterators.java:1801)  
at java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:482)  
at java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:472)  
at java.util.stream.ForEachOps$ForEachOp.evaluateSequential(ForEachOps.java:151)  
at java.util.stream.ForEachOps$ForEachOp$OfRef.evaluateSequential(ForEachOps.java:174)  
at java.util.stream.AbstractPipeline.evaluate(AbstractPipeline.java:234)  
at java.util.stream.ReferencePipeline.forEach(ReferencePipeline.java:418)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestExecutor.lambda$execute$3(HierarchicalTestExecutor.java:92)  
at org.junit.platform.engine.support.hierarchical.SingleTestExecutor.executeSafely(SingleTestExecutor.java:66)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestExecutor.execute(HierarchicalTestExecutor.java:77)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestExecutor.execute(HierarchicalTestExecutor.java:51)  
at org.junit.platform.engine.support.hierarchical.HierarchicalTestEngine.execute(HierarchicalTestEngine.java:43)  
at org.junit.platform.launcher.core.DefaultLauncher.execute(DefaultLauncher.java:170)  
at org.junit.platform.launcher.core.DefaultLauncher.execute(DefaultLauncher.java:154)  
at org.junit.platform.launcher.core.DefaultLauncher.execute(DefaultLauncher.java:90)  
at org.eclipse.jdt.internal.junit5.runner.JUnit5TestReference.run(JUnit5TestReference.java:86)  
at org.eclipse.jdt.internal.junit.runner.TestExecution.run(TestExecution.java:38)  
at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.runTests(RemoteTestRunner.java:538)  
at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.runTests(RemoteTestRunner.java:760)  
at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.run(RemoteTestRunner.java:460)  
at org.eclipse.jdt.internal.junit.runner.RemoteTestRunner.main(RemoteTestRunner.java:206)

Solution:

Please check edam-system-config package installed or not.

**The list of drop-down properties not to be in synch**

The synchronization does not happen between metadata schema editor to search facets for all CRUD operations on the configured drop-down properties.

**Checklist:**

Navigate to AEM web console (i.e. \[hostname\]:\[portnumber\]/system/console/configMgr)

Search for Metadata schema update exclusion of dropdown property names config and on edit.

Those dropdowns property are should configure in the config manager.

### TRISUL-571 & TRISUL-705 : User View - Customize Download Dialog with Rendition Picker, Presets, permissions

**Exception**:  
com.wsgc.ecommerce.edam.core.exceptions.DownloadAssetRenditionsException: An error occured in getImageRenditons method of CreateAssetRenditionsServlet :: {}  
at com.wsgc.ecommerce.edam.core.servlets.CreateAssetRenditionsServlet.getImageRenditons(CreateAssetRenditionsServlet.java:219)  
at com.wsgc.ecommerce.edam.core.servlets.CreateAssetRenditionsServlet.doPost(CreateAssetRenditionsServlet.java:130)  
Caused by: com.wsgc.ecommerce.edam.core.exceptions.CommandLineProcessTimeOutException: An error occured in CreateAssetRenditionsServlet execute: failed to creating asset rendition Execute command line \[convert, -alpha, off, ./9727ca06-aba6-4ca3-854b-bbdcc392394c\[0\], -colorspace, "ICC 2014", -profile, /etc/ImageMagick-6/sRGB2014.icc, -resize, 500x500, "a 711abcd efbcd efgh ijjkl imno pqr stu1 vwxyzabcd efgh ijjkl imno pqr stu2 vwxyz abcd efgh ijjkl imno pqr stu3 vwxyz abcd efgh ijjkl imno pqr stu345 a 3abcd efbcd efgh ij34jkl imno pqr stu1 vwxyzabcd 45efg.JPEG"\] for asset /content/dam/west-elm/a 711abcd efbcd efgh ijjkl imno pqr stu1 vwxyzabcd efgh ijjkl imno pqr stu2 vwxyz abcd efgh ijjkl imno pqr stu3 vwxyz abcd efgh ijjkl imno pqr stu345 a 3abcd efbcd efgh ij34jkl imno pqr stu1 vwxyzabcd 45efg.TIF.  
at com.wsgc.ecommerce.edam.core.servlets.CreateAssetRenditionsServlet.runCommandLineProcess(CreateAssetRenditionsServlet.java:251)  
at com.wsgc.ecommerce.edam.core.servlets.CreateAssetRenditionsServlet.getImageRenditons(CreateAssetRenditionsServlet.java:216)  
... 129 more  
Caused by: org.apache.commons.exec.ExecuteException: Process exited with an error: 1 (Exit value: 1)  
at org.apache.commons.exec.DefaultExecutor.executeInternal(DefaultExecutor.java:404)  
at org.apache.commons.exec.DefaultExecutor.execute(DefaultExecutor.java:166)  
at org.apache.commons.exec.DefaultExecutor.execute(DefaultExecutor.java:153)  
at com.wsgc.ecommerce.edam.core.servlets.CreateAssetRenditionsServlet.runCommandLineProcess(CreateAssetRenditionsServlet.java:249)  
... 130 more

**Solution**: 

[http://localhost:4502/conf/global/settings/dam/renditionprofileconfiguration/renditionProfileConfigurationList](http://localhost:4502/conf/global/settings/dam/renditionprofileconfiguration/renditionProfileConfigurationList).

Go to \[host\]:\[port\]/conf/global/settings/dam/renditionprofileconfiguration/renditionProfileConfigurationList.html

Select which rendition profile you selected for downloading the image rendition and click on edit.

Check the image magick command format and give the proper image magick command.

Example Image magick commands : -resize "2000x2000" or -quality 90 -resize "1000x1000"

**Exception**:

13.02.2021 02:30:02.849 \*ERROR\* \[10.170.18.43 \[1613212202842\] POST /bin/currentuser/download/rendition/profiles HTTP/1.1\] org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught Throwable  
java.lang.NullPointerException: null

**Solution:**

Please check the request header, Selected assets path list must contain an asset path.

Go to \[host\]:\[port\]/system/console/components find out the "CurrentUserAssetRenditonProfilesServlet" and check component is active or not.  If the component is not in an active state then check the references.

**Exception**:

Cannot serve request to /bin/currentuser/asset/download/permissions in com.wsgc.ecommerce.edam.core.servlets.CurrentUserAssetDownloadPermissionsServlet

Exception:  
java.lang.NullPointerException  
at java.util.Objects.requireNonNull(Unknown Source)  
at java.util.Arrays$ArrayList.<init>(Unknown Source)  
at java.util.Arrays.asList(Unknown Source)  
at com.wsgc.ecommerce.edam.core.services.impl.AssetReditionProfilesServiceImpl.getAssetPathsFromJson(AssetReditionProfilesServiceImpl.java:421)  
at com.wsgc.ecommerce.edam.core.servlets.CurrentUserAssetDownloadPermissionsServlet.doPost(CurrentUserAssetDownloadPermissionsServlet.java:66)  
at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146)  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342)  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374)  
at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552)  
at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44)  
at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82)

**Solution**:

Go to \[host\]:\[port\]/system/console/components find out the "CurrentUserAssetDownloadPermissionsServlet" and check component is active or not.  If the component is not in an active state then check the references.

Please check the request header, Selected assets path list must contain an asset path and uuid. 

**Exception**:  
com.wsgc.ecommerce.edam.core.exceptions.DownloadAssetRenditionsException: An error occured in getAssetRendition method of AssetReditionProfilesServiceImpl ::  
at com.wsgc.ecommerce.edam.core.services.impl.AssetReditionProfilesServiceImpl.getAssetRendition(AssetReditionProfilesServiceImpl.java:406)  
at com.wsgc.ecommerce.edam.core.servlets.CreateAssetRenditionsServlet.doPost(CreateAssetRenditionsServlet.java:153)  
Caused by:  [java.io](http://java.io/).FileNotFoundException:  
at  [java.io](http://java.io/).FileInputStream.open0(Native Method)  
at  [java.io](http://java.io/).FileInputStream.open(Unknown Source)  
at  [java.io](http://java.io/).FileInputStream.<init>(Unknown Source)  
at com.wsgc.ecommerce.edam.core.services.impl.AssetReditionProfilesServiceImpl.getAssetRendition(AssetReditionProfilesServiceImpl.java:398)

**Solution**:

Please check the request header, Selected assets path list must contain an asset path.

**Exception**:

Cannot serve request to /bin/currentuser/download/rendition/profiles  in com.wsgc.ecommerce.edam.core.servlets.CurrentUserAssetRenditonProfilesServlet

Exception:  
java.lang.NullPointerException  
at java.util.Objects.requireNonNull(Unknown Source)  
at java.util.Arrays$ArrayList.<init>(Unknown Source)  
at java.util.Arrays.asList(Unknown Source)  
at com.wsgc.ecommerce.edam.core.services.impl.AssetReditionProfilesServiceImpl.getAssetPathsFromJson(AssetReditionProfilesServiceImpl.java:421)  
at com.wsgc.ecommerce.edam.core.servlets.CurrentUserAssetDownloadPermissionsServlet.doPost(CurrentUserAssetDownloadPermissionsServlet.java:66)  
at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146)  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342)  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374)  
at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552)

**Solution**:

Go to \[host\]:\[port\]/system/console/components find out the "CurrentUserAssetRenditonProfilesServlet" and check component is active or not.  If the component is not in an active state then check the references.

Please check the request header, Selected assets path list must contain an asset path.

**Error message**:

After selecting the images click on the "Download" if you see any dialog saying that " **Sorry, you do not have privileges to download the following assets: Test.jpg** ". This means you don't have permission to download a particular rendition.

**Error message**:

After selecting the images click on the "Download" if you see any dialog saying that "**You do not have permissions to download the JPEG 200x200 rendition for the following assets: Test1.jpg Would you like to continue with the remaining 1 assets ?**". This means you don't have permission to download a particular rendition.

**Error message**: 

After selecting the images click on the "Download" if you see any dialog saying that "**Sorry, there was an error preparing your files for download. Please try again later.**" This means the admin needs to provide proper configuration details in the admin view. 

**Solution**: 

Go to \[host\]:\[port\]/conf/global/settings/dam/renditionprofileconfiguration/renditionProfileConfigurationList.html

Select which rendition profile you selected for downloading the image rendition and click on edit.

Check the image magick command format and give the proper image magick command.

Example Image magick commands : -resize "2000x2000" or -quality 90 -resize "1000x1000"

### TRISUL-350, TRISUL-344 - Retrofit WSI Schema

When we open an image properties and if the Summary Tab is empty and in the edam.log if we are observing the following exception :

Exception :

17.02.2021 10:13:46.604 \*ERROR\* \[0:0:0:0:0:0:0:1 \[1613537026260\] GET /bin/edam/summarytab HTTP/1.1\] com.wsgc.ecommerce.edam.core.servlets.SummaryTabServlet Error while getting node with exception : Login Failure: all modules ignored  
javax.jcr.LoginException: Login Failure: all modules ignored

Caused by: javax.security.auth.login.LoginException: Login Failure: all modules ignored  
at javax.security.auth.login.LoginContext.invoke(LoginContext.java:906)  
at javax.security.auth.login.LoginContext.access$000(LoginContext.java:195)  
at javax.security.auth.login.LoginContext$4.run(LoginContext.java:682)  
at javax.security.auth.login.LoginContext$4.run(LoginContext.java:680)  
at java.security.AccessController.doPrivileged(Native Method)  
at javax.security.auth.login.LoginContext.invokePriv(LoginContext.java:680)  
at javax.security.auth.login.LoginContext.login(LoginContext.java:587)  
at org.apache.jackrabbit.oak.core.ContentRepositoryImpl.login(ContentRepositoryImpl.java:163) \[org.apache.jackrabbit.oak-core:1.10.3\]  
at org.apache.jackrabbit.oak.jcr.repository.RepositoryImpl.login(RepositoryImpl.java:282) \[org.apache.jackrabbit.oak-jcr:1.10.3\]  
... 141 common frames omitted

Solution :   System User Package is not installed in the instance . Go to \[host\]:\[port\]/crx/packmgr/index.jsp) upload the   **ui.system.user-1.0.2.zip**  and you can refresh the image properties on Summary Tab now you can find the properties .

**Any Image Properties are missing on the Summary Tab .**

If any of the existing Image properties are missing on the Summary Tab , Go to \[host\]:\[port\]/system/console/configMgr) search for the Summary tab configurations and in the Summary tab values add the image property with correct format example\[wsi property(wsi:is-cgi)=Title of the property(Is CGI)#Table ID(Photography)\] .

### TRISUL-344 Trisul-350 Trisul-857 Trisul-858 Applying Rules Metadata Cascading

**How to Apply rules for the image properties :**

**Manually adding newly values for drop downs :** 

Under Tools section click on Assets click on metadata schema edit the wsi schema : 

In WSI Schema Template 

![](troubleshootingimages/image017.png?raw=true)

For any of the Image property we need to add drop down value click on the asset property  in the Settings tab under the Add manually choices click add and enter the label and the value.

**For which brands that newly added drop down value should be seen :** 

Based on the requirement for example the newly added drop down value should be visible based on the brand value , click on the rules tab and in the rules click on based on choices rules and in that we can add the rules for which brand the newly added drop down value should appear .

![](troubleshootingimages/image018.png?raw=true)

**Rules can we apply for the Image property :**

**Multi values Field :** If any of the single drop down value if the requirement is to change the single drop down field to multi valued drop down  then for the image property in the rules check on multi value field then the drop down will change to multi values drop down .

![](troubleshootingimages/image019.png?raw=true)

**Requirement :** For any of the image property based on the requirement if that property is non mandatory the we can check the non required option and if that property is required for all the brands then check on the required option and if that property is required only for some brands and not required for the some brands then check on the required based on new rule option.

![](troubleshootingimages/image020.png?raw=true)

Add rule based on the brand is it required or not .

**Visibility :** Based on the requirement if that property is visible for all the brands check on the visible option and if that property need to visible for only some brands then we need to check on visibile based on new rule option.

![](troubleshootingimages/image021.png?raw=true)

Add the rule based on which property it is visible.

**Choices :**  This rule applicable only for the drop down fields , If all the drop down values should appear on image properties check on Based on field settings and  ,if the drop down values are dependent on any other drop downs check on based on new rule .

![](troubleshootingimages/image022.png?raw=true)

### TRISUL-885 TRISUL-886 Setup Groups and Permissions

[https://jira.wsgc.com/browse/TRISUL-885](https://jira.wsgc.com/browse/TRISUL-885)  - MG Rollout - Setup Groups and Permissions

[https://jira.wsgc.com/browse/TRISUL-886](https://jira.wsgc.com/browse/TRISUL-886)  - RJ Rollout - Setup Groups and Permissions

1 . For MG and RJ Brands If any of the user trying to log in if the user is not able to access the /content/dam and observed the following exception :

Exception :

Resource at '/libs/dam/gui/content/assets.html/content/dam' not found: No resource found

Cannot serve request to /assets.html/content/dam in /libs/sling/servlet/errorhandler/404.jsp

Solution :

Go to   [http://domain:port/](http://localhost:4502/system/console/configMgr)useradmin and Check whether the user is mapped to corresponding group in the useradmin , and Check if all the groups and users are mapped accordingly say user is mapped to group but group is not mapped to parent group (APR\_EDAM\_QA\_MG) and the parent User group is mapped to (APR\_EDAM\_QA\_ALL). 

On every deployment, the mappings will be lost. Ensure you map the user to the corresponding group .

2\. Impersonate is working .

Go to   [http://domain:port/](http://localhost:4502/system/console/configMgr)useradmin and check in the APR\_EDAM\_QA\_Admins User Group have the administrator user ,  and the APR\_EDAM\_QA\_ALL have the DAM USER , If the dam user is in parent group then impersonate from one user to other user will work .

3 . Unable to view approved assets for General user for MG and RJ brands:

As per the permissions both MG and RJ General User group have a permission to see only approved assets. If that particular User group is not seeing the approved assets , we have to check the configuration .

Go to   [http://domain:port/](http://localhost:4502/system/console/configMgr)system/console/configMgr search for dam metadata update listener and under approved viewers list our config paths will be there followingly :

![](troubleshootingimages/image023.png?raw=true)

4\. For any of the User is not able to download the asset :

If any of the User is not have a permission to download the asset , we need to configure that user group in Asset downloaders config under [http://domain:port/](http://localhost:4502/system/console/configMgr)system/console/configMgr . 

5\. Third Party Folder creating when user log in :

If any of the user mapped to third party group then the particular user login on fly on his name the folder will create , if this fails we need to check under the [http://domain:port/](http://localhost:4502/system/console/configMgr)system/console/configMgr .  search for the third party configurations under we have a configs like following :

![](troubleshootingimages/image024.png?raw=true)

the brand path and the folder name and the third party group are configured correctly or not , Production User will have  a access to the third party folder , we have to map in the configuration like above snap shot .

### TRISUL-661 : Add "Keywords" Metadata to "Overview" section

[TRISUL-661](https://jira.wsgc.com/browse/TRISUL-661)  -  Getting issue details...   STATUS   

Under the image overview section if the image properties are not there check for the class 

com.wsgc.ecommerce.edam.core.services.DropdownPropTextService .

![](troubleshootingimages/image025.png?raw=true)

Only if the value is present in jcr content only that label and the value is present under the overview section .

If we need to add new property or to delete the existing property under overview go to the path /apps/dam/gui/content/assetdetails/jcr:content/rails/properties/items/metadata/items add or del the nodes 

![](troubleshootingimages/image026.png?raw=true)  

Do not edit manually the overviewfield.jsp at /apps/dam/gui/coral/components/admin/assetdetails/info/overviewfield/overviewfield.jsp , through JSP the values are rendering under the image overview section.

If any of the image properties need to add under the overview section must and should their sling:resourceType is dam/gui/coral/components/admin/assetdetails/info/overviewfield .

![](troubleshootingimages/image027.png?raw=true)

### RM-23552 : Merchant user and General user are not able to view existing assets

**Exception**  :

19.02.2021 23:02:15.059 \*ERROR\* \[0:0:0:0:0:0:0:1 \[1613755935012\] POST /bin/edam/updateAcls HTTP/1.1\] com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet Error while adding ACLs at asset path :/content/dam/west-elm  
com.wsgc.ecommerce.edam.core.exceptions.AclException: Exception while granting privilege on path :/content/dam/west-elm/7517848\_2.jpg and principal name :APR\_EDAM\_QA\_WE\_MERCHANT,APR\_EDAM\_QA\_WE\_GENERA  
at com.wsgc.ecommerce.edam.core.services.impl.EdamAclServiceImpl.permissionsUpdate(EdamAclServiceImpl.java:202) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
at com.wsgc.ecommerce.edam.core.services.impl.EdamAclServiceImpl.addPermissions(EdamAclServiceImpl.java:127) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
at com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet.updateAclPermission(UpdateOlderAssetsAclsServlet.java:104) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
at com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet.doPost(UpdateOlderAssetsAclsServlet.java:82) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) \[org.apache.sling.api:2.20.0\]  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342) \[org.apache.sling.api:2.20.0\]  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374) \[org.apache.sling.api:2.20.0\]  
at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) \[org.apache.sling.engine:2.6.18\]  
at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) \[org.apache.sling.engine:2.6.18\]  
at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) \[org.apache.sling.engine:2.6.18\]  
at com.day.cq.wcm.core.impl.WCMDebugFilter.doFilter(WCMDebugFilter.java:156) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
at com.day.cq.wcm.core.impl.WCMComponentFilter.filterRootInclude(WCMComponentFilter.java:375) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
at com.day.cq.wcm.core.impl.WCMComponentFilter.doFilter(WCMComponentFilter.java:190) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
Caused by: com.wsgc.ecommerce.edam.core.exceptions.AclException: User principal APR\_EDAM\_QA\_WE\_MERCHANTS1,APR\_EDAM\_QA\_WE\_GENERAL1 is not present or current service user edamSystemService session cannot edit it  
at com.wsgc.ecommerce.edam.core.services.impl.EdamAclServiceImpl.permissionsUpdate(EdamAclServiceImpl.java:191) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
... 134 common frames omitted

**Solution**  :

Here issue is with group names are not correct and not available in server. Please provide correct group names and associated brand Path.

Go to \[host\]:\[port\]/system/console/configMgr. search for "EDAM Utility Configuration" and click on it and add or update "BrandPath and group Names"  field.

**Exception**  :

19.02.2021 23:13:42.808 \*ERROR\* \[0:0:0:0:0:0:0:1 \[1613756622805\] POST /bin/edam/updateAcls HTTP/1.1\] org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught Throwable  
java.lang.ArrayIndexOutOfBoundsException: 1  
at com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet.lambda$doPost$2(UpdateOlderAssetsAclsServlet.java:77) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
at java.util.stream.Collectors.lambda$toMap$58(Collectors.java:1321)  
at java.util.stream.ReduceOps$3ReducingSink.accept(ReduceOps.java:169)  
at java.util.stream.ReferencePipeline$3$1.accept(ReferencePipeline.java:193)  
at java.util.Spliterators$ArraySpliterator.forEachRemaining(Spliterators.java:948)  
at java.util.stream.AbstractPipeline.copyInto(AbstractPipeline.java:482)  
at java.util.stream.AbstractPipeline.wrapAndCopyInto(AbstractPipeline.java:472)  
at java.util.stream.ReduceOps$ReduceOp.evaluateSequential(ReduceOps.java:708)  
at java.util.stream.AbstractPipeline.evaluate(AbstractPipeline.java:234)  
at java.util.stream.ReferencePipeline.collect(ReferencePipeline.java:499)  
at com.wsgc.ecommerce.edam.core.servlets.UpdateOlderAssetsAclsServlet.doPost(UpdateOlderAssetsAclsServlet.java:77) \[com.wsgc.ecommerce.edam.core:1.0.0.SNAPSHOT\]  
at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) \[org.apache.sling.api:2.20.0\]  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:342) \[org.apache.sling.api:2.20.0\]  
at org.apache.sling.api.servlets.SlingSafeMethodsServlet.service(SlingSafeMethodsServlet.java:374) \[org.apache.sling.api:2.20.0\]  
at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) \[org.apache.sling.engine:2.6.18\]  
at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) \[org.apache.sling.engine:2.6.18\]  
at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) \[org.apache.sling.engine:2.6.18\]  
at com.day.cq.wcm.core.impl.WCMDebugFilter.doFilter(WCMDebugFilter.java:156) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) \[org.apache.sling.engine:2.6.18\]  
at com.day.cq.wcm.core.impl.WCMComponentFilter.filterRootInclude(WCMComponentFilter.java:375) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]  
at com.day.cq.wcm.core.impl.WCMComponentFilter.doFilter(WCMComponentFilter.java:190) \[com.day.cq.wcm.cq-wcm-core:5.12.102\]

**Solution**  :

Here issue is with config properties. Please check given data is correct or not like below format.

Example:  /content/dam/west-elm=APR\_EDAM\_QA\_WE\_MERCHANTS,APR\_EDAM\_QA\_WE\_GENERAL

Go to \[host\]:\[port\]/system/console/configMgr. search for "EDAM Utility Configuration" and click on it and add or update "BrandPath and group Names"  field.

### Guide for Asset Migration from Legacy to EDAM

 **1. Command to trigger the migration script (Example Included)**

 **2. Possible Exceptions and Errors**

**1.** **Command to trigger the migration script (Example Included)** 

This step shows the command to trigger the script

1. Format:

<path of script>$./<script\_name.sh> <source server with port number> <source server username> <source server password> <destination server with port number> <destination server username> <destination server password> <source server path to be migrated> <destination server path to be stored at> <batch size> <throttle value> <crx-quickstart path> &

Example: ./migrationscript.sh damqark1p:38781 admin admin  [aemrck-vicn002.wsgc.com](http://aemrck-vicn002.wsgc.com/):4501 admin admin content/dam/ws/2010/winter content/dam/williams-sonoma/2010/winter 1000 5 /apps/edam/aem-primary/crx-quickstart &

**2.** **Possible Exception and Errors**

1.  If any argument is missed or ordering is missed, the script will not run properly and you will get various errors and the migration process will not trigger.
2.  If you give wrong port or server names, connection will not be established for the command and we will get connection exception
3.  if paths does not exist, we will get path not found error and script will terminate.
4.  You can see various errors in the same place where you run the command for these scenarios. So please make sure to give proper arguments and in the same order.
5.  Once script execution starts, a log file name will be displayed on screen where logs will be rolled. Also a file with name  **'IgnoredFiles.log'**  will be created where the skipped file paths will be written.
6.  As soon as you see the log file name on screen, migrate to the log and tail the log for entries.
7.  If any exception occurs in the migration process, the script will capture it and re run the migration script by resuming from that particular path. In this process, the skipped/error-ed path will be written to  **IgnoredFiles.log**  file.
8.  This continues till all files are migrated and errored files are logged.
9.  After this, script will try to migrate error files by reading the  **IgnoredFiles.log**.
10.  Once operation is completed, logs rolling will stop and process will be completed.

For Ignored/Skipped files, please refer '**IgnoredFiles.log**' file. You can manually migrate these files at a later stage.

If any session closes or your console is timed out, process may be stopped sometimes. So the '&' symbol at the end of command makes sure you do not encounter these session timeouts.

Even if your command line session times out, you can still check for the process by typing  **'ps -ef | grep java'** to check the process ID running. If you see the migration script going into infinite loop or unresponsive, you can get the process ID and kill the process using '**Kill -9 <process ID>**' . Re run the migration script after you kill the process.

If your server goes down due to memory issues, please raise a ticket to bring the server up and re run the script.

**Possible Exceptions:**

1.  **NullPointerException:** This Exception will occur in certain files during the migration process. We have handled this in the script and adding the files to the **IgnoredFiles.log**  to be able to check later and migrate.
2.  **InvalidItemStateException:** This Exception will occur in certain files during the migration process. We are excluding such nodes in the vlt command as they are not relevant to actual asset and metadata like rep:policy nodes.
3.  **GC OverHead Limit/OutOfMemoryError :** This occurs when most of the CPU space is taken for Garbage Collection. To fix this, Increase the  **maximum**  heap size to a number that is suitable by updating the heap params.
4.  **RepositoryException:** javax.jcr.RepositoryException:  [java.io](http://java.io/).IOException: No space left on device . /tmp memory becomes full. Sometimes log takes too much space and fill up the server space. We need to restart the server and increase log space and /tmp space if required and restart the migration process.
5.  **PathNotFoundException :** This occurs when the path given to migrate does not exist on the source server. Make sure to check the proper path and arguments in the script trigger and re run the migration process.
