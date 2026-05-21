---
title: Video-Player
description: Der Video-Player ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2741821f-78fe-44d4-8604-fee10086e0a0
TQID: 'https://experienceleague.adobe.com/mVDQWuBQZT9--O4V3XCrPRasFvG8x7fIsxqQLFsMpNU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 0%

---

# Video-Player{#video-player}

Der Video-Player ist der rechteckige Bereich, in dem der Videoinhalt im Viewer angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn die Abmessungen des wiedergegebenen Videos nicht den Abmessungen des Video-Players entsprechen, wird der Videoinhalt im rechteckigen Anzeigebereich des Video-Players zentriert.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Video-Players:

```
.s7videoviewer .s7videoplayer
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

Die Fehlermeldung, die angezeigt wird, wenn das System das Video nicht abspielen kann, kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: So richten Sie einen Video-Viewer ein, wobei die Größe des Video-Players auf 512 x 288 Pixel eingestellt ist.

```
.s7videoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

Untertitel werden in einen internen Container im Video-Player eingefügt. Die Position dieses Containers wird durch unterstützte WebVTT-Positionierungsoperatoren gesteuert. Der Beschriftungstext selbst befindet sich in diesem Container und sein Stil wird mit dem folgenden CSS-Klassenselektor gesteuert:

`. s7videoviewer .s7 videoplayer .s7caption`

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
.s7videoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

Das Erscheinungsbild der Pufferanimation wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7videoplayer .s7waiticon
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
.s7videoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
