---
title: Bildunterschrift
description: URL-Befehl für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 8eb2aa50-52b9-4b63-9789-87e492f34a22
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 3%

---

# Bildunterschrift{#caption}

URL-Befehl für den interaktiven Video-Viewer.

` caption= *`Datei`*[,0|1]`

Der Viewer unterstützt verdeckte Untertitel durch gehostete WebVTT-Dateien. Überlappende Hinweise und Bereiche werden nicht unterstützt. Zu den unterstützten Operatoren für die Cue-Positionierung gehören:

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
   <td colname="col1"> <p> </span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Textausrichtung </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> links|rechts|Mitte|Start|Ende </span> </p> </td> 
   <td colname="col4"> <p> Steuern der Textausrichtung. </p> <p>Der Standardwert ist <span class="codeph"> Middle </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>Textposition </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Prozentsatz der Einfügung in die VideoPlayer-Komponente für den Anfang des Untertiteltextes. </p> <p>Der Standardwert ist 0 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>Zeilengröße </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Prozentsatz der für Untertitel verwendeten Videobreite. </p> <p>Der Standardwert lautet 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>Zeilenposition </p> </td> 
   <td colname="col3"> <p> 0%-100%|Integer </p> </td> 
   <td colname="col4"> <p> Bestimmt die Zeilenposition auf der Seite. </p> <p>Wenn er als Ganzzahl ausgedrückt wird (kein Prozentzeichen), dann ist dies die Anzahl der Zeilen von oben, in denen der Text angezeigt wird. </p> <p>Wenn es sich um einen Prozentsatz handelt (das Prozentzeichen ist das letzte Zeichen), wird der Beschriftungstext in diesem Prozentsatz unterhalb des Anzeigebereichs angezeigt. </p> <p>Der Standardwert lautet 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>

Andere WebVTT-Funktionen in der WebVTT-Datei werden nicht unterstützt, sollten die Untertitelung jedoch nicht stören.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Datei </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum WebVTT-Untertitelinhalt an. Bereitstellen der WebVTT-Datei durch Image Serving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt den standardmäßigen Untertitelstatus an (aktiviert ist <span class="codeph"> 1 </span>). </p> </td> 
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
