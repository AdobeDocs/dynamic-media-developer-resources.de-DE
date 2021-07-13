---
description: URL-Befehl für interaktiven Video-Viewer.
solution: Experience Manager
title: interactivedata
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 5%

---

# interactivedata{#interactivedata}

URL-Befehl für interaktiven Video-Viewer.

`interactivedata= *`Datei`*`

Interaktive Daten ordnen bestimmte Zeitbereiche im Videoinhalt den Produktdaten zu, die später in interaktiven Farbfeldern neben dem Video angezeigt werden. Sie ist auch im Aktionsaufruf-Bedienfeld enthalten, das am Ende der Videowiedergabe angezeigt wird. Außerdem wird ein Titel für das interaktive Video bereitgestellt, das im Aktionsaufruf-Bedienfeld angezeigt wird.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
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
