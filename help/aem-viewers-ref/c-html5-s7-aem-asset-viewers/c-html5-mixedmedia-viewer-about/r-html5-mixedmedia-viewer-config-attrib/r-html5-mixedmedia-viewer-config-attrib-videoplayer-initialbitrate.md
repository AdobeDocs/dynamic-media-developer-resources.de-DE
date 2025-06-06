---
title: VideoPlayer.initialbitrate
description: VideoPlayer.initialbitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Wert </span> </span> </p> </td> 
   <td colname="col2"> <p>Legt die Video-Bitrate (in Kilobit pro Sekunde oder kbps) fest, die für die anfängliche Wiedergabe von Videos auf Desktops verwendet wird. </p> <p>Wenn dieser Bitratenwert nicht im adaptiven Videoset vorhanden ist, startet der Video-Player das Video mit der nächstniedrigsten Bitrate. </p> <p>Wenn auf <span class="codeph"> 0 </span> festgelegt, startet der Video-Player mit der niedrigstmöglichen Bitrate. Gilt nur für Systeme, die keine native Unterstützung für HTML5 HLS-Videos haben (d. h. Browser Firefox, Chrome und Internet Explorer 11 unter Windows 10), und wenn der Wiedergabemodus auf <span class="codeph"> automatische </span> eingestellt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
