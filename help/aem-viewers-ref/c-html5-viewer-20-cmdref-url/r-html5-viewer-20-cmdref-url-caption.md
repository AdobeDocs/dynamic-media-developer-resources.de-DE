---
title: Bildunterschrift
description: Für alle Viewer gemeinsamer Parameter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# Bildunterschrift{#caption}

Für alle Viewer gemeinsamer Parameter.

>[!NOTE]
>
>Dieser Befehl gilt nicht für den Videobild-Viewer.

` caption= *`Datei`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Datei </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum WebVTT-Untertitelinhalt an. Image Serving stellt die WebVTT-Datei bereit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt den standardmäßigen Untertitelstatus an. Aktiviert ist <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dieser Viewer unterstützt verdeckte Untertitel über gehostete WebVTT-Dateien. Mit diesem Parameter angegebene Untertitel gelten für das Video, das in Mediensets zuerst angezeigt wird. Nachfolgende Videos werden ohne Untertitel wiedergegeben. Überlappende Hinweise und Bereiche werden nicht unterstützt. Unterstützte Bediener für die Cue-Positionierung:

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Schlüssel </p> </th> 
   <th colname="col2" class="entry"> <p>Name </p> </th> 
   <th colname="col3" class="entry"> <p>Werte </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Testausrichtung </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> links|rechts|Mitte|Start|Ende </span> </p> </td> 
   <td colname="col4"> <p> Steuert die Ausrichtung von Text. </p> <p>Der Standardwert ist <span class="codeph"> Middle </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>Textposition </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Prozentsatz der Einfügung in die VideoPlayer-Komponente für den Anfang des Untertiteltextes. </p> <p>Der Standardwert ist <span class="codeph"> 0 % </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>Zeilengröße </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Prozentsatz der für Untertitel verwendeten Videobreite. </p> <p>Der Standardwert lautet <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>Zeilenposition </p> </td> 
   <td colname="col3"> <p> 0%-100%|Integer </p> </td> 
   <td colname="col4"> <p> Bestimmt die Zeilenposition auf der Seite. </p> <p>Wenn er als Ganzzahl ohne Prozentzeichen ausgedrückt wird, dann ist dies die Anzahl der Zeilen von oben, in denen der Text angezeigt wird. </p> <p>Wenn er als Prozentsatz ausgedrückt wird - das Prozentzeichen ist das letzte Zeichen -, wird der Beschriftungstext in diesem Prozentsatz nach unten im Anzeigebereich angezeigt. </p> <p>Der Standardwert lautet <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Wenn in der WebVTT-Datei andere WebVTT-Funktionen vorhanden sind, werden diese nicht unterstützt. Sie unterbrechen die Untertitelung jedoch nicht.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Datei </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum WebVTT-Untertitelinhalt an. Die WebVTT-Datei wird von Image Serving bereitgestellt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt den standardmäßigen Untertitelstatus an. </p> <p>Aktiviert ist <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Keine.

## Beispiel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
