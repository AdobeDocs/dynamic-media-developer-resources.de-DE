---
title: VideoPlayer.ssl
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16e17e2f-be98-4a5a-ba5e-5d18e7f76fa4
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Konfigurationsattribut für den interaktiven Video-Viewer.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Steuert, ob das Video über eine sichere SSL-Verbindung (HTTPS) oder eine unsichere Verbindung (HTTP) wiedergegeben wird. </p> <p>Bei Festlegung auf <span class="codeph"> automatisch </span> das Videobereitstellungsprotokoll vom Protokoll der einbettenden Web-Seite übernommen. Wenn die Web-Seite über HTTPS geladen wird, wird das Video auch über HTTPS wiedergegeben, und umgekehrt. Wenn die Web-Seite über HTTP aufgerufen wird, wird das Video über HTTP wiedergegeben. </p> <p>Bei Einstellung von <span class="codeph"> auf </span> erfolgt die Videowiedergabe immer über eine sichere Verbindung, unabhängig vom Webseitenprotokoll. </p> <p>Wirkt sich nur auf die Bereitstellung veröffentlichter Videos aus und wird für die Videovorschau im Autorenmodus ignoriert. </p> </td> 
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

Siehe auch [Sichere Videowiedergabe](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27).
