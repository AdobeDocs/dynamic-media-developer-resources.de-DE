---
description: URL-Befehl für den interaktiven Video-Viewer.
solution: Experience Manager
title: Navigation
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 12%

---

# Navigation{#navigation}

URL-Befehl für den interaktiven Video-Viewer.

` navigation= *`Datei`*`

Der Viewer unterstützt die Videokapitelnavigation über gehostete WebVTT-Dateien. Cue-Positionierungsoperatoren werden nicht unterstützt.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zu WebVTT-Navigationsinhalten an. Image Serving sollte die WebVTT-Datei hosten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Keine.

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```
