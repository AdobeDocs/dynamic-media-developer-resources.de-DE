---
description: Konfigurationsattribut für Video-Viewer für gemischte Medien.
solution: Experience Manager
title: VideoPlayer.mutevolume
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: 13398ac5-7137-4345-88b8-5e4df09edb7b
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---

# VideoPlayer.mutevolume{#videoplayer-mutevolume}

Konfigurationsattribut für Video-Viewer für gemischte Medien.

`[VideoPlayer.|<containerId>_videoPlayer.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Legt den stummschalteten Modus für die Videowiedergabe beim ersten Laden fest. Wenn auf <span class="codeph"> 1 </span> gesetzt, wird das Volumen stummgeschaltet. Andernfalls wird das Video mit Ton wiedergegeben. Auf bestimmten Geräten kann das Mutation der Videowiedergabe beim Laden auch die automatische Wiedergabe des Videos ermöglichen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`
