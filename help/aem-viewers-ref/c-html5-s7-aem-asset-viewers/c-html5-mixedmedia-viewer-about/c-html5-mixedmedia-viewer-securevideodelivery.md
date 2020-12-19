---
description: 'null'
seo-description: 'null'
seo-title: HTTPS-Video-Versand
solution: Experience Manager
title: HTTPS-Video-Versand
topic: Dynamic media
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# HTTPS-Video-Versand{#https-video-delivery}

>[!NOTE]
>
>Secure Video Versand gilt nur für AEM 6.2 mit der Installation von [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) und für AEM 6.1 mit der Installation von [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Sofern der Viewer in der Konfiguration funktioniert, wie zu Beginn dieses Abschnitts beschrieben, kann der veröffentlichte Video-Versand sowohl im HTTPS-Modus (sicher) als auch im HTTP-Modus (unsicher) erfolgen. In einer Standardkonfiguration folgt das Video Versand-Protokoll strikt dem Versand-Protokoll der Einbettungswebseite. Es ist jedoch möglich, HTTPS-Video-Versand zu erzwingen, unabhängig vom verwendeten Protokoll, indem die Webseite mit dem Konfigurationsattribut [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) eingebettet wird. (Beachten Sie, dass Video-Vorschauen im Autorenmodus immer sicher über HTTPS bereitgestellt werden.)

Abhängig von der Methode zum Veröffentlichen von Dynamic Media-Videos, die Sie in AEM verwenden, wird das `VideoPlayer.ssl`-Konfigurationsattribut anders angewendet, wie im Folgenden gezeigt:

* Wenn Sie ein Dynamic Media-Video mit einer URL veröffentlichen, hängen Sie `VideoPlayer.ssl` an die URL an. Um beispielsweise sicheren Video-Versand zu erzwingen, hängen Sie `&VideoPlayer.ssl=on` an das Ende des folgenden Viewer-URL-Beispiels an:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   Siehe auch [(Verknüpfen von URLs mit Ihrer Webanwendung](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Wenn Sie ein Dynamic Media-Video mit Einbettungscode veröffentlichen, fügen Sie `VideoPlayer.ssl` zur Liste anderer Viewer-Konfigurationsparameter im Einbettungscodefragment hinzu. Um beispielsweise HTTPS-Video-Versand zu erzwingen, hängen Sie `&VideoPlayer.ssl=on` wie im folgenden Beispiel an:

   ```
   <style type="text/css"> 
    #s7mixedmedia_div.s7mixedmediaviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
   <div id="s7mixedmedia_div"></div> 
   <script type="text/javascript"> 
    var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
     "containerId" : "s7mixedmedia_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
    }).init(); 
   </script>
   ```

   Siehe auch [(Einbetten des Videos auf einer Webseite](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

