---
description: Konfigurationsattribut für Video-Viewer für gemischte Medien.
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5fd3aa39-edb0-4434-aa5f-e511c84cf950
source-git-commit: c58199c5884c368e92e50fe0ef9d6ad523e36266
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Konfigurationsattribut für Video-Viewer für gemischte Medien.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Steuert, ob das Video über eine sichere SSL-Verbindung (HTTPS) oder eine unsichere Verbindung (HTTP) bereitgestellt wird. </p> <p>Wenn auf <span class="codeph"> auto</span> festgelegt, wird das Videobereitstellungsprotokoll vom Protokoll der eingebetteten Webseite übernommen. Wenn die Webseite über HTTPS geladen wird, wird das Video auch über HTTPS bereitgestellt und umgekehrt. Wenn sich die Webseite auf HTTP befindet, wird das Video über HTTP bereitgestellt. </p> <p>Wenn auf <span class="codeph"> unter</span> gesetzt, erfolgt die Videobereitstellung immer über eine sichere Verbindung, unabhängig vom Webseitenprotokoll. </p> <p>Betrifft nur die veröffentlichte Videobereitstellung und wird bei der Videovorschau im Autorenmodus ignoriert. </p> </td> 
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

Siehe auch [Sichere Videobereitstellung](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb).
