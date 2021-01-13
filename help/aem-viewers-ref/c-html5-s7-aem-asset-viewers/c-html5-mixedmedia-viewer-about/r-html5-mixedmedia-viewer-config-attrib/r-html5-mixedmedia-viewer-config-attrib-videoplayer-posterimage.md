---
description: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic media
uuid: 28663f44-11cb-4522-bd12-d6bec17b4173
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 3%

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
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

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Keine.

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
