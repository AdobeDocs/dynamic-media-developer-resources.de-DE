---
description: HTTP-Videobereitstellung
solution: Experience Manager
title: HTTP-Videobereitstellung
feature: Dynamic Media Classic,Viewer,SDK/API,Video
role: Developer,User
exl-id: 33907e22-107b-4345-82bb-cad47cb7a839
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# HTTP-Videobereitstellung{#http-video-delivery}

>[!NOTE]
>
>Die sichere Videobereitstellung gilt nur für AEM 6.2 mit der Installation von [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) und für AEM 6.1 mit der Installation von [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Sofern der Viewer in der Konfiguration funktioniert, wie am Anfang dieses Abschnitts beschrieben, kann die veröffentlichte Videobereitstellung sowohl im HTTPS-Modus (sicher) als auch im HTTP-Modus (unsicher) erfolgen. In einer Standardkonfiguration folgt das Videobereitstellungsprotokoll strikt dem Versandprotokoll der eingebetteten Webseite. Es ist jedoch möglich, die HTTPS-Videobereitstellung ohne Rücksicht auf das verwendete Protokoll zu erzwingen, indem die Webseite mit dem Konfigurationsattribut [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) eingebettet wird. (Beachten Sie, dass die Videovorschau im Autorenmodus immer sicher über HTTPS bereitgestellt wird.)

Je nach der Veröffentlichungsmethode für Dynamic Media-Videos, die Sie in AEM verwenden, wird das Konfigurationsattribut `VideoPlayer.ssl` unterschiedlich angewendet, wie im Folgenden gezeigt:

* Wenn Sie ein Dynamic Media-Video mit einer URL veröffentlichen, hängen Sie `VideoPlayer.ssl` an die URL an. Um beispielsweise die sichere Videobereitstellung zu erzwingen, hängen Sie `&VideoPlayer.ssl=on` am Ende der folgenden Viewer-URL an:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
   ```

   Siehe auch [Verknüpfen von URLs mit einer Webanwendung](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Wenn Sie ein Dynamic Media-Video mit Einbettungscode veröffentlichen, fügen Sie `VideoPlayer.ssl` zur Liste der anderen Viewer-Konfigurationsparameter im Einbettungscode-Snippet hinzu. Um beispielsweise die HTTPS-Videobereitstellung zu erzwingen, hängen Sie `&VideoPlayer.ssl=on` wie im folgenden Beispiel an:

   ```
   <style type="text/css"> 
    #s7video_div.s7videoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/VideoViewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7videoviewer = new s7viewers.VideoViewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Video", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }).init(); 
   </script>
   ```

   Siehe auch [Einbetten des Videos auf einer Webseite](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
