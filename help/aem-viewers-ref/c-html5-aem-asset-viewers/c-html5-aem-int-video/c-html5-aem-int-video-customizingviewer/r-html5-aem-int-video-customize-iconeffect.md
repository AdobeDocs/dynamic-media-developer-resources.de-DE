---
description: Das Wiedergabesymbol wird im Hauptbereich der Ansicht überlagert. Es wird angezeigt, wenn das Video angehalten wird oder das Ende des Videos erreicht wird, und es hängt auch vom iconeffect-Parameter ab.
seo-description: Das Wiedergabesymbol wird im Hauptbereich der Ansicht überlagert. Es wird angezeigt, wenn das Video angehalten wird oder das Ende des Videos erreicht wird, und es hängt auch vom iconeffect-Parameter ab.
seo-title: Symbol, Effekt
solution: Experience Manager
title: Symbol, Effekt
topic: Dynamic media
uuid: 81c9c344-5256-4015-8d02-abbf09dca541
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Icon effect{#icon-effect}

Das Wiedergabesymbol wird im Hauptbereich der Ansicht überlagert. Es wird angezeigt, wenn das Video angehalten wird oder das Ende des Videos erreicht wird, und es hängt auch vom iconeffect-Parameter ab.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild des Wiedergabesymbols wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer . s7videoplayer .s7iconeffect
```

**CSS-Eigenschaften des Wiedergabesymbols**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das angezeigte Bild für das Wiedergabesymbol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
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

Der Symboleffekt unterstützt die `state` Attributauswahl. `state="play"` wird verwendet, wenn das Video in der Mitte der Wiedergabe angehalten wird, und `state="replay"` wird verwendet, wenn sich der Abspielkopf am Ende des Streams befindet.

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Richten Sie ein Wiedergabesymbol im Format 100 x 100 Pixel ein.

```
.s7interactivevideoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7interactivevideoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

