---
title: videoPlayer.play
description: Konfigurationsattribut für den Viewer für gemischte Medien-Videos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
TQID: 'https://experienceleague.adobe.com/BWApI4QtEvmeQk1vNJDLtKIvrG3uO02oUlOVEGhyl2s'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 2%

---

# videoPlayer.play{#videoplayer-playback}

Konfigurationsattribut für den Viewer für gemischte Medien-Videos.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressiv</span> </p> </td> 
   <td colname="col2"> <p> Legt den Wiedergabetyp fest, der vom Viewer verwendet wird. Wenn <span class="codeph"> auto</span> festgelegt ist, verwendet der Viewer in den meisten Desktop-Browsern und auf allen iOS-Geräten HTML5-Streaming-Videos im HLS-Format. Es wird auf die progressive HTML5-Wiedergabe auf bestimmten Systemen wie dem älteren Internet Explorer und Android™ zurückgegriffen. </p> <p>Wenn <span class="codeph"> Progressive</span> angegeben ist, verlässt sich der Viewer nur auf die HTML5-Wiedergabe, wie sie nativ von Browsern unterstützt wird, und gibt Videos progressiv auf allen Systemen wieder. </p> <p>Weiterführende Informationen zur Wiedergabeauswahl im automatischen und progressiven Modus finden Sie im Benutzerhandbuch zum Viewer-SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
