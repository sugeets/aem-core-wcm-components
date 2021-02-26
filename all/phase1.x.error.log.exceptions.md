

<div class="WordSection1">

<h1>EDAM 1.x Error Log Exceptions</h1>

<div>

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" style="border-collapse: collapse; border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: initial; border-right-style: none; border-right-width: initial; border-bottom-color: initial; border-bottom-style: none; border-bottom-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial;">
 <colgroup><col style="width: 50px;"><col style="width: 3608px;"><col style="width: 60px;"><col style="width: 57px;"><col style="width: 73px;"><col style="width: 282px;"></colgroup>
 <tbody><tr style="page-break-inside: avoid;">
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>SNO</p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Exception</p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>WSGC</p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>OOTB</p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Overlaid</p>
  </td>
  <td style="border-top-color: windowtext; border-top-style: solid; border-top-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: initial; border-left-style: none; border-left-width: initial; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Root Cause</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>1.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>03.02.2021 10:08:49.050 *ERROR* [qtp659164676-1907] org.apache.felix.http.jetty Exception while processing request to /crx/de/endorsed/extjs/ext-all-debug.js (<a href="http://org.eclipse.jetty.io">org.eclipse.jetty.io</a>.EofException)<br>
  <a href="http://org.eclipse.jetty.io">org.eclipse.jetty.io</a>.EofException: null&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at <a href="http://org.eclipse.jetty.io">org.eclipse.jetty.io</a>.ChannelEndPoint.flush(ChannelEndPoint.java:284) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at <a href="http://org.eclipse.jetty.io">org.eclipse.jetty.io</a>.WriteFlusher.flush(WriteFlusher.java:393) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at <a href="http://org.eclipse.jetty.io">org.eclipse.jetty.io</a>.WriteFlusher.completeWrite(WriteFlusher.java:349) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at <a href="http://org.eclipse.jetty.io">org.eclipse.jetty.io</a>.ChannelEndPoint$3.run(ChannelEndPoint.java:132) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.eclipse.jetty.util.thread.strategy.EatWhatYouKill.runTask(EatWhatYouKill.java:333) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.eclipse.jetty.util.thread.strategy.EatWhatYouKill.doProduce(EatWhatYouKill.java:295) [org.apache.felix.http.jetty:4.0.8]</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is a product level exception which is being thrown upon network
  slowness while opening CRXDE or package manager.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>2.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>03.02.2021 10:12:16.985 *ERROR* [10.174.68.57 [1612375936089] GET /assets.html/content/dam/west-elm HTTP/1.1] com.day.cq.wcm.tags.IncludeTag Error while executing script quickActions.jsp<br>
