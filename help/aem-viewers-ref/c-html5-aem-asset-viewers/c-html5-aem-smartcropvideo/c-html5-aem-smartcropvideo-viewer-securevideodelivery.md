---
title: HTTP-Videobereitstellung
description: HTTP-Videobereitstellung
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: b809a11f-3c2d-4abd-b317-fabb36245b1b
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# HTTP-Videobereitstellung{#http-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Wenn der Viewer in der Konfiguration funktioniert, wie am Anfang dieses Abschnitts beschrieben, kann die Bereitstellung veröffentlichter Videos sowohl im HTTPS-Modus (sicher) als auch im HTTP-Modus (unsicher) erfolgen. In einer Standardkonfiguration folgt das Videobereitstellungsprotokoll streng dem Bereitstellungsprotokoll der einbettenden Web-Seite. Es ist jedoch möglich, die HTTPS-Videobereitstellung unabhängig vom verwendeten Protokoll zu erzwingen, indem die Web-Seite mit dem Konfigurationsattribut [SmartCropVideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) eingebettet wird. (Die Videovorschau im Autorenmodus wird immer sicher über HTTPS bereitgestellt.)

Je nach der Methode zum Veröffentlichen von Dynamic Media-Videos, die Sie in Adobe Experience Manager verwenden, wird das `SmartCropVideoPlayer.ssl` Konfigurationsattribut anders angewendet, wie im Folgenden gezeigt:

* Wenn Sie ein Dynamic Media-Video mit einer URL veröffentlichen, hängen Sie `SmartCropVideoPlayer.ssl` an die URL an. Um beispielsweise eine sichere Videobereitstellung zu erzwingen, hängen Sie `&SmartCropVideoPlayer.ssl=on` an das Ende des folgenden Viewer-URL-Beispiels an:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/SmartCropVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&SmartCropVideoPlayer.ssl=on
  ```

  Siehe auch [Verknüpfen von URLs mit einer Web-Anwendung](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=de#dynamic).

* Wenn Sie ein Dynamic Media-Video mit Einbettungs-Code veröffentlichen, fügen Sie `SmartCropVideoPlayer.ssl` zur Liste der anderen Viewer-Konfigurationsparameter im Einbettungs-Code-Snippet hinzu. Um beispielsweise die HTTPS-Videobereitstellung zu erzwingen, hängen Sie `&SmartCropVideoPlayer.ssl=on` wie im folgenden Beispiel an:

  ```
  <style type="text/css"> 
   #s7video_div.s7videoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
  <div id="s7video_div"></div> 
  <script type="text/javascript"> 
   var s7videoviewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId" : "s7video_div", 
    "params" : {  
     "SmartCropVideoPlayer.ssl" : "on", 
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

  Siehe auch [Einbetten des Videos auf einer Web-Seite](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=de#dynamic).
