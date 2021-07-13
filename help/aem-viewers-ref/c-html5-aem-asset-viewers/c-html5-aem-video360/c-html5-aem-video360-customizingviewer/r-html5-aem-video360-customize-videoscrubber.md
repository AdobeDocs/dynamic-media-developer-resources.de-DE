---
description: Der Video-Scrubber ist das horizontale Regler-Steuerelement, mit dem ein Benutzer dynamisch an eine beliebige Zeitposition innerhalb des derzeit wiedergegebenen Videos suchen kann.
solution: Experience Manager
title: Videobauber
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a0b89b4b-5f66-41d5-88b9-a01fddec437e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 3%

---

# Videobauber{#video-scrubber}

Der Video-Scrubber ist das horizontale Regler-Steuerelement, mit dem ein Benutzer dynamisch an eine beliebige Zeitposition innerhalb des derzeit wiedergegebenen Videos suchen kann.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Der Scrubber-Knopf bewegt sich auch, während das Video abgespielt wird, um die aktuelle Zeitposition des Videos während der Wiedergabe anzugeben. Der Video-Scrubber nimmt immer die gesamte Breite der Steuerleiste ein. Es ist möglich, den Video-Scrubber zu entlüften. ihre Höhe und vertikale Position durch CSS ändern.

Das allgemeine Erscheinungsbild des Video-Scrubbers wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7video360viewer .s7videoscrubber 
.s7video360viewer .s7videoscrubber .s7videotime 
.s7video360viewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Video-Scrubbers**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Position vom unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Video-Scrubbers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Farbe des Video-Scrubbers. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die folgenden CSS-Klassenselektoren verfolgen Hintergrund-, Wiedergabe- und Lastindikatoren:

```
.s7video360viewer .s7videoscrubber .s7track 
.s7video360viewer .s7videoscrubber .s7trackloaded 
.s7video360viewer .s7videoscrubber .s7trackplayed
```

**CSS-Eigenschaften des Tracks**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höhe der entsprechenden Strecke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Farbe der entsprechenden Strecke. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der folgende CSS-Klassenselektor steuert den Knoten:

```
.s7video360viewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Knotens**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Drehversatz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Knopfes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Knotens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Knob-Grafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der folgende CSS-Klassenselektor steuert die Wiedergabedauer:

```
.s7video360viewer .s7videoscrubber .s7videotime
```

**CSS-Eigenschaften der wiedergegebenen Blase**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie  </span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfamilie, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße  </span> </p> </td> 
   <td colname="col2"> <p> Die Schriftgröße, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfarbe für die Zeitanzeige. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Blasenbereichbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Blasenbereichshöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Blasenflächen-Umrandung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Blasengrafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>Ausrichtung des Texts am Blasenbereich </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo für Video-Scrubber kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Beispiel** : Zum Einrichten eines Video-Viewers mit einem Video-Scrubber mit benutzerdefinierten Spurfarben mit einer Größe von 10 Pixel und einer Positionierung von 10 Pixel und 35 Pixel von der oberen und linken Kante der Steuerleiste.

```
.s7video360viewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7video360viewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7video360viewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7video360viewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
