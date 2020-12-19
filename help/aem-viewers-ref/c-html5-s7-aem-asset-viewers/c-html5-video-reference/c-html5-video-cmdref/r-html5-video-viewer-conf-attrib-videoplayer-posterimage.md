---
description: Konfigurationsattribut für Video Viewer.
seo-description: Konfigurationsattribut für Video Viewer.
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic media
uuid: 59d81a72-ac17-4c32-ab47-89bd14dc17a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

Konfigurationsattribut für Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das vor dem Abspielen des Beginns im ersten Bild angezeigt werden soll, wurde gegen <span class="codeph"> serl</span> aufgelöst. Wenn in der URL angegeben, können Sie Folgendes HTTP-kodieren: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> als  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Wenn der Wert <span class="codeph"><span class="varname"> image_id</span></span> weggelassen wird, versucht die Komponente stattdessen, das Standbild für dieses Asset zu verwenden. </p> <p>Wenn das Video als Pfad angegeben wird, wird die Standard-Katalogkennung für Standbilder vom Videopfad abgeleitet, da das Paar <span class="codeph"> catalog_id/image_id</span> <span class="codeph"> catalog_id</span> dem ersten Token im Pfad und <span class="codeph"> image_id</span> dem Namen des Videos entspricht, dessen Erweiterung entfernt wurde. Wenn das Bild mit dieser ID nicht vorhanden ist, wird das Standbild nicht angezeigt. </p> <p>Um die Anzeige des Standbilds zu verhindern, geben Sie <span class="codeph"> none</span> als Standbildwert an. Wenn nur <span class="codeph"><span class="varname"> isCommands</span></span> angegeben sind, werden die Befehle auf das Standbild angewendet, bevor das Bild angezeigt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Keine.

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```