org.apache.sling.api.scripting.ScriptEvaluationException: org.apache.sling.scripting.jsp.jasper.JasperException: Unable to compile class for JSP:<br>
An error occurred at line: 57 in the jsp file: /apps/dam/gui/coral/components/admin/contentrenderer/card/asset/quickActions.jsp<br>
IS_LIVE_COPY cannot be resolved to a variable<br>
54: boolean canUseRestricedActions = isSubAsset ? (!isParentAssetCheckedOut || isParentAssetCheckedOutByCurrentUser) : (!isCheckedOut || isCheckedOutByCurrentUser);<br>
55: String escapedResourcePath = (Text.escape(resourcePath)).replaceAll("%2f","/");<br>
56: boolean isDownloadable = request.getAttribute(IS_DOWNLOADABLE) != null ? (Boolean.parseBoolean(request.getAttribute(IS_DOWNLOADABLE).toString())) : true;<br>
57: boolean isLiveCopy = request.getAttribute(IS_LIVE_COPY) != null ? (boolean) request.getAttribute(IS_LIVE_COPY) : false;<br>
58: boolean hasSimSearchFeatures = request.getAttribute(HAS_FEATURES) != null ? (Boolean.parseBoolean(request.getAttribute(HAS_FEATURES).toString())) : true;<br>
59: boolean canFindSimilar = request.getAttribute(CAN_FINDSIMILAR) != null ? (Boolean.parseBoolean(request.getAttribute(CAN_FINDSIMILAR).toString())) : false;<br>
60: %&gt;<br>
An error occurred at line: 57 in the jsp file: /apps/dam/gui/coral/components/admin/contentrenderer/card/asset/quickActions.jsp<br>
IS_LIVE_COPY cannot be resolved to a variable<br>
54: boolean canUseRestricedActions = isSubAsset ? (!isParentAssetCheckedOut || isParentAssetCheckedOutByCurrentUser) : (!isCheckedOut || isCheckedOutByCurrentUser);<br>
55: String escapedResourcePath = (Text.escape(resourcePath)).replaceAll("%2f","/");<br>
56: boolean isDownloadable = request.getAttribute(IS_DOWNLOADABLE) != null ? (Boolean.parseBoolean(request.getAttribute(IS_DOWNLOADABLE).toString())) : true;<br>
57: boolean isLiveCopy = request.getAttribute(IS_LIVE_COPY) != null ? (boolean) request.getAttribute(IS_LIVE_COPY) : false;<br>
58: boolean hasSimSearchFeatures = request.getAttribute(HAS_FEATURES) != null ? (Boolean.parseBoolean(request.getAttribute(HAS_FEATURES).toString())) : true;<br>
59: boolean canFindSimilar = request.getAttribute(CAN_FINDSIMILAR) != null ? (Boolean.parseBoolean(request.getAttribute(CAN_FINDSIMILAR).toString())) : false;<br>
60: %&gt;<br>
An error occurred at line: 58 in the jsp file: /apps/dam/gui/coral/components/admin/contentrenderer/card/asset/quickActions.jsp<br>
HAS_FEATURES cannot be resolved to a variable<br>
55: String escapedResourcePath = (Text.escape(resourcePath)).replaceAll("%2f","/");<br>
56: boolean isDownloadable = request.getAttribute(IS_DOWNLOADABLE) != null ? (Boolean.parseBoolean(request.getAttribute(IS_DOWNLOADABLE).toString())) : true;<br>
57: boolean isLiveCopy = request.getAttribute(IS_LIVE_COPY) != null ? (boolean) request.getAttribute(IS_LIVE_COPY) : false;<br>
58: boolean hasSimSearchFeatures = request.getAttribute(HAS_FEATURES) != null ? (Boolean.parseBoolean(request.getAttribute(HAS_FEATURES).toString())) : true;<br>
59: boolean canFindSimilar = request.getAttribute(CAN_FINDSIMILAR) != null ? (Boolean.parseBoolean(request.getAttribute(CAN_FINDSIMILAR).toString())) : false;<br>
60: %&gt;<br>
61: &lt;coral-quickactions target="_prev" alignmy="left top" alignat="left top"&gt;<br>
An error occurred at line: 58 in the jsp file: /apps/dam/gui/coral/components/admin/contentrenderer/card/asset/quickActions.jsp<br>
HAS_FEATURES cannot be resolved to a variable<br>
55: String escapedResourcePath = (Text.escape(resourcePath)).replaceAll("%2f","/");<br>
56: boolean isDownloadable = request.getAttribute(IS_DOWNLOADABLE) != null ? (Boolean.parseBoolean(request.getAttribute(IS_DOWNLOADABLE).toString())) : true;<br>
57: boolean isLiveCopy = request.getAttribute(IS_LIVE_COPY) != null ? (boolean) request.getAttribute(IS_LIVE_COPY) : false;<br>
58: boolean hasSimSearchFeatures = request.getAttribute(HAS_FEATURES) != null ? (Boolean.parseBoolean(request.getAttribute(HAS_FEATURES).toString())) : true;<br>
59: boolean canFindSimilar = request.getAttribute(CAN_FINDSIMILAR) != null ? (Boolean.parseBoolean(request.getAttribute(CAN_FINDSIMILAR).toString())) : false;<br>
60: %&gt;<br>
61: &lt;coral-quickactions target="_prev" alignmy="left top" alignat="left top"&gt;<br>
An error occurred at line: 59 in the jsp file: /apps/dam/gui/coral/components/admin/contentrenderer/card/asset/quickActions.jsp<br>
CAN_FINDSIMILAR cannot be resolved to a variable<br>
56: boolean isDownloadable = request.getAttribute(IS_DOWNLOADABLE) != null ? (Boolean.parseBoolean(request.getAttribute(IS_DOWNLOADABLE).toString())) : true;<br>
57: boolean isLiveCopy = request.getAttribute(IS_LIVE_COPY) != null ? (boolean) request.getAttribute(IS_LIVE_COPY) : false;<br>
58: boolean hasSimSearchFeatures = request.getAttribute(HAS_FEATURES) != null ? (Boolean.parseBoolean(request.getAttribute(HAS_FEATURES).toString())) : true;<br>
59: boolean canFindSimilar = request.getAttribute(CAN_FINDSIMILAR) != null ? (Boolean.parseBoolean(request.getAttribute(CAN_FINDSIMILAR).toString())) : false;<br>
60: %&gt;<br>
61: &lt;coral-quickactions target="_prev" alignmy="left top" alignat="left top"&gt;<br>
62:&nbsp;&nbsp;&nbsp;&nbsp; &lt;coral-quickactions-item icon="check" class="foundation-collection-item-activator"&gt;&lt;%= xssAPI.encodeForHTML(i18n.get("Select")) %&gt;&lt;/coral-quickactions-item&gt;<br>
An error occurred at line: 59 in the jsp file: /apps/dam/gui/coral/components/admin/contentrenderer/card/asset/quickActions.jsp<br>
CAN_FINDSIMILAR cannot be resolved to a variable<br>
56: boolean isDownloadable = request.getAttribute(IS_DOWNLOADABLE) != null ? (Boolean.parseBoolean(request.getAttribute(IS_DOWNLOADABLE).toString())) : true;<br>
57: boolean isLiveCopy = request.getAttribute(IS_LIVE_COPY) != null ? (boolean) request.getAttribute(IS_LIVE_COPY) : false;<br>
58: boolean hasSimSearchFeatures = request.getAttribute(HAS_FEATURES) != null ? (Boolean.parseBoolean(request.getAttribute(HAS_FEATURES).toString())) : true;<br>
59: boolean canFindSimilar = request.getAttribute(CAN_FINDSIMILAR) != null ? (Boolean.parseBoolean(request.getAttribute(CAN_FINDSIMILAR).toString())) : false;<br>
60: %&gt;<br>
61: &lt;coral-quickactions target="_prev" alignmy="left top" alignat="left top"&gt;<br>
62:&nbsp;&nbsp;&nbsp;&nbsp; &lt;coral-quickactions-item icon="check" class="foundation-collection-item-activator"&gt;&lt;%= xssAPI.encodeForHTML(i18n.get("Select")) %&gt;&lt;/coral-quickactions-item&gt;</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is a product level exception which is being thrown upon accessing
  quick actions bar in AEM. This particular error occurs when a variable is
  unresolved. Bad string variables should have been handled in libs core. There
  are multiple user flows to invoke this element and it needs a product level
  feature regression to identify these unused variables. Hence, cannot be fixed
  by AppDev team.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>3.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>05.02.2021 04:34:44.908 *ERROR* [10.170.17.227 [1612528454902] GET /content/dam/rejuvenation/mar/Test%20PS-AEM31.jpg.thumb.48.48.png HTTP/1.1] org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught Throwable<br>
