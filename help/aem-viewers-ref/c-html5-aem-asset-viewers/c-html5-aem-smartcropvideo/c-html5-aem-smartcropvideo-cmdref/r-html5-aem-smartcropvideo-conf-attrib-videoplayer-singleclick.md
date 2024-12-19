---
title: SmartCropVideoPlayer.singleclick
description: Konfigurationsattribut für den Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f48f0866-4eb7-46c5-a7f5-457df7a568e7
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

Konfigurationsattribut für den Smart Crop Video Viewer.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklick/Tippen zum Umschalten der Wiedergabe/Pause. Wenn Sie Keine <span class="codeph">, wird </span> Ein-Klick/Tippen zur Wiedergabe/Pause deaktiviert. Wenn <span class="codeph"> PlayPause eingestellt ist</span> wird beim Klicken auf das Video zwischen der Wiedergabe und dem Anhalten des Videos umgeschaltet. Auf einigen Geräten können Sie native Steuerelemente verwenden. In diesem Fall ist <span class="codeph"> SingleClick</span>-Verhalten deaktiviert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
