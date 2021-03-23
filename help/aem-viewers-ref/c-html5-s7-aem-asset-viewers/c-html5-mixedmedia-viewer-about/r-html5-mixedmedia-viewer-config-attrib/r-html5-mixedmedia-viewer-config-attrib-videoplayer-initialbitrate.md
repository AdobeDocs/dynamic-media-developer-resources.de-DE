---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
feature: Dynamic Media Classic,Viewer,SDK/API,Mix-Mediensets
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 4%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`Wert`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>Legt die Bitrate-in-Bit-Rate für Videos pro Sekunden oder Kbit/s fest, die für die anfängliche Wiedergabe von Videos auf Desktops verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Video-Set vorhanden ist, wird der Videoplayer mit der nächstniedrigsten Bitrate Beginn. </p> <p>Bei Festlegung auf <span class="codeph"> 0 </span> wird der Videoplayer mit der niedrigstmöglichen Bitrate Beginn. Gilt nur für Systeme, die keine native Unterstützung für HTML5-HLS-Videos haben (Firefox, Chrome und Internet Explorer 11 unter Windows 10), und wenn der Wiedergabemodus auf <span class="codeph"> auto </span> eingestellt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
