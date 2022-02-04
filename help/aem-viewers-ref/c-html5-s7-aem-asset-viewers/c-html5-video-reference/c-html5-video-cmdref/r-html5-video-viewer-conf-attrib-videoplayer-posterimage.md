---
title: VideoPlayer.posterimage
description: Konfigurationsattribut für Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

Konfigurationsattribut für Video-Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das vor der Videowiedergabe im ersten Frame angezeigt werden soll und mit dem <span class="codeph"> serverurl</span>. Falls in der URL angegeben, kodieren Sie Folgendes über HTTP: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Wenn die Variable <span class="codeph"><span class="varname"> image_id</span></span> weggelassen wird, versucht die Komponente stattdessen, das standardmäßige Posterbild für dieses Asset zu verwenden. </p> <p>When the video is specified as a path, the default poster images catalog ID is derived from the video path as the <span class="codeph"> catalog_id/image_id</span> pair where <span class="codeph"> catalog_id</span> corresponds to the first token in the path. Und <span class="codeph"> image_id</span> ist der Name des Videos, wobei die Erweiterung entfernt wird. If the image with that ID does not exist, the poster image is not shown. </p> <p>Um die Anzeige des standardmäßigen Posterbilds zu verhindern, geben Sie <span class="codeph"> Keine</span> als Poster-Bildwert. Wenn nur die <span class="codeph"><span class="varname"> isCommands</span></span> festgelegt sind, werden die Befehle auf das standardmäßige Posterbild angewendet, bevor das Bild angezeigt wird. </p> </td> 
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
