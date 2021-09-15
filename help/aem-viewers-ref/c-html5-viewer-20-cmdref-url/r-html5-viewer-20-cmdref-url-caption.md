---
title: caption
description: Parameter, die allen Viewern gemeinsam sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 6%

---

# caption{#caption}

Parameter, die allen Viewern gemeinsam sind.

>[!NOTE]
>
>Dieser Befehl gilt nicht für den Video-Bild-Viewer.

` caption= *`Datei`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum WebVTT-Beschriftungsinhalt an. Image Serving stellt die WebVTT-Datei bereit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt den standardmäßigen Beschriftungsstatus an. Aktiviert ist <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dieser Viewer unterstützt die Untertitelung über gehostete WebVTT-Dateien. Mit diesem Parameter angegebene Untertitel gelten für das Video, das in Mediensets zuerst angezeigt wird. nachfolgende Videos werden ohne Untertitel wiedergegeben. Überschneidende Hinweise und Regionen werden nicht unterstützt. Unterstützte Cue-Point-Positionierungsoperatoren:

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
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>Testausrichtung </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end  </span> </p> </td> 
   <td colname="col4"> <p> Steuert die Ausrichtung des Textes. </p> <p>Der Standardwert ist <span class="codeph"> middle </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>Textposition </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Prozentsatz des Einsatzes in die VideoPlayer-Komponente für den Anfang des Beschriftungstextes. </p> <p>Der Standardwert ist <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>Zeilengröße </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Prozentsatz der für Untertitel verwendeten Videobreite. </p> <p>Der Standardwert ist <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>Zeilenposition </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Bestimmt die Zeilenposition auf der Seite. </p> <p>Wenn es als Ganzzahl ohne Prozentzeichen ausgedrückt wird, dann ist es die Anzahl der Zeilen oben, in denen der Text angezeigt wird. </p> <p>Wenn es als Prozentsatz ausgedrückt wird - das Prozentzeichen ist das letzte Zeichen -, wird der Beschriftungstext angezeigt, der den Anzeigebereich in Prozent nach unten zeigt. </p> <p>Der Standardwert ist <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Wenn die WebVTT-Datei andere WebVTT-Funktionen enthält, werden diese nicht unterstützt. Sie stören jedoch nicht die Untertitelung.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum WebVTT-Beschriftungsinhalt an. Die WebVTT-Datei wird von Image Serving bereitgestellt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt den standardmäßigen Beschriftungsstatus an. </p> <p>Aktiviert ist <span class="codeph"> 1 </span>. </p> </td> 
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
