---
description: Das Wiedergabesymbol wird im Videoansichtsbereich überlagert. Es wird angezeigt, wenn das Video angehalten wird oder wenn das Ende des Videos erreicht wird, und es hängt auch vom iconffekt -Parameter ab.
solution: Experience Manager
title: Videoplayer-Symboleffekt
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# Videoplayer-Symboleffekt{#video-player-icon-effect}

Das Wiedergabesymbol wird im Videoansichtsbereich überlagert. Es wird angezeigt, wenn das Video angehalten wird oder wenn das Ende des Videos erreicht wird, und es hängt auch vom iconffekt -Parameter ab.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild des Wiedergabesymbols wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**CSS-Eigenschaften des Wiedergabesymbols**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das angezeigte Bild für das Wiedergabesymbol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Wiedergabesymbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Wiedergabesymbols. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Symboleffekt unterstützt die Attributauswahl `state`. `state="play"` wird verwendet, wenn das Video während der Wiedergabe angehalten wird, und  `state="replay"` wird verwendet, wenn sich der Abspielkopf am Ende des Streams befindet.

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Richten Sie ein Wiedergabesymbol mit 100 x 100 Pixel ein.

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
