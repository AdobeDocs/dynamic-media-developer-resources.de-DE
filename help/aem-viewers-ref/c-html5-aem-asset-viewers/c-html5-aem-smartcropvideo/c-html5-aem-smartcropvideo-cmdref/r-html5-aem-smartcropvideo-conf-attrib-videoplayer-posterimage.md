---
title: SmartCropVideoPlayer.posterimage
description: Konfigurationsattribut für den Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ff4f8e2c-b9c3-4fba-b3f0-fa1eaddcd8c0
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

Konfigurationsattribut für den Smart Crop Video Viewer.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> keine|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das im ersten Frame angezeigt werden soll, bevor die Wiedergabe des Videos beginnt, wird gegen <span class="codeph"> ServerUrl aufgelöst</span>. Wenn in der URL angegeben, kodieren Sie Folgendes HTTP: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> als <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> als <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> wie <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Wenn der Wert <span class="codeph"><span class="varname"> image_id</span></span> weggelassen wird, versucht die Komponente, stattdessen das standardmäßige Posterbild für dieses Asset zu verwenden. </p> <p>Wenn das Video als Pfad angegeben ist, wird die standardmäßige Katalog-ID der Poster-Bilder aus dem Videopfad als <span class="codeph"> Paar catalog_id/image_id</span> abgeleitet. Die <span class="codeph"> catalog_id</span> entspricht dem ersten Token im Pfad und <span class="codeph"> image_id</span> ist der Name des Videos, aus dem die Erweiterung entfernt wurde. Wenn das Bild mit dieser ID nicht vorhanden ist, wird das Standbild nicht angezeigt. </p> <p>Um die Anzeige des standardmäßigen Posterbildes zu verhindern, geben Sie <span class="codeph"> Wert none</span> als Wert für das Posterbild an. Wenn nur die <span class="codeph"><span class="varname"> isCommands</span></span> angegeben sind, werden die Befehle auf das standardmäßige Posterbild angewendet, bevor das Bild angezeigt wird. </p> </td> 
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
