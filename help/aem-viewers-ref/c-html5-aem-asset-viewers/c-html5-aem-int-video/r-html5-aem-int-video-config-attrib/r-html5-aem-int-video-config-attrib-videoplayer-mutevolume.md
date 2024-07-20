---
title: VideoPlayer.mutevolume
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 84deb0d4-ac7e-4ba0-884f-675a0dcc827b
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 5%

---

# VideoPlayer.mutevolume{#videoplayer-mutevolume}

Konfigurationsattribut für interaktiven Video-Viewer.

`[VideoPlayer.|<containerId>_videoPlayer.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Legt den stummschalteten Modus für die Videowiedergabe beim ersten Laden fest. Wenn der Wert auf <span class="codeph"> 1 </span> gesetzt ist, ist die Lautstärke stummgeschaltet; andernfalls wird das Video mit dem Ton wiedergegeben. Auf bestimmten Geräten ermöglicht die Mutation der Videowiedergabe beim Laden auch die automatische Wiedergabe des Videos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`
