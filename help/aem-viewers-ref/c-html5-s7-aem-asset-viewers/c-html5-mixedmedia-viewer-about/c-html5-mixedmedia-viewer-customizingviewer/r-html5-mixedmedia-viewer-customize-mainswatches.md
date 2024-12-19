---
title: Hauptfarbfelder
description: Hauptmuster bestehen aus einer Reihe von Miniaturbildern mit optionalen Bildlaufschaltflächen auf der linken und rechten Seite. Bildlaufschaltflächen sind nur dann auf der Arbeitsfläche sichtbar, wenn nicht alle Miniaturen in die Breite des Containers passen. Auf Mobilgeräten oder wenn Miniaturen in die Container-Breite passen, werden die Bildlaufschaltflächen nicht angezeigt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e6ff32bf-f85a-4288-a0e5-34487229a9d9
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Hauptfarbfelder{#main-swatches}

Hauptmuster bestehen aus einer Reihe von Miniaturbildern mit optionalen Bildlaufschaltflächen auf der linken und rechten Seite. Bildlaufschaltflächen sind nur dann auf der Arbeitsfläche sichtbar, wenn nicht alle Miniaturen in die Breite des Containers passen. Auf Mobilgeräten oder wenn Miniaturen in die Container-Breite passen, werden die Bildlaufschaltflächen nicht angezeigt.

Das Erscheinungsbild des Farbfeld-Containers wird mit dem CSS-Klassenselektor gesteuert:

```
.s7mixedmediaviewer .s7swatches
```

**CSS-Eigenschaften der Farbfelder**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Farbfelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Die vertikalen Farbfelder, die relativ zum Viewer-Container versetzt sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie Farbfelder mit einer Höhe von 100 Pixel ein.

```
.s7mixedmediviewer .s7swatches { 
 height: 100px;  
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Der Abstand zwischen den Musterminiaturen wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7mixedmediaviewer .s7swatches .s7thumbcell`

<table id="table_ECE063DB98154E099FB024F66FF877D7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Größe des horizontalen und vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand zwischen den Miniaturen entspricht der Summe der linken und rechten Ränder, die für <span class="codeph"> s7thumbcell-</span> festgelegt wurden. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel**

So legen Sie den Abstand sowohl vertikal als auch horizontal auf zehn Pixel fest.

```
.s7mixedmediaviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild der einzelnen Miniaturen wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7mixedmediaviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniatur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen der Miniatur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>„Miniaturansicht“ unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichtszustände angewendet werden können. Insbesondere entspricht `state="selected"` der Miniatur für das Bild, das derzeit in der Hauptansicht angezeigt wird, `state="default"` entspricht dem Rest der Miniaturen, und `state="over"` wird beim Bewegen des Mauszeigers verwendet.

Beispiel: Für Miniaturen mit einer Größe von 56 x 56 Pixel wird ein hellgrauer Standardrahmen und ein dunkelgrauer Rahmen ausgewählt.

```
.s7mixedmediaviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7mixedmediaviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7mixedviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Der Typ des Assets wird als Symbol angezeigt, das über dem Miniaturbild eingeblendet wird, und wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay`

<table id="table_460FC57D12CC4B52B3782F4DFAC3A194"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Symbolüberlagerung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Symbolüberlagerung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Überlagerung unterstützt den `type`-Attributselektor mit den folgenden möglichen Werten: `image` (für einzelne Bilder), `swatchset` (für Mustersets), `spinset` (für Rotationssets) und `video` (für einzelne Videos oder adaptive Videosets).

Beispiel: So richten Sie Symbolüberlagerungen für Rotationssets, Mustersets und Videos ein:

```
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="swatchset"] { 
 background-image: url(images/v2/ThumbOverlaySwatchSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="spinset"] { 
 background-image: url(images/v2/ThumbOverlaySpinSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="video"] { 
 background-image: url(images/v2/ThumbOverlayVideo.png);  
}
```

Die Darstellung der linken und rechten Bildlaufschaltflächen wird mit den folgenden CSS-Klassenselektoren gesteuert:

`.s7mixedmediaviewer .s7swatches .s7scrollleftbutton`

`.s7mixedmediaviewer .s7swatches .s7scrollrightbutton`

Scroll-Schaltflächen können nicht mit den Eigenschaften CSS `top`, `left`, `bottom` und `right` positioniert werden. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können: `up`, `down`, `over` und `disabled`.

Die QuickInfos für die Schaltfläche können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) für weitere Informationen.

Beispiel: So richten Sie Bildlaufschaltflächen ein, die eine Größe von 56 x 56 Pixeln haben und für jeden Status unterschiedliche Grafiken aufweisen.

```
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
