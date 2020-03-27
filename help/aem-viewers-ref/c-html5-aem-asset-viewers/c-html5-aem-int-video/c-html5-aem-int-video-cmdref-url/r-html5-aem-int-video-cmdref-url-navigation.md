---
description: URL-Befehl für den interaktiven Video-Viewer.
seo-description: URL-Befehl für den interaktiven Video-Viewer.
seo-title: Navigation
solution: Experience Manager
title: Navigation
topic: Dynamic media
uuid: eecc7458-153c-4f36-b29e-97451f275c0c
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# Navigation{#navigation}

URL-Befehl für den interaktiven Video-Viewer.

` navigation= *`Datei`*`

Der Viewer unterstützt die Videokapitelnavigation über gehostete WebVTT-Dateien. Cue-Positionierungsoperatoren werden nicht unterstützt.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Datei</span></span> </p> </td> 
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

