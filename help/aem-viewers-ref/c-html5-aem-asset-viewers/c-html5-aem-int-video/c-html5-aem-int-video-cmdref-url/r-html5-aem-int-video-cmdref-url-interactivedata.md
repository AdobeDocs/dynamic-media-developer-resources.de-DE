---
description: URL-Befehl für den interaktiven Video-Viewer.
seo-description: URL-Befehl für den interaktiven Video-Viewer.
seo-title: interactivedata
solution: Experience Manager
title: interactivedata
uuid: 72360679-7a39-46dd-ab10-7228d9c42a98
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---


# interactivedata{#interactivedata}

URL-Befehl für den interaktiven Video-Viewer.

`interactivedata= *`Datei`*`

Interaktive Daten ordnen bestimmte Zeitbereiche im Videoinhalt den Produktdaten zu, die später in interaktiven Farbfeldern neben dem Video angezeigt werden. Er ist auch im Aktionsaufruf-Bedienfeld enthalten, das beim Abschluss der Videowiedergabe angezeigt wird. Es enthält auch einen Titel für das interaktive Video, das im Aktionsaufruf-Bedienfeld angezeigt wird.

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