java.lang.IllegalStateException: Committed<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.eclipse.jetty.server.HttpChannel.resetBuffer(HttpChannel.java:928) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.eclipse.jetty.server.HttpOutput.resetBuffer(HttpOutput.java:1081) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.eclipse.jetty.server.Response.resetBuffer(Response.java:1312) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.eclipse.jetty.server.Response.sendRedirect(Response.java:720) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.eclipse.jetty.server.Response.sendRedirect(Response.java:729) [org.apache.felix.http.jetty:4.0.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at javax.servlet.http.HttpServletResponseWrapper.sendRedirect(HttpServletResponseWrapper.java:136) [org.apache.felix.http.servlet-api:1.1.2]</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>48x48 is not the rendition used in EDAM. This is a OOTB rendition......
  etc.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>4.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>03.02.2021 10:07:27.976 *ERROR* [OsgiInstallerImpl] org.apache.aries.jmx.whiteboard.MBeanHolder register: Failure registering MBean org.apache.sling.engine.impl.filter.FilterProcessorMBeanImpl@26a6c0bc<br>
javax.management.InstanceAlreadyExistsException: org.apache.sling:type=engine-filter,service=com.wsgc.ecommerce.edam.core.filters.AdhocAssetShareProxyServletFilter<br>
at com.sun.jmx.mbeanserver.Repository.addMBean(Repository.java:437)<br>
at com.sun.jmx.interceptor.DefaultMBeanServerInterceptor.registerWithRepository(DefaultMBeanServerInterceptor.java:1898)<br>
at com.sun.jmx.interceptor.DefaultMBeanServerInterceptor.registerDynamicMBean(DefaultMBeanServerInterceptor.java:966)</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Issue with acs commons content package. this package not installed
  properly.</p>
  <p>Now issue is fixed.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>5.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>05.02.2021 00:00:40.738 *ERROR* [10.168.131.37 [1612512040688] GET /mnt/overlay/dam/gui/content/collections/addtocollectionwizard.external.html HTTP/1.1] org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught SlingException<br>
javax.el.ELException: Cannot convert external of type class java.lang.String to long<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.el.lang.ELSupport.coerceToNumber(ELSupport.java:300)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.el.lang.ELSupport.coerceToNumber(ELSupport.java:279)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.el.lang.ELSupport.coerceToType(ELSupport.java:410)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.el.ValueExpressionImpl.getValue(ValueExpressionImpl.java:188)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.granite.ui.components.impl.el.ExpressionResolverImpl.resolve(ExpressionResolverImpl.java:130) [com.adobe.granite.ui.commons:5.10.14]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.granite.ui.components.ExpressionHelper.get(ExpressionHelper.java:145) [com.adobe.granite.ui.commons:5.10.14]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.granite.ui.components.ExpressionHelper.get(ExpressionHelper.java:124) [com.adobe.granite.ui.commons:5.10.14]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jsp.apps.granite.ui.components.coral.foundation.masonry.masonry_jsp._jspService(masonry_jsp.java:247)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.scripting.jsp.jasper.runtime.HttpJspBase.service(HttpJspBase.java:70) [org.apache.sling.scripting.jsp:2.3.4]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at javax.servlet.http.HttpServlet.service(HttpServlet.java:725) [org.apache.felix.http.servlet-api:1.1.2]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.scripting.jsp.jasper.servlet.JspServletWrapper.service(JspServletWrapper.java:502) [org.apache.sling.scripting.</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is a product level exception which is being thrown upon network
  slowness while adding assets to collection.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>6.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>05.02.2021 00:06:59.440 *ERROR* [10.168.131.37 [1612512410841] GET /mnt/overlay/granite/ui/content/shell/omnisearch/searchresults/singleresults/searchpanel.asset.html HTTP/1.1] com.day.cq.wcm.core.impl.WCMDeveloperModeFilter Error during include of SlingRequestPathInfo: path='/libs/dam/content/predicates/omnisearch/mimetypes', selectorString='asset', extension='html', suffix='null'<br>
org.apache.sling.api.scripting.ScriptEvaluationException:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.scripting.core.impl.DefaultSlingScript.call(DefaultSlingScript.java:416) [org.apache.sling.scripting.core:2.0.56]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.scripting.core.impl.DefaultSlingScript.eval(DefaultSlingScript.java:184) [org.apache.sling.scripting.core:2.0.56]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.scripting.core.impl.DefaultSlingScript.service(DefaultSlingScript.java:491) [org.apache.sling.scripting.core:2.0.56]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) [org.apache.sling.engine:2.6.18]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) [org.apache.sling.engine:2.6.18]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) [org.apache.sling.engine:2.6.18]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.wcm.core.impl.WCMDeveloperModeFilter.doFilterWithErrorHandling(WCMDeveloperModeFilter.java:164) [com.day.cq.wcm.cq-wcm-core:5.12.102]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.wcm.core.impl.WCMDeveloperModeFilter.doFilter(WCMDeveloperModeFilter.java:135) [com.day.cq.wcm.cq-wcm-core:5.12.102]</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is a product level exception which is being thrown upon restart of
  the server.&nbsp;</p>
  <p>following the reason:</p>
  <p>"<em>Adobe Experience Manager Core WCM Components Core Bundle
  (com.adobe.cq.core.wcm.components.core)</em>" was installed but not
  active because of dependencies missing.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>7.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>05.02.2021 04:14:58.943 *ERROR* [10.170.17.227 [1612527298843] GET /mnt/overlay/dam/gui/content/assets/metadataeditor.html HTTP/1.1] libs.granite.ui.components.shell.propertiespage Unable to render properties page correctly<br>
