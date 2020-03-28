---
description: 'null'
seo-description: 'null'
seo-title: HTTPS-Video-Versand
solution: Experience Manager
title: HTTPS-Video-Versand
topic: Dynamic media
uuid: 68984ba1-2802-496a-8ad0-ba46b59514ad
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# HTTPS-Video-Versand{#https-video-delivery}

>[!NOTE]
>
>HTTP Secure Video Versand gilt nur für AEM 6.2 mit der Installation von [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) und für AEM 6.1 mit der Installation von [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Sofern der Viewer in der Konfiguration funktioniert, wie zu Beginn dieses Abschnitts beschrieben, kann der veröffentlichte Video-Versand sowohl im HTTPS-Modus (sicher) als auch im HTTP-Modus (unsicher) erfolgen. In einer Standardkonfiguration folgt das Video Versand-Protokoll strikt dem Versand-Protokoll der Einbettungswebseite. Es ist jedoch möglich, HTTPS-Video-Versand zu erzwingen, unabhängig vom verwendeten Protokoll, indem die Webseite mit dem Konfigurationsattribut [Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md) einbettet wird. (Beachten Sie, dass Video-Vorschauen im Autorenmodus immer sicher über HTTPS bereitgestellt werden.)

Je nach der Methode zum Veröffentlichen von Videos mit dynamischen Medien, die Sie in AEM verwenden, wird das `Video360Player.ssl` Konfigurationsattribut anders angewendet, wie im Folgenden gezeigt:

* Wenn Sie ein Video mit dynamischen Medien mit einer URL veröffentlichen, hängen Sie `Video360Player.ssl` an die URL an. Um beispielsweise einen sicheren Video-Versand zu erzwingen, hängen Sie `&Video360Player.ssl=on` am Ende des folgenden Viewer-URL-Beispiels an:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   See also [Linking URLs to your Web Application](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Wenn Sie ein Video für dynamische Medien mit Einbettungscode veröffentlichen, fügen Sie der Liste anderer Viewer-Konfigurationsparameter im Einbettungscode-Snippet hinzu. `Video360Player.ssl` Um beispielsweise HTTPS-Video-Versand zu erzwingen, hängen Sie `&Video360Player.ssl=on` wie im folgenden Beispiel an:

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

   See also [Embedding the Video on a Web Page](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)

