---
description: Der Videoplayer für smartes Zuschneiden ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.
solution: Experience Manager
title: Videoplayer
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2741821f-78fe-44d4-8604-fee10086e0a0
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 1%

---

# Videoplayer{#video-player}

Der Videoplayer für smartes Zuschneiden ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn die Abmessungen des wiedergegebenen Videos nicht mit den Abmessungen des Smart-Zuschnitt-Videoplayers übereinstimmen, wird der Videoinhalt innerhalb des Anzeigebereichs für das Rechteck des Smart-Zuschnitt-Videoplayers zentriert.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Smart-Zuschnitt-Videoplayers:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**CSS-Eigenschaften des Smart-Zuschnitt-Videoplayers**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Hauptansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Fehlermeldung, die angezeigt wird, wenn das System das Video nicht wiedergeben kann, kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Um einen Video-Viewer für smartes Zuschneiden einzurichten, bei dem die Größe des Smart-Zuschnitt-Videoplayers auf 512 x 288 Pixel festgelegt ist.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

Geschlossene Untertitel werden in einen internen Container im Smart-Zuschnitt-Videoplayer eingefügt. Die Position dieses Containers wird durch unterstützte WebVTT-Positionierungsoperatoren gesteuert. Der Beschriftungstext selbst befindet sich in diesem Container und sein Stil wird mit der folgenden CSS-Klassenauswahl gesteuert:

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**CSS-Eigenschaften von verdeckten Untertiteln**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Geschlossener Beschriftungstexthintergrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe für Beschriftung schließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftstärke </span> </p> </td> 
   <td colname="col2"> <p> Schriftstärke der verdeckten Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
   <td colname="col2"> <p> Schriftgröße der verdeckten Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Geschlossene Beschriftungsschrift. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um den Text für die geschlossene Beschriftung auf einen halb transparenten schwarzen Hintergrund mit 14 Pixel, hellgrau, Arial einzurichten:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

Das Erscheinungsbild der Pufferanimation wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
```

**CSS-Eigenschaften des Wartezeichens**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breite des Animationssymbols </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Höhe des Animationssymbols </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> Animationssymbol am linken Rand, normalerweise minus der Hälfte der Breite des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Der obere Rand des Animationssymbols, normalerweise minus der Hälfte der Höhe des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Knob-Grafik. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten einer Pufferanimation, die 101 Pixel breit und 29 Pixel hoch ist:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
