---
title: SmartCropVideoPlayer.singleclick
description: Konfigurationsattribut für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

Konfigurationsattribut für Smart Crop Video Viewer.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einzelklicks/Tippen zum Umschalten von Wiedergabe/Pause. Einstellung auf <span class="codeph"> Keine</span> Deaktiviert Einzelklicks/Tippen zum Abspielen/Anhalten. Wenn auf <span class="codeph"> playPause</span>, wenn Sie auf das Video klicken, wechseln Sie zwischen dem Abspielen und Anhalten des Videos. Auf einigen Geräten können Sie native Steuerelemente verwenden. In diesem Fall <span class="codeph"> singleclick</span> Verhalten deaktiviert ist. </p> </td> 
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
