---
title: caption
description: URL-Befehl für interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 8eb2aa50-52b9-4b63-9789-87e492f34a22
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 3%

---

# caption{#caption}

URL-Befehl für interaktiven Video-Viewer.

` caption= *`file`*[,0|1]`

Der Viewer unterstützt die Untertitelung über gehostete WebVTT-Dateien. Überschneidende Hinweise und Regionen werden nicht unterstützt. Zu den unterstützten Cue-Point-Positionierungs-Operatoren zählen:

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Schlüssel </p> </th> 
   <th colname="col2" class="entry"> <p>Name </p> </th> 
   <th colname="col3" class="entry"> <p>Wert </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>Textausrichtung </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end </span> </p> </td> 
   <td colname="col4"> <p> Textausrichtung steuern </p> <p>Der Standardwert ist <span class="codeph"> middle </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>Textposition </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Prozentsatz des Einsatzes in die VideoPlayer-Komponente für den Anfang des Beschriftungstextes. </p> <p>Der Standardwert ist 0 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>Zeilengröße </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Prozentsatz der für Untertitel verwendeten Videobreite. </p> <p>Der Standardwert ist 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>Zeilenposition </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Bestimmt die Zeilenposition auf der Seite. </p> <p>Wenn der Text als Ganzzahl (kein Prozentzeichen) ausgedrückt wird, ist dies die Anzahl der Zeilen von oben, in denen der Text angezeigt wird. </p> <p>Wenn es sich um einen Prozentsatz handelt (Prozentzeichen ist das letzte Zeichen), wird der Beschriftungstext angezeigt, der den Anzeigebereich um einen Prozentwert nach unten zeigt. </p> <p>Der Standardwert ist 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>

Andere WebVTT-Funktionen, die in der WebVTT-Datei vorhanden sind, werden nicht unterstützt, sollten aber die Untertitelung nicht stören.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum WebVTT-Beschriftungsinhalt an. Stellen Sie die WebVTT-Datei über Image Serving bereit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt den standardmäßigen Beschriftungsstatus an (aktiviert ist <span class="codeph"> 1 </span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Keine.

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.caption.vtt,1
```
