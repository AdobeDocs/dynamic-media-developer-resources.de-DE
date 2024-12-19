---
title: Video360Player.singleclick
description: Konfigurationsattribut für Video360-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# Video360Player.singleclick{#video-player-singleclick}

Konfigurationsattribut für Video360-Viewer.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick/Tippen zum Umschalten der Wiedergabe/Pause. Wenn Sie Keine <span class="codeph">, wird </span> Ein-Klick/Tippen zur Wiedergabe/Pause deaktiviert. Wenn <span class="codeph"> PlayPause</span> festgelegt ist, wird bei Auswahl des Videos zwischen Wiedergabe und Pause des Videos umgeschaltet. Auf einigen Geräten können Sie native Steuerelemente verwenden. In diesem Fall ist ein <span class="codeph"> Einzelklick</span>Verhalten deaktiviert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`playPause`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```
