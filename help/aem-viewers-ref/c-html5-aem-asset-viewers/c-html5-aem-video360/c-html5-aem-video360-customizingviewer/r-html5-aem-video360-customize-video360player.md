---
description: Der Videoplayer ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.
seo-description: Der Videoplayer ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.
seo-title: Video360-Player
solution: Experience Manager
title: Video360-Player
topic: Dynamic media
uuid: e78a9c22-4217-42cc-ba47-3acb4130a4fd
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---


# Video360 player{#video-player}

Der Videoplayer ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn die Abmessungen des abgespielten Videos nicht mit den Abmessungen des Videoplayers übereinstimmen, wird der Videoinhalt innerhalb des Rechteckanzeigebereichs des Videoplayers zentriert.

Die folgende CSS-Klassenauswahl steuert das Erscheinungsbild des Videoplayers:

```
.s7video360viewer .s7video360player
```

**CSS-Eigenschaften des Videoplayers**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Haupt-Ansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können die Fehlermeldung lokalisieren, die angezeigt wird, wenn das System das Video nicht abspielen kann.

Siehe [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Beispiel: Zum Einrichten eines Video-Viewers mit einer Videoplayer-Größe von 512 x 288 Pixel.

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

Das Erscheinungsbild der Pufferanimation wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7video360viewer .s7video360player .s7waiticon
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
   <td colname="col2"> <p> Animationssymbol links, normalerweise minus die Hälfte der Breite des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Animationssymbole am oberen Rand, normalerweise minus der Hälfte der Höhe des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Knob-Grafik. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Pufferung auf 101 Pixel breit und 29 Pixel hoch ein:

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

