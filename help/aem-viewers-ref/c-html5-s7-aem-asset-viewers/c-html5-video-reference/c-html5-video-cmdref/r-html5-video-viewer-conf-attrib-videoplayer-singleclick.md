---
description: Konfigurationsattribut für Video Viewer.
seo-description: Konfigurationsattribut für Video Viewer.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic media
uuid: df669b2e-31da-4de0-b480-e54402c9545c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Konfigurationsattribut für Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span></span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert die Zuordnung von Einfaches Klicken/Tippen zum Umschalten zwischen Wiedergabe/Pause. Wenn Sie auf " <span class="codeph"> Ohne</span> "einstellen, wird das einmalige Klicken/Tippen zum Abspielen/Anhalten deaktiviert. Wenn "playPause"festgelegt ist, wird durch Klicken auf das Video zwischen dem Abspielen und Anhalten des Videos umgeschaltet <span class="codeph"></span>. Auf einigen Geräten können Sie native Steuerelemente verwenden. In einem solchen Fall ist das <span class="codeph"> Verhalten von</span> "singleclick"deaktiviert. </p> </td> 
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

