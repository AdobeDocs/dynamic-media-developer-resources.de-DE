---
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
title: VideoPlayer.posterimage
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: 17c1220d-f2a4-4729-84e2-b9f6f5732423
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

Konfigurationsattribut für interaktiven Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das im ersten Frame angezeigt werden soll, bevor das Video wiedergegeben wird, aufgelöst gegen <span class="codeph"> serverurl</span>. Falls in der URL angegeben, kodieren Sie Folgendes über HTTP: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> als  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Wenn der Wert <span class="codeph"><span class="varname"> image_id</span></span> weggelassen wird, versucht die Komponente stattdessen, das standardmäßige Posterbild für dieses Asset zu verwenden. </p> <p>Wenn das Video als Pfad angegeben wird, wird die standardmäßige Katalogkennung für Posterbilder aus dem Videopfad abgeleitet, da das Paar <span class="codeph"> catalog_id/image_id</span> , wobei <span class="codeph"> catalog_id</span> dem ersten Token im Pfad und <span class="codeph"> image_id</span> dem Namen des Videos entspricht, dessen Erweiterung entfernt wurde. Wenn das Bild mit dieser ID nicht vorhanden ist, wird das Standbild nicht angezeigt. </p> <p>Um die Anzeige des standardmäßigen Posterbilds zu verhindern, geben Sie <span class="codeph"> none</span> als Posterbildwert an. Wenn nur die <span class="codeph"><span class="varname"> isCommands</span></span> angegeben sind, werden die Befehle auf das standardmäßige Posterbild angewendet, bevor das Bild angezeigt wird. </p> </td> 
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