org.apache.sling.api.scripting.ScriptEvaluationException:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.scripting.core.impl.DefaultSlingScript.call(DefaultSlingScript.java:416) [org.apache.sling.scripting.core:2.0.56]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.scripting.core.impl.DefaultSlingScript.eval(DefaultSlingScript.java:184) [org.apache.sling.scripting.core:2.0.56]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.scripting.core.impl.DefaultSlingScript.service(DefaultSlingScript.java:491) [org.apache.sling.scripting.core:2.0.56]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.engine.impl.request.RequestData.service(RequestData.java:552) [org.apache.sling.engine:2.6.18]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.engine.impl.filter.SlingComponentFilterChain.render(SlingComponentFilterChain.java:44) [org.apache.sling.engine:2.6.18]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:82) [org.apache.sling.engine:2.6.18]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.wcm.core.impl.WCMDeveloperModeFilter.doFilter(WCMDeveloperModeFilter.java:119) [com.day.cq.wcm.cq-wcm-core:5.12.102]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) [org.apache.sling.engine:2.6.18]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.wcm.core.impl.WCMDebugFilter.doFilter(WCMDebugFilter.java:138) [com.day.cq.wcm.cq-wcm-core:5.12.102]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) [org.apache.sling.engine:2.6.18]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.wcm.core.impl.WCMComponentFilter.filterRootInclude(WCMComponentFilter.java:375) [com.day.cq.wcm.cq-wcm-core:5.12.102]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.wcm.core.impl.WCMComponentFilter.doFilter(WCMComponentFilter.java:190) [com.day.cq.wcm.cq-wcm-core:5.12.102]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.engine.impl.filter.AbstractSlingFilterChain.doFilter(AbstractSlingFilterChain.java:72) [org.apache.sling.engine:2.6.18]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.wcm.core.impl.page.PageLockFilter.doFilter(PageLockFilter.java:91) [com.day.cq.wcm.cq-wcm-core:5.12.102]</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is a product level exception which is being thrown upon restart of
  the server.&nbsp;</p>
  <p>following the reason:</p>
  <p>"<em>Adobe Experience Manager Core WCM Components Core Bundle
  (com.adobe.cq.core.wcm.components.core)</em>" was installed but not
  active because of dependencies missing.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>8.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>05.02.2021 04:14:58.944 *ERROR* [10.170.17.227 [1612527298843] GET /mnt/overlay/dam/gui/content/assets/metadataeditor.html HTTP/1.1] org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught SlingException<br>
java.lang.NullPointerException: null<br>
at com.day.cq.dam.commons.util.SchemaFormHelper.getMasterForms(SchemaFormHelper.java:124) [com.day.cq.dam.cq-dam-commons:5.12.70]<br>
at org.apache.jsp.libs.dam.gui.coral.components.admin.metadataeditor.formresourcefinder_jsp._jspService(formresourcefinder_jsp.java:302)<br>
at org.apache.sling.scripting.jsp.jasper.runtime.HttpJspBase.service(HttpJspBase.java:70) [org.apache.sling.scripting.jsp:2.3.4]<br>
at javax.servlet.http.HttpServlet.service(HttpServlet.java:725) [org.apache.felix.http.servlet-api:1.1.2]<br>
at org.apache.sling.scripting.jsp.jasper.servlet.JspServletWrapper.service(JspServletWrapper.java:502) [org.apache.sling.scripting.jsp:2.3.4]<br>
at org.apache.sling.scripting.jsp.jasper.servlet.JspServletWrapper.service(JspServletWrapper.java:449) [org.apache.sling.scripting.jsp:2.3.4]<br>
at org.apache.sling.scripting.jsp.JspScriptEngineFactory.callJsp(JspScriptEngineFactory.java:342) [org.apache.sling.scripting.jsp:2.3.4]<br>
at org.apache.sling.scripting.jsp.JspScriptEngineFactory.access$100(JspScriptEngineFactory.java:97) [org.apache.sling.scripting.jsp:2.3.4]<br>
at org.apache.sling.scripting.jsp.JspScriptEngineFactory$JspScriptEngine.eval(JspScriptEngineFactory.java:603) [org.apache.sling.scripting.jsp:2.3.4]<br>
at org.apache.sling.scripting.core.impl.DefaultSlingScript.call(DefaultSlingScript.java:388) [org.apache.sling.scripting.core:2.0.56]</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is a product level exception which is being thrown upon restart of
  the server.&nbsp;</p>
  <p>following the reason:</p>
  <p>"<em>Adobe Experience Manager Core WCM Components Core Bundle
  (com.adobe.cq.core.wcm.components.core)</em>" was installed but not
  active because of dependencies missing.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>9.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>03.02.2021 11:07:14.416 *ERROR* [OsgiInstallerImpl] com.adobe.acs.acs-aem-commons-bundle bundle com.adobe.acs.acs-aem-commons-bundle:4.4.0 (588)[com.adobe.acs.commons.replication.packages.automatic.impl.ConfigurationUpdateListener(3459)] : The activate method has thrown an exception (java.lang.NullPointerException)<br>
