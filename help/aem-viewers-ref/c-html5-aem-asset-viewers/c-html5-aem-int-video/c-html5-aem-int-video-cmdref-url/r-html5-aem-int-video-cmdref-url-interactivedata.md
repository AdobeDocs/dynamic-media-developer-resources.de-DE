---
title: InteractiveData
description: URL-Befehl für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
TQID: 'https://experienceleague.adobe.com/xIjjnZZX0Y7wce2TJwN2R228elxxysj0qXB2WELq9xc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 4%

---

# InteractiveData{#interactivedata}

URL-Befehl für den interaktiven Video-Viewer.

`interactivedata= *`Datei`*`

Interaktive Daten verknüpfen bestimmte Zeitbereiche im Videoinhalt mit den Produktdaten, die später in interaktiven Farb-/Bildmustern neben dem Video angezeigt werden. Es ist auch im call-to-action-Bedienfeld verknüpft, das nach Abschluss der Videowiedergabe angezeigt wird. Es enthält auch einen Titel für das interaktive Video, das im call-to-action-Bedienfeld angezeigt wird.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Datei</span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum interaktiven WebVTT-Dateninhalt an. Die WebVTT-Datei muss von Image Serving bereitgestellt werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Keine.

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
