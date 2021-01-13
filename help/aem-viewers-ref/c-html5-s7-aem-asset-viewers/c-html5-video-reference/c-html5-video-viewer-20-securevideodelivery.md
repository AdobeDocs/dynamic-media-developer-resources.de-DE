---
description: HTTP-Video-Versand
solution: Experience Manager
title: HTTP-Video-Versand
topic: Dynamic media
uuid: fd02a55a-a0f1-47a2-983f-15f296d1dbb4
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# HTTP-Video-Versand{#http-video-delivery}

>[!NOTE]
>
>Secure Video Versand gilt nur für AEM 6.2 mit der Installation von [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) und für AEM 6.1 mit der Installation von [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Sofern der Viewer in der Konfiguration funktioniert, wie zu Beginn dieses Abschnitts beschrieben, kann der veröffentlichte Video-Versand sowohl im HTTPS-Modus (sicher) als auch im HTTP-Modus (unsicher) erfolgen. In einer Standardkonfiguration folgt das Video Versand-Protokoll strikt dem Versand-Protokoll der Einbettungswebseite. Es ist jedoch möglich, HTTPS-Video-Versand zu erzwingen, unabhängig vom verwendeten Protokoll, indem die Webseite mit dem Konfigurationsattribut [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) eingebettet wird. (Beachten Sie, dass Video-Vorschauen im Autorenmodus immer sicher über HTTPS bereitgestellt werden.)

Abhängig von der Methode zum Veröffentlichen von Dynamic Media-Videos, die Sie in AEM verwenden, wird das `VideoPlayer.ssl`-Konfigurationsattribut anders angewendet, wie im Folgenden gezeigt:

* Wenn Sie ein Dynamic Media-Video mit einer URL veröffentlichen, hängen Sie `VideoPlayer.ssl` an die URL an. Um beispielsweise sicheren Video-Versand zu erzwingen, hängen Sie `&VideoPlayer.ssl=on` an das Ende des folgenden Viewer-URL-Beispiels an:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
   ```

   Siehe auch [Verknüpfen von URLs mit Ihrer Webanwendung](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Wenn Sie ein Dynamic Media-Video mit Einbettungscode veröffentlichen, fügen Sie `VideoPlayer.ssl` zur Liste anderer Viewer-Konfigurationsparameter im Einbettungscodefragment hinzu. Um beispielsweise HTTPS-Video-Versand zu erzwingen, hängen Sie `&VideoPlayer.ssl=on` wie im folgenden Beispiel an:

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

   Siehe auch [Einbetten des Videos auf einer Webseite](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

