---
title: Video-Player-Symboleffekt
description: Das Wiedergabesymbol wird im Videoansichtsbereich überlagert. Er wird angezeigt, wenn das Video angehalten oder das Ende des Videos erreicht wird, und hängt auch vom IconEffect-Parameter ab.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# Video-Player-Symboleffekt{#video-player-icon-effect}

Das Wiedergabesymbol wird im Videoansichtsbereich überlagert. Er wird angezeigt, wenn das Video angehalten oder das Ende des Videos erreicht wird, und hängt auch vom IconEffect-Parameter ab.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild des Wiedergabesymbols wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**CSS-Eigenschaften des Wiedergabesymbols**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das angezeigte Bild für das Wiedergabesymbol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Wiedergabesymbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Spielsymbols. </p> </td> 
  </tr> 
 </tbody> 
</table>

Symboleffekt unterstützt die `state` Attributauswahl. Der `state="play"` wird verwendet, wenn das Video inmitten der Wiedergabe angehalten wird, und `state="replay"` wird verwendet, wenn sich der Abspielkopf am Ende des Streams befindet.

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Richten Sie ein Wiedergabesymbol von 100 x 100 Pixel ein.

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
