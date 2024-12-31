---
title: Video-Player
description: Der Smart-Crop-Video-Player ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Video-Player{#video-player}

Der Smart-Crop-Video-Player ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn die Abmessungen des wiedergegebenen Videos nicht mit den Abmessungen des Smart-Crop-Video-Players übereinstimmen, wird der Videoinhalt im rechteckigen Anzeigebereich des Smart-Crop-Video-Players zentriert.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Smart-Crop-Video-Players:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**CSS-Eigenschaften des Smart-Crop-Video-Players**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Hauptansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Fehlermeldung, die angezeigt wird, wenn das System das Video nicht abspielen kann, kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: So richten Sie einen Video-Viewer für smartes Zuschneiden mit einer Größe des Video-Players für smartes Zuschneiden von 512 x 288 Pixel ein.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

Geschlossene Untertitel werden in einen internen Container im Video-Player für smartes Zuschneiden eingefügt. Die Position dieses Containers wird durch unterstützte WebVTT-Positionierungsoperatoren gesteuert. Der Beschriftungstext selbst befindet sich in diesem Container und sein Stil wird mit dem folgenden CSS-Klassenselektor gesteuert:

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**CSS-Eigenschaften von Untertiteln**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Text für Untertitel - Hintergrund </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe der Beschriftung schließen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Schriftstärke für Untertitel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Schriftgröße für Untertitel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftart für Untertitel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So legen Sie für Text für Untertitel einen Wert von 14 Pixeln (hellgrau, Arial®) auf einem halbtransparenten schwarzen Hintergrund fest:

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

**CSS-Eigenschaften des Wartesymbols**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Breite des Animationssymbols </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p> Höhe des Animationssymbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rand links </span> </p> </td> 
   <td colname="col2"> <p> Animationssymbol Linker Rand, normalerweise minus der Hälfte der Breite des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Oberer Rand des Animationssymbols, normalerweise abzüglich der Hälfte der Höhe des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Knopf-Bildmaterial. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Eine Puffer-Animation soll 101 Pixel breit und 29 Pixel hoch sein:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
