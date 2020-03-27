---
description: Parameter, die allen Viewern gemein sind.
seo-description: Parameter, die allen Viewern gemein sind.
seo-title: caption
solution: Experience Manager
title: caption
topic: Dynamic media
uuid: e5a715c4-9b5b-48fc-8228-5e7416e2b71a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# caption{#caption}

Parameter, die allen Viewern gemein sind.

>[!NOTE]
>
>Dieser Befehl gilt nicht für den Video-Bild-Viewer.

` caption= *`Datei`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> -Datei </span></span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum WebVTT-Beschriftungsinhalt an. Image Serving stellt die WebVTT-Datei bereit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Standard-Beschriftungsstatus an. Aktiviert ist <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dieser Viewer unterstützt Untertitel über gehostete WebVTT-Dateien. Die mit diesem Parameter angegebenen Beschriftungen gelten für das Video, das in Mediensets zuerst angezeigt wird. nachfolgende Videos werden ohne Bildunterschriften abgespielt. Überschneidende Hinweise und Regionen werden nicht unterstützt. Unterstützte Cue-Positionierungsoperatoren:

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
   <td colname="col2"> <p>test align </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|Beginn|end </span> </p> </td> 
   <td colname="col4"> <p> Steuert die Ausrichtung des Textes. </p> <p>Der Standardwert ist <span class="codeph"> Mitte </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>Textposition </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Prozentsatz des Einschnitts in die VideoPlayer-Komponente am Anfang des Beschriftungstexts. </p> <p>Default is <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>Liniengröße </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Prozentsatz der für Bildunterschriften verwendeten Videobreite. </p> <p>Default is <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>Zeilenposition </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Bestimmt die Zeilenposition auf der Seite. </p> <p>Wenn der Text als Ganzzahl ohne Prozentzeichen ausgedrückt wird, ist dies die Anzahl der Zeilen von oben, in denen der Text angezeigt wird. </p> <p>Wenn es als Prozentwert ausgedrückt wird, ist das Prozentzeichen das letzte Zeichen, dann wird der Beschriftungstext in Prozent unter dem Anzeigebereich angezeigt. </p> <p>Default is <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beachten Sie, dass WebVTT-Funktionen, die in der WebVTT-Datei vorhanden sind, nicht unterstützt werden. Sie werden jedoch die Untertitel nicht stören.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> -Datei </span></span> </p> </td> 
   <td colname="col2"> <p> Gibt eine URL oder einen Pfad zum WebVTT-Untertitelinhalt an. Die WebVTT-Datei wird von Image Serving bereitgestellt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Standard-Beschriftungsstatus an. </p> <p>Aktiviert ist <span class="codeph"> 1 </span>. </p> </td> 
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

