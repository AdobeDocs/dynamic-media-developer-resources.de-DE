---
title: Farbfelder
description: Muster bestehen aus einer Zeile von Miniaturbildern mit optionalen Bildlauftasten auf der linken und rechten Seite. Bildlauftasten werden nur dann auf dem Desktop angezeigt, wenn alle Miniaturansichten nicht in die Container-Breite passen. Auf Mobilgeräten oder wenn Miniaturansichten in die Container-Breite passen, werden die Bildlauftasten nicht angezeigt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 7eaa4a6e-98e8-477b-9f45-66f8a79dfd85
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Farbfelder{#swatches}

Muster bestehen aus einer Zeile von Miniaturbildern mit optionalen Bildlauftasten auf der linken und rechten Seite. Bildlauftasten werden nur dann auf dem Desktop angezeigt, wenn alle Miniaturansichten nicht in die Container-Breite passen. Auf Mobilgeräten oder wenn Miniaturansichten in die Container-Breite passen, werden die Bildlauftasten nicht angezeigt.

`.s7zoomviewer .s7swatches`

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Farbmuster-Containers wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7zoomviewer .s7zoomresetbutton
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Farbfelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Farbfelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Vertikale Farbfelder versetzen sich relativ zum Viewer-Container. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten von Farbfeldern auf 460 x 100 Pixel.

```
.s7zoomviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

Der Abstand zwischen den Musterminiaturansichten wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7zoomviewer .s7swatches .s7thumbcell`

<table id="table_565B354FEA814804A0BE3978E1242110"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Die Größe des horizontalen und vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand der Miniaturansichten entspricht der Summe des linken und rechten Rands, der für <span class="codeph"> .s7thumbcell </span> festgelegt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel**

So legen Sie den Abstand sowohl vertikal als auch horizontal auf zehn Pixel fest.

```
.s7zoomviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild der einzelnen Miniaturansichten wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7zoomviewer .s7swatches .s7thumb`

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
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand der Miniaturansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniaturansichten unterstützen die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden können. Insbesondere entspricht `state="selected"` der Miniaturansicht des Bildes, das derzeit in der Hauptansicht angezeigt wird, `state="default"` dem Rest der Miniaturansichten und `state="over"` beim Bewegen der Maus.

Beispiel: Zum Einrichten von Miniaturansichten mit 56 x 56 Pixel, einem hellgrauen Standardrahmen und einem dunkelgrauen ausgewählten Rahmen.

```
.s7zoomviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7zoomviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7zoomviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Das Erscheinungsbild der linken und rechten Bildlaufschaltflächen wird mit den folgenden CSS-Klassenselektoren gesteuert:

`.s7zoomviewer .s7swatches .s7scrollleftbutton`

`.s7zoomviewer .s7swatches .s7scrollrightbutton`

Es ist nicht möglich, Bildlaufschaltflächen mithilfe der CSS-Eigenschaften oben, links, unten und rechts zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

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
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, die verwendet werden kann, um unterschiedliche Schaltflächenzustände anzuwenden: `up`, `down`, `over` und `disabled`.

Die QuickInfos für Schaltflächen können lokalisiert werden. Siehe [Lokalisierung von Elementen der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Zum Einrichten von Bildlaufschaltflächen mit einer Größe von 56 x 56 Pixel und einer für jeden Status unterschiedlichen Grafik.

```
.s7zoomviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7zoomviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