java.lang.NullPointerException: null<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.acs.commons.util.ResourceServiceManager.refreshCache(ResourceServiceManager.java:142) [com.adobe.acs.acs-aem-commons-bundle:4.4.0]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.acs.commons.util.ResourceServiceManager.activate(ResourceServiceManager.java:74) [com.adobe.acs.acs-aem-commons-bundle:4.4.0]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at java.lang.reflect.Method.invoke(Method.java:498)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod.invokeMethod(BaseMethod.java:228) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod.access$500(BaseMethod.java:41) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod$Resolved.invoke(BaseMethod.java:664) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod.invoke(BaseMethod.java:510) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.ActivateMethod.invoke(ActivateMethod.java:317) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.ActivateMethod.invoke(ActivateMethod.java:307) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.manager.SingleComponentManager.createImplementationObject(SingleComponentManager.java:340) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.manager.SingleComponentManager.createComponent(SingleComponentManager.java:114) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.manager.SingleComponentManager.getService(SingleComponentManager.java:982) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.manager.SingleComponentManager.getServiceInternal(SingleComponentManager.java:955) [org.apache.felix.scr:2.1.16]</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Issue with acs commons content package. this package not installed
  properly.</p>
  <p>Now issue is fixed.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>10.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>03.02.2021 11:07:14.418 *ERROR* [OsgiInstallerImpl] org.apache.aries.jmx.whiteboard.JmxWhiteboardSupport registerMBean: Cannot register MBean service null with MBean servers: Not an instanceof DynamicMBean or not MBean spec compliant standard MBean<br>
03.02.2021 11:07:14.418 *ERROR* [FelixDispatchQueue] org.apache.aries.jmx.whiteboard FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null. (Component: com.adobe.acs.commons.replication.packages.automatic.impl.ConfigurationUpdateListener (3459)))<br>
org.osgi.framework.ServiceException: Service factory returned null. (Component: com.adobe.acs.commons.replication.packages.automatic.impl.ConfigurationUpdateListener (3459))<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.framework.ServiceRegistrationImpl.getFactoryUnchecked(ServiceRegistrationImpl.java:381)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.framework.ServiceRegistrationImpl.getService(ServiceRegistrationImpl.java:248)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.framework.ServiceRegistry.getService(ServiceRegistry.java:350)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.framework.Felix.getService(Felix.java:3954)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.framework.BundleContextImpl.getService(BundleContextImpl.java:450)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.osgi.util.tracker.ServiceTracker.addingService(ServiceTracker.java:416)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.aries.jmx.whiteboard.Activator$MBeanTracker.addingService(Activator.java:101) [org.apache.aries.jmx.whiteboard:1.2.0]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.osgi.util.tracker.ServiceTracker$Tracked.customizerAdding(ServiceTracker.java:943)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.osgi.util.tracker.ServiceTracker$Tracked.customizerAdding(ServiceTracker.java:871)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.osgi.util.tracker.AbstractTracked.trackAdding(AbstractTracked.java:256)</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is a product level exception which is being thrown upon restart of
  the server.&nbsp;</p>
  <p>&nbsp;</p>
  <p>This will be resolved by starting the event admin bundle which will
  automatically start once AEM server is up.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>11.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>03.02.2021 11:07:15.627 *ERROR* [OsgiInstallerImpl] com.adobe.acs.acs-aem-commons-bundle bundle com.adobe.acs.acs-aem-commons-bundle:4.4.0 (588)[com.adobe.acs.commons.workflow.impl.WorkflowPackageManagerImpl(3595)] : The activate method has thrown an exception (java.lang.IllegalStateException: org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.acs.acs-aem-commons-bundle [588] and sub service workflowpackagemanager-service)<br>
java.lang.IllegalStateException: org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.acs.acs-aem-commons-bundle [588] and sub service workflowpackagemanager-service<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.acs.commons.workflow.impl.WorkflowPackageManagerImpl.activate(WorkflowPackageManagerImpl.java:298) [com.adobe.acs.acs-aem-commons-bundle:4.4.0]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at java.lang.reflect.Method.invoke(Method.java:498)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod.invokeMethod(BaseMethod.java:228) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod.access$500(BaseMethod.java:41) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod$Resolved.invoke(BaseMethod.java:664) [org.apache.felix.scr:2.1.16]</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Issue with acs commons content package. this package not installed
  properly.</p>
  <p>Now issue is fixed.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>12.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>03.02.2021 11:22:44.982 *ERROR* [FelixStartLevel] com.adobe.acs.commons.replication.packages.automatic.impl.ConfigurationUpdateListener Exception allocating resource resolver<br>
org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.acs.acs-aem-commons-bundle [588] and sub service automatic-package-replicator<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.resourceresolver.impl.ResourceResolverFactoryImpl.getServiceResourceResolver(ResourceResolverFactoryImpl.java:79) [org.apache.sling.resourceresolver:1.6.8]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.acs.commons.replication.packages.automatic.impl.ConfigurationUpdateListener.getResourceResolver(ConfigurationUpdateListener.java:96) [com.adobe.acs.acs-aem-commons-bundle:4.4.0]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.acs.commons.replication.packages.automatic.impl.ConfigurationUpdateListener.getResourceResolver(ConfigurationUpdateListener.java:106) [com.adobe.acs.acs-aem-commons-bundle:4.4.0]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.acs.commons.util.ResourceServiceManager.refreshCache(ResourceServiceManager.java:140) [com.adobe.acs.acs-aem-commons-bundle:4.4.0]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.adobe.acs.commons.util.ResourceServiceManager.activate(ResourceServiceManager.java:74) [com.adobe.acs.acs-aem-commons-bundle:4.4.0]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at java.lang.reflect.Method.invoke(Method.java:498)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod.invokeMethod(BaseMethod.java:228) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod.access$500(BaseMethod.java:41) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod$Resolved.invoke(BaseMethod.java:664) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.BaseMethod.invoke(BaseMethod.java:510) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.ActivateMethod.invoke(ActivateMethod.java:317) [org.apache.felix.scr:2.1.16]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.felix.scr.impl.inject.methods.ActivateMethod.invoke(ActivateMethod.java:307) [org.apache.felix.scr:2.1.16]</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Issue with acs commons content package. this package not installed
  properly.</p>
  <p>Now issue is fixed.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>13.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"><pre>12.02.2021 02:29:21.049 *ERROR* [10.174.69.227 [1613125761032] POST /content/dam/collections.collection.html HTTP/1.1] com.day.cq.dam.core.impl.collection.DamCollectionManager Repository Exception while creating collection<br>
