---
description: Konfigurationsattribut für Video-Viewer für gemischte Medien.
seo-description: Konfigurationsattribut für Video-Viewer für gemischte Medien.
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: 07e2c55b-2388-44c8-83ab-338997c5cb71
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# VideoPlayer.ssl{#videoplayer-ssl}

Konfigurationsattribut für Video-Viewer für gemischte Medien.

>[!NOTE]
>
>Dieses Konfigurationsattribut gilt nur für AEM 6.2 mit der Installation von [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) und für AEM 6.1 mit der Installation von [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Steuert, ob das Video über eine sichere SSL-Verbindung (HTTPS) oder über eine unsichere Verbindung (HTTP) bereitgestellt wird. </p> <p>Bei Festlegung auf <span class="codeph"> auto</span> wird das Video-Versand-Protokoll vom Protokoll der Einbettungswebseite übernommen. Wenn die Webseite über HTTPS geladen wird, wird das Video auch über HTTPS bereitgestellt und umgekehrt. Befindet sich die Webseite auf HTTP, wird das Video über HTTP bereitgestellt. </p> <p>Bei Festlegung auf " <span class="codeph"> on</span>"erfolgt der Video-Versand immer über eine sichere Verbindung, unabhängig vom Webseitenprotokoll. </p> <p>Betrifft nur veröffentlichte Video-Versand und wird bei der Vorschau von Videos im Autorenmodus ignoriert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

Siehe auch [Secure Video Versand](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb).
