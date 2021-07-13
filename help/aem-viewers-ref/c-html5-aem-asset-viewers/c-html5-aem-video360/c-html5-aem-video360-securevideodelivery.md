---
description: HTTPS-Videobereitstellung
solution: Experience Manager
title: HTTPS-Videobereitstellung
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 79f7e356-55d1-46e1-b85a-2e73633c9404
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# HTTPS-Videobereitstellung{#https-video-delivery}

>[!NOTE]
>
>Die sichere HTTP-Videobereitstellung gilt nur für AEM 6.2 mit der Installation von [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) und für AEM 6.1 mit der Installation von [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Sofern der Viewer in der Konfiguration funktioniert, wie am Anfang dieses Abschnitts beschrieben, kann die veröffentlichte Videobereitstellung sowohl im HTTPS-Modus (sicher) als auch im HTTP-Modus (unsicher) erfolgen. In einer Standardkonfiguration folgt das Videobereitstellungsprotokoll strikt dem Versandprotokoll der eingebetteten Webseite. Es ist jedoch möglich, die HTTPS-Videobereitstellung ohne Rücksicht auf das verwendete Protokoll zu erzwingen, indem die Webseite mit dem Konfigurationsattribut [Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md) eingebettet wird. (Beachten Sie, dass die Videovorschau im Autorenmodus immer sicher über HTTPS bereitgestellt wird.)

Je nach der Veröffentlichungsmethode für Dynamic Media-Videos, die Sie in AEM verwenden, wird das Konfigurationsattribut `Video360Player.ssl` unterschiedlich angewendet, wie im Folgenden gezeigt:

* Wenn Sie ein Dynamic Media-Video mit einer URL veröffentlichen, hängen Sie `Video360Player.ssl` an die URL an. Um beispielsweise die sichere Videobereitstellung zu erzwingen, hängen Sie `&Video360Player.ssl=on` am Ende der folgenden Viewer-URL an:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   Siehe auch [Verknüpfen von URLs mit einer Webanwendung](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Wenn Sie ein Dynamic Media-Video mit Einbettungscode veröffentlichen, fügen Sie `Video360Player.ssl` zur Liste der anderen Viewer-Konfigurationsparameter im Einbettungscode-Snippet hinzu. Um beispielsweise die HTTPS-Videobereitstellung zu erzwingen, hängen Sie `&Video360Player.ssl=on` wie im folgenden Beispiel an:

   ```
   <style type="text/css"> 
    #s7video_div.s7video360viewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7video360viewer = new s7viewers.Video360Viewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "Video360Player.ssl" : "on", 
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

   Siehe auch [Einbetten des Videos auf einer Webseite](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)