javax.jcr.AccessDeniedException: Access denied.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jackrabbit.oak.jcr.security.AccessManager.checkPermissions(AccessManager.java:71) [org.apache.jackrabbit.oak-jcr:1.10.3]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jackrabbit.oak.jcr.session.NodeImpl$5.perform(NodeImpl.java:298) [org.apache.jackrabbit.oak-jcr:1.10.3]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jackrabbit.oak.jcr.session.NodeImpl$5.perform(NodeImpl.java:267) [org.apache.jackrabbit.oak-jcr:1.10.3]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jackrabbit.oak.jcr.delegate.SessionDelegate.perform(SessionDelegate.java:207) [org.apache.jackrabbit.oak-jcr:1.10.3]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jackrabbit.oak.jcr.session.ItemImpl.perform(ItemImpl.java:112) [org.apache.jackrabbit.oak-jcr:1.10.3]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jackrabbit.oak.jcr.session.NodeImpl.addNode(NodeImpl.java:267) [org.apache.jackrabbit.oak-jcr:1.10.3]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jackrabbit.commons.JcrUtils.getOrCreateByPath(JcrUtils.java:1616) [org.apache.jackrabbit.jackrabbit-jcr-commons:2.18.2]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jackrabbit.commons.JcrUtils.getOrCreateByPath(JcrUtils.java:1470) [org.apache.jackrabbit.jackrabbit-jcr-commons:2.18.2]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.jackrabbit.commons.JcrUtils.getOrCreateByPath(JcrUtils.java:1371) [org.apache.jackrabbit.jackrabbit-jcr-commons:2.18.2]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.dam.core.impl.collection.DamCollectionManager.createCollection(DamCollectionManager.java:175) [com.day.cq.dam.cq-dam-core:5.12.194]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.dam.core.impl.collection.DamCollectionManager.createCollection(DamCollectionManager.java:133) [com.day.cq.dam.cq-dam-core:5.12.194]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at com.day.cq.dam.core.impl.servlet.ResourceCollectionServlet.doPost(ResourceCollectionServlet.java:226) [com.day.cq.dam.cq-dam-core:5.12.194]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at org.apache.sling.api.servlets.SlingAllMethodsServlet.mayService(SlingAllMethodsServlet.java:146) [org.apache.sling.api:2.20.0]</pre></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is permission issue.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>14.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">12.02.2021 00:26:35.496 *ERROR* [qtp1199066084-1737]
  com.adobe.acs.commons.workflow.impl.WorkflowPackageManagerImpl Cannot
  determine bucket path for WorkflowPackageManager, do not activate this
  serviceorg.apache.sling.api.resource.LoginException: Cannot derive user name
  for bundle com.adobe.acs.acs-aem-commons-bundle [587] and sub service
  workflowpackagemanager-service&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.sling.resourceresolver.impl.ResourceResolverFactoryImpl.getServiceResourceResolver(ResourceResolverFactoryImpl.java:79)
  [org.apache.sling.resourceresolver:1.6.8]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  at
  com.adobe.acs.commons.workflow.impl.WorkflowPackageManagerImpl.activate(WorkflowPackageManagerImpl.java:292)
  [com.adobe.acs.acs-aem-commons-bundle:4.4.0]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  at sun.reflect.NativeMethodAccessorImpl.invoke0(Native
  Method)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  at
  java.lang.reflect.Method.invoke(Method.java:498)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  at
  org.apache.felix.scr.impl.inject.methods.BaseMethod.invokeMethod(BaseMethod.java:228)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.inject.methods.BaseMethod.access$500(BaseMethod.java:41)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.inject.methods.BaseMethod$Resolved.invoke(BaseMethod.java:664)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.inject.methods.BaseMethod.invoke(BaseMethod.java:510)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.inject.methods.ActivateMethod.invoke(ActivateMethod.java:317)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.inject.methods.ActivateMethod.invoke(ActivateMethod.java:307)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.manager.SingleComponentManager.createImplementationObject(SingleComponentManager.java:340)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.manager.SingleComponentManager.createComponent(SingleComponentManager.java:114)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.manager.SingleComponentManager.getService(SingleComponentManager.java:982)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.manager.SingleComponentManager.getServiceInternal(SingleComponentManager.java:955)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.scr.impl.manager.SingleComponentManager.getService(SingleComponentManager.java:900)
  [org.apache.felix.scr:2.1.16]&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; at
  org.apache.felix.framework.ServiceRegistrationImpl.getFactoryUnchecked(ServiceRegistrationImpl.java:348)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  at org.apache.felix.framework.ServiceRegistrationImpl.getService(ServiceRegistrationImpl.java:248)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  at org.apache.felix.framework.ServiceRegistry.getService(ServiceRegistry.java:350)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  at org.apache.felix.framework.Felix.getService(Felix.java:3954)</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Issue with acs commons content package. this package not installed
  properly.</p>
  <p>Now issue is fixed.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>15.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>05.02.2021 18:42:07.541 *ERROR* [OsgiInstallerImpl]
  org.apache.sling.installer.factories.configuration.impl.ConfigInstallTask
  Exception during installation of config TaskResource(url=<a href="http://jcrinstall/apps/edam/config/com.wsgc.ecommerce.edam.core.listeners.HighResolutionImageListener.config">jcrinstall:/apps/edam/config/com.wsgc.ecommerce.edam.core.listeners.HighResolutionImageListener.config</a>,
  entity=config:com.wsgc.ecommerce.edam.core.listeners.HighResolutionImageListener,
  state=INSTALL, attributes=[org.apache.sling.installer.api.tasks.ResourceTransformer=:35:,
  service.pid=com.wsgc.ecommerce.edam.core.listeners.HighResolutionImageListener],
  digest=6beef8d4c60bbb16025cc5cbf162887) : Argument is not an array<br>
  java.lang.IllegalArgumentException: Argument is not an array</p>
  <p class="MsoNormal">&nbsp;</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>HighResolutionImageListener.config</p>
  <p>Moved to environment specific Run mode and due which still this config is
  not getting deleted when we deployed updated 1.x common configuration.</p>
  <p>Now this has fixed by updating the filter.xml</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>16.</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>*ERROR* [JobHandler: /var/workflow/instances/server0/2021-02-18/<strong>dam-xmp-writeback_</strong>161:/content/dam/west-elm/rollbacktesting/hyb-1195696-we-design-bite-midnight-blue-big-hug-rack-midnight-blue-fa19-prefall-d1-001.jpg/jcr:content/metadata]<br>
  com.day.cq.dam.core.impl.handler.xmp.NCommXMPHandler Failed to create version
  for Asset
  /content/dam/west-elm/rollbacktesting/hyb-1195696-we-design-bite-midnight-blue-big-hug-rack-midnight-blue-fa19-prefall-d1-001.jpg<br>
  java.lang.Exception: Unable to create revision.<br>
  at
  com.day.cq.dam.core.impl.AssetManagerImpl.createRevision(AssetManagerImpl.java:452)
  [com.day.cq.dam.cq-dam-cor e:5.12.194]<br>
  at com.day.cq.dam.core.impl.AssetImpl.createRevision(AssetImpl.java:443)
  [com.day.cq.dam.cq-dam-core:5.12.194]<br>
  at com.day.cq.dam.core.impl.handler.xmp.NCommXMPHandler.version(NCommXMPHandler.java:317)
  [com.day.cq.dam.cq-dam-core:5.12.194]<br>
  at
  com.day.cq.dam.core.impl.handler.xmp.NCommXMPHandler.writeXmp(NCommXMPHandler.java:225)
  [com.day.cq.dam.cq-dam-core:5.12.194]<br>
  at com.day.cq.dam.core.impl.handler.xmp.NCommXMPHandler.writeXmpMetadata(NCommXMPHandler.java:258)
  [com.day.cq.dam.cq-dam-core:5.12.194]<br>
  at
  com.day.cq.dam.core.process.XMPWritebackProcess.writeXmp(XMPWritebackProcess.java:406)
  [com.day.cq.dam.cq-dam</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>No</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>No</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is a product defect , This is coming from when DAM XMP Metadata
  Process step is enabled . This defect is observed from Phase 1.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">17</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">23.02.2021 23:05:18.973 *ERROR* [10.170.18.53
  [1614150318970] POST /bin/edam/bulkassetmetdata HTTP/1.1]
  org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught
  Throwable<br>
  com.wsgc.ecommerce.edam.core.exceptions.BulkAssetMetadataUpdateException:
  Error occured while reading schemaProperies map :
  /jcr:content/metadata/dc:creator : null<br>
  at com.wsgc.ecommerce.edam.core.servlets.BulkAssetMetadataUpdateServlet.setPropertiesToNode(BulkAssetMetadataUpdateServlet.java:205)<br>
  at
  com.wsgc.ecommerce.edam.core.servlets.BulkAssetMetadataUpdateServlet.lambda$null$1(BulkAssetMetadataUpdateServlet.java:169)<br>
  at java.lang.Iterable.forEach(Iterable.java:75)<br>
  at
  com.wsgc.ecommerce.edam.core.servlets.BulkAssetMetadataUpdateServlet.lambda$setMetadataPropertiesToAssets$2(BulkAssetMetadataUpdateServlet.java:168)<br>
  at java.lang.Iterable.forEach(Iterable.java:75)</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">No</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">No</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>Error occured while reading schemaProperies map :<strong>&nbsp;"&nbsp;</strong>BulkAssetMetadataUpdateException
  , this&nbsp;exception will get while reading the wsi metadata schema
  properties map from "MetadataSchemaPropertyTypeService" service.</p>
  <p>This error occurred duo absence of dc:creator node for the image being updated</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">18</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">23.02.2021 23:10:43.947 *ERROR* [10.170.18.53
  [1614150643670] GET
  /etc.clientlibs/dam/gui/coral/components/admin/adhocassetshare/clientlibs/shareembedded.min.js
  HTTP/1.1] com.google.javascript.jscomp
  /libs/dam/gui/coral/components/admin/adhocassetshare/clientlibs/shareembedded.js:78764:
  ERROR - Parse error. primary expression expected<br>
  totalList.push(asset?.dataset?.foundationCollectionSelectallItemsId);</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">No</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">It is related to new js shortcut es 6 and It is working
  with all the browsers supported for for es 6 as the code is implemented to
  support for es 6</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">19</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">23.02.2021 22:45:28.190 *ERROR* [10.168.17.117
  [1614149124228] GET
  /mnt/overlay/granite/ui/content/shell/omnisearch/searchresults/singleresults/searchpanel.asset.html
  HTTP/1.1] org.apache.sling.engine.impl.SlingMainServlet service: Uncaught
  Problem handling the request<br>
  <a href="http://org.eclipse.jetty.io">org.eclipse.jetty.io</a>.RuntimeIOException:
  <a href="http://org.eclipse.jetty.io">org.eclipse.jetty.io</a>.EofException
  Caused by: <a href="http://java.io">java.io</a>.IOException: Connection reset
  by peer<br>
  at <a href="http://sun.nio.ch">sun.nio.ch</a>.FileDispatcherImpl.write0(Native
  Method)<br>
  at <a href="http://sun.nio.ch">sun.nio.ch</a>.SocketDispatcher.write(SocketDispatcher.java:47)</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">No</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">No</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal"><span style="color: rgb(36, 39, 41);">The other side has abruptly
  aborted the connection in midst of a transaction. That can have many causes
  which are not controllable from the server side on</span></p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">20</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">23.02.2021 23:45:35.067 *ERROR* [10.168.17.117 [1614152735058]
  POST /bin/currentuser/download/rendition/profiles HTTP/1.1]
  org.apache.sling.engine.impl.SlingRequestProcessorImpl service: Uncaught
  Throwable<br>
  java.lang.NullPointerException: null<br>
  at <a href="http://java.io">java.io</a>.PrintWriter.write(PrintWriter.java:473)<br>
  at
  com.wsgc.ecommerce.edam.core.services.impl.AssetReditionProfilesServiceImpl.setResponse(AssetReditionProfilesServiceImpl.java:454)<br>
  at
  com.wsgc.ecommerce.edam.core.servlets.CurrentUserAssetRenditonProfilesServlet.doPost(CurrentUserAssetRenditonProfilesServlet.java:103)</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">This error comes when user logins,select a folder and
  click on download button.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">21</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>23.02.2021 23:22:54.819 *ERROR* [10.170.16.101 [1614151374744] GET
  /apps/dam/gui/coral/components/admin/renditionProfileConfigurationList/clientlib.min.js
  HTTP/1.1] com.google.javascript.jscomp
  /apps/dam/gui/coral/components/admin/renditionProfileConfigurationList/clientlib/js/style.js:26:
  ERROR - This language feature is only supported for ECMASCRIPT6 mode or
  better: let declaration.<br>
  let shadow;<br>
  ^</p>
  <p>23.02.2021 23:22:54.819 *ERROR* [10.170.16.101 [1614151374744] GET
  /apps/dam/gui/coral/components/admin/renditionProfileConfigurationList/clientlib.min.js
  HTTP/1.1] com.google.javascript.jscomp
  /apps/dam/gui/coral/components/admin/renditionProfileConfigurationList/clientlib/js/style.js:35:
  ERROR - This language feature is only supported for ECMASCRIPT6 mode or
  better: let declaration.<br>
  let children = Array.from(e.target.parentNode.parentNode.children);<br>
  ^</p>
  <p>23.02.2021 23:22:54.819 *ERROR* [10.170.16.101 [1614151374744] GET
  /apps/dam/gui/coral/components/admin/renditionProfileConfigurationList/clientlib.min.js
  HTTP/1.1] com.google.javascript.jscomp
  /apps/dam/gui/coral/components/admin/renditionProfileConfigurationList/clientlib/js/style.js:36:
  ERROR - This language feature is only supported for ECMASCRIPT6 mode or
  better: let declaration.<br>
  let check = true;<br>
  ^</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">This is written in a higher version es6 but current
  version is es5 so throwing this exception</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">22</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">23.02.2021 23:15:52.064 *ERROR* [10.170.16.101 [1614150952061]
  GET
  /mnt/overlay/dam/gui/content/reports/reportproperties.html/mnt/overlay/cq/core/content/nav/tools/assets
  HTTP/1.1] org.apache.sling.engine.impl.SlingRequestProcessorImpl service:
  Uncaught SlingException<br>
  java.lang.NullPointerException: null<br>
  at
  org.apache.jsp.libs.dam.gui.coral.components.admin.reports.reportproperties.reportproperties_jsp._jspService(reportproperties_jsp.java:197)<br>
  at
  org.apache.sling.scripting.jsp.jasper.runtime.HttpJspBase.service(HttpJspBase.java:70)
  [org.apache.sling.scripting.jsp:2.3.4]<br>
  at javax.servlet.http.HttpServlet.service(HttpServlet.java:725)
  [org.apache.felix.http.servlet-api:1.1.2]</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;"></td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>This is a product level exception which is being thrown upon restart of
  the server.&nbsp;</p>
  <p>following the reason:</p>
  <p>"<em>Adobe Experience Manager Core WCM Components Core Bundle
  (com.adobe.cq.core.wcm.components.core)</em>" was installed but not
  active because of dependencies missing.</p>
  </td>
 </tr>
 <tr style="page-break-inside: avoid;">
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-left-color: windowtext; border-left-style: solid; border-left-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">23</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>*ERROR* [qtp1614296223-3254] org.apache.felix.http.jetty Exception while
  processing request to /content/saml_login
  (com.wsgc.ecommerce.edam.core.exceptions.AuthenticationProcessorException:
  Could not impersonate user: null to system user: edamSystemService)<br>
  com.wsgc.ecommerce.edam.core.exceptions.AuthenticationProcessorException:
  Could not impersonate user: null to system user: edamSystemService</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">Yes</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">No</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p class="MsoNormal">No</p>
  </td>
  <td style="border-top-color: initial; border-top-style: none; border-top-width: initial; border-left-color: initial; border-left-style: none; border-left-width: initial; border-bottom-color: windowtext; border-bottom-style: solid; border-bottom-width: 1pt; border-right-color: windowtext; border-right-style: solid; border-right-width: 1pt; padding-top: 3.75pt; padding-right: 3.75pt; padding-bottom: 3.75pt; padding-left: 3.75pt;">
  <p>User defined custom exceptions&nbsp;​which was thrown explicitly when user
  could not impersonate .</p>
  </td>
 </tr>
</tbody></table>

<p class="MsoNormal">&nbsp;</p>

</div>

</div>




