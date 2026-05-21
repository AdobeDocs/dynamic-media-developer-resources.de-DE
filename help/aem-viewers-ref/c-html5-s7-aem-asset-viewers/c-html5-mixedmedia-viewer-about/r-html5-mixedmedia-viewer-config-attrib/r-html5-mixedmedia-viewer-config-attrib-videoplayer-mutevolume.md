---
title: VideoPlayer.muteVolume
description: Konfigurationsattribut für den Viewer für gemischte Medien-Videos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 13398ac5-7137-4345-88b8-5e4df09edb7b
TQID: 'https://experienceleague.adobe.com/F3BsS2qXezMhbmpx-NKFstl-eU2WoYN1XK6N6-3DsbM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 8%

---

# VideoPlayer.muteVolume{#videoplayer-mutevolume}

Konfigurationsattribut für den Viewer für gemischte Medien-Videos.

`[VideoPlayer.|<containerId>_videoPlayer.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Legt den Stummschaltungsmodus für die Videowiedergabe beim Laden fest. Wenn auf <span class="codeph"> 1 </span>, wird die Lautstärke stummgeschaltet, andernfalls wird das Video mit Ton wiedergegeben. Auf bestimmten Geräten ermöglicht die Stummschaltung der Videowiedergabe beim Laden auch die automatische Wiedergabe des Videos. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`
