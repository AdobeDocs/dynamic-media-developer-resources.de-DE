---
description: Konfigurationsattribut für Video-Viewer.
solution: Experience Manager
title: VideoPlayer.mutevolume
feature: Dynamic Media Classic,Viewer,SDK/API,Video
role: Developer,User
exl-id: 8f644a40-7fd9-4edd-be29-698635b46507
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---

# VideoPlayer.mutevolume{#videoplayer-mutevolume}

Konfigurationsattribut für Video-Viewer.

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
