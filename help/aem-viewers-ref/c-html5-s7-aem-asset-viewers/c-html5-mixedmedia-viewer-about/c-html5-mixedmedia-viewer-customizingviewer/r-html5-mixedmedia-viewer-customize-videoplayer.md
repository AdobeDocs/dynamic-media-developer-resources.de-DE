---
title: Videoplayer
description: Der Videoplayer ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2f92d76e-3104-4ad8-9426-662275492251
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Videoplayer{#video-player}

Der Videoplayer ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn die Abmessungen des abgespielten Videos nicht mit den Abmessungen des Videoplayers übereinstimmen, wird der Videoinhalt innerhalb des Anzeigebereichs für das Rechteck des Videoplayers zentriert.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Videoplayers:

```
.s7mixedmediaviewer .s7videoplayer
```

**CSS-Eigenschaften des Videoplayers**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Die Hintergrundfarbe des Videoplayers. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Fehlermeldung, die angezeigt wird, wenn das System das Video nicht wiedergeben kann, kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) .

Beispiel - So machen Sie den Videoplayer transparent:

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

Untertitel werden im Video-Player in einen internen Container eingefügt. Die Position dieses Containers wird durch unterstützte WebVTT-Positionierungsoperatoren gesteuert. Der Beschriftungstext selbst befindet sich in diesem Container. Der Stil wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**CSS-Eigenschaften von Beschriftungen**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Beschriftungstexthintergrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Beschriftungstextfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So legen Sie fest, dass Beschriftungstext auf einem halbtransparenten schwarzen Hintergrund 14 Pixel hellgraues Arial® sein soll:

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

Das Erscheinungsbild der Pufferanimation wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
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

Beispiel: Um eine Pufferanimation auf 101 Pixel breit und 29 Pixel hoch einzurichten:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
