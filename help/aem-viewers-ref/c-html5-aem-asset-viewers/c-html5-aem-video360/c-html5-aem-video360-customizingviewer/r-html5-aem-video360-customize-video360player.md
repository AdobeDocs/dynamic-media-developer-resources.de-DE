---
title: Video360-Player
description: Der Video-Player ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 54ccf872-2d24-4d3f-9808-6d0e2558f5a5
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Video360-Player{#video-player}

Der Video-Player ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn die Abmessungen des wiedergegebenen Videos nicht den Abmessungen des Video-Players entsprechen, wird der Videoinhalt im rechteckigen Anzeigebereich des Video-Players zentriert.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Video-Players:

```
.s7video360viewer .s7video360player
```

**CSS-Eigenschaften des Video-Players**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Hauptansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können die Fehlermeldung lokalisieren, die angezeigt wird, wenn das System das Video nicht abspielen kann.

Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Beispiel: So richten Sie einen Video-Viewer ein, wobei die Größe des Video-Players auf 512 x 288 Pixel eingestellt ist.

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

Das Erscheinungsbild der Pufferanimation wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7video360player .s7waiticon
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
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
