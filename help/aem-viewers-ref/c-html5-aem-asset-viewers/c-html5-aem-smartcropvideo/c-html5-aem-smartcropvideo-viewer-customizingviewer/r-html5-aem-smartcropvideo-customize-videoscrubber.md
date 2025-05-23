---
title: Video-Scrubber
description: Der Video-Scrubber ist der horizontale Schieberegler, mit dem Benutzende dynamisch nach einer beliebigen Position innerhalb des aktuell wiedergegebenen Videos suchen können.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 9f7e3fec-8303-4114-86b2-fb75d041701d
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Video-Scrubber{#video-scrubber}

Der Video-Scrubber ist der horizontale Schieberegler, mit dem Benutzende dynamisch nach einer beliebigen Position innerhalb des aktuell wiedergegebenen Videos suchen können.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Der Scrubber-Regler bewegt sich während der Videowiedergabe auch, um die aktuelle Zeitposition des Videos während der Wiedergabe anzuzeigen. Der Video-Scrubber nimmt immer die gesamte Breite der Steuerleiste ein. Es ist möglich, den Video-Scrubber mit Haut zu versehen und seine Höhe und vertikale Position mithilfe von CSS zu ändern.

Das allgemeine Erscheinungsbild des Video-Scrubbers wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7videoscrubber 
.s7smartcropvideoviewer .s7videoscrubber .s7videotime 
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Video-Scrubbers**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p> Position ab dem unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Video-Scrubbers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Farbe des Video-Scrubbers. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die folgenden CSS-Klassenselektoren verfolgen Hintergrund-, Wiedergabe- und Lastindikatoren:

```
.s7smartcropvideoviewer .s7videoscrubber .s7track 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed
```

**CSS-Eigenschaften der Spur**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des entsprechenden Gleises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Farbe der entsprechenden Spur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der folgende CSS-Klassenselektor steuert den Regler:

```
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Reglers**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Knopfversatz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Knopfes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Drehknopfs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Knopf-Bildmaterial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der folgende CSS-Klassenselektor steuert die wiedergegebene Zeitblase:

```
.s7smartcropvideoviewer .s7videoscrubber .s7videotime
```

**CSS-Eigenschaften der wiedergegebenen Zeitblase**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfamilie, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Schriftgröße, die für den Text der Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfarbe, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Blasenbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Blasenbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Auffüllung des Blasenbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Bubble-Grafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> zur Textausrichtung <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Ausrichtung des Textes am Blasenbereich. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo des Video-Scrubbers kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

**Beispiel** - Zum Einrichten eines Video-Viewers mit einem Video-Scrubber mit benutzerdefinierten Spurfarben, der zehn Pixel hoch ist. Und schließlich muss er 10 Pixel und 35 Pixel von den oberen und linken Rändern der Steuerleiste positioniert werden.

```
.s7smartcropvideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
