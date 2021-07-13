---
description: Der Videoplayer ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.
solution: Experience Manager
title: Videoplayer
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: 9cfeceff-f6bd-42d9-9b85-456bbaa278fd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---

# Videoplayer{#video-player}

Der Videoplayer ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn die Abmessungen des abgespielten Videos nicht mit den Abmessungen des Videoplayers übereinstimmen, wird der Videoinhalt innerhalb des Anzeigebereichs für das Rechteck des Videoplayers zentriert.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Videoplayers:

```
.s7interactivevideoviewer .s7videoplayer
```

**CSS-Eigenschaften des Videoplayers**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Hauptansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können die Fehlermeldung lokalisieren, die angezeigt wird, wenn das System das Video nicht wiedergeben kann.

Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Zum Einrichten eines Video-Viewers mit einer Videoplayergröße von 512 x 288 Pixel.

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

Geschlossene Untertitel werden in einen internen Container im Videoplayer eingefügt. Die Position dieses Containers wird durch unterstützte WebVTT-Positionierungsoperatoren gesteuert. Der Beschriftungstext selbst befindet sich in diesem Container und sein Stil wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**CSS-Eigenschaften von verdeckten Untertiteln**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Geschlossener Beschriftungstexthintergrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe für Beschriftung schließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftstärke  </span> </p> </td> 
   <td colname="col2"> <p> Schriftstärke der verdeckten Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße  </span> </p> </td> 
   <td colname="col2"> <p> Schriftgröße der verdeckten Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie  </span> </p> </td> 
   <td colname="col2"> <p>Geschlossene Beschriftungsschrift. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-5b82913ff3c44b7b8187969cb15e9560}

So richten Sie Beschriftungstext auf einem halbtransparenten schwarzen Hintergrund auf 14 Pixel, hellgrau, Arial ein:

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

Das Erscheinungsbild der Pufferanimation wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Animationssymbol am linken Rand, normalerweise minus der Hälfte der Breite des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Der obere Rand des Animationssymbols, normalerweise minus der Hälfte der Höhe des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Knob-Grafik. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten einer Pufferanimation, die 101 Pixel breit und 29 Pixel hoch ist:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
