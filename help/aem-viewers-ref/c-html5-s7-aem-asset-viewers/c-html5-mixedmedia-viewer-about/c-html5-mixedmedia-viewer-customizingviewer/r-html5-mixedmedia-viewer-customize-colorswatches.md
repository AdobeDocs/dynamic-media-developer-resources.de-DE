---
title: Farbmuster
description: Farbmuster bestehen aus einer Zeile von Miniaturbildern mit optionalen Bildlauftasten auf der linken und rechten Seite. Farbmuster sind nur auf dem Desktop sichtbar, wenn alle Miniaturansichten nicht in die Breite des Containers passen. Auf Mobilgeräten oder wenn Miniaturansichten in die Container-Breite passen, werden keine Bildlauftasten angezeigt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a73d1c9-362d-48a5-96c9-3d543e68ebec
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---

# Farbmuster{#color-swatches}

Farbmuster bestehen aus einer Zeile von Miniaturbildern mit optionalen Bildlauftasten auf der linken und rechten Seite. Farbmuster sind nur auf dem Desktop sichtbar, wenn alle Miniaturansichten nicht in die Breite des Containers passen. Auf Mobilgeräten oder wenn Miniaturansichten in die Container-Breite passen, werden keine Bildlauftasten angezeigt.

Das Erscheinungsbild des Farbmuster-Containers wird mit der CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7colorswatches .s7swatches
```

**CSS-Eigenschaften der Farbmuster**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Die Breite der Farbfelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Farbfelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Die vertikalen Farbfelder versetzen sich relativ zum Viewer-Container. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten von Farbfeldern mit einer Höhe von 100 Pixel.

```
.s7mixedmediviewer .s7colorswatches .s7swatches { 
 height: 100px;  
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Der Abstand zwischen den Musterminiaturansichten wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumbcell`

<table id="table_ECE063DB98154E099FB024F66FF877D7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Die Größe des horizontalen und vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand der Miniaturansichten entspricht der Summe des linken und rechten Rands, der für <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel**

So legen Sie den Abstand sowohl vertikal als auch horizontal auf zehn Pixel fest.

```
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild der einzelnen Miniaturansichten wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Rand der Miniaturansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniaturansichten unterstützen die `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Miniaturansichten anzuwenden. Insbesondere `state="selected"` entspricht der Miniaturansicht für das Bild, das derzeit in der Hauptansicht angezeigt wird, `state="default"` dem Rest der Miniaturansichten entspricht und `state="over"` wird beim Bewegen der Maus verwendet.

Beispiel: Zum Einrichten von Miniaturansichten mit 56 x 56 Pixel, einem hellgrauen Standardrahmen und einem dunkelgrauen ausgewählten Rahmen.

```
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7mixedviewer .s7colorswatches .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Das Erscheinungsbild der linken und rechten Bildlaufschaltflächen wird mit den folgenden CSS-Klassenselektoren gesteuert:

`.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton`

`.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton`

Es ist nicht möglich, Bildlaufschaltflächen mithilfe von CSS zu positionieren `top`, `left`, `bottom`, und `right` Eigenschaften. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden: `up`, `down`, `over`, und `disabled`.

Beispiel: Zum Einrichten von Bildlaufschaltflächen mit einer Größe von 56 x 56 Pixel und einer für jeden Status unterschiedlichen Grafik.

```
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
