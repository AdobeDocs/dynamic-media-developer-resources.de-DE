---
description: Muster bestehen aus einer Reihe von Miniaturbildern mit optionalen Bildlaufschaltflächen auf der linken und rechten Seite. Bildlaufschaltflächen sind nur dann auf dem Desktop sichtbar, wenn alle Miniaturansichten nicht in die Breite des Containers passen. Auf Mobilgeräten oder, wenn Miniaturansichten in die Breite des Containers passen, werden die Bildlaufschaltflächen nicht angezeigt.
seo-description: Muster bestehen aus einer Reihe von Miniaturbildern mit optionalen Bildlaufschaltflächen auf der linken und rechten Seite. Bildlaufschaltflächen sind nur dann auf dem Desktop sichtbar, wenn alle Miniaturansichten nicht in die Breite des Containers passen. Auf Mobilgeräten oder, wenn Miniaturansichten in die Breite des Containers passen, werden die Bildlaufschaltflächen nicht angezeigt.
seo-title: Muster
solution: Experience Manager
title: Muster
topic: Dynamic media
uuid: d44e775d-5253-4990-98a4-84ff50db09b9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Muster{#swatches}

Muster bestehen aus einer Reihe von Miniaturbildern mit optionalen Bildlaufschaltflächen auf der linken und rechten Seite. Bildlaufschaltflächen sind nur dann auf dem Desktop sichtbar, wenn alle Miniaturansichten nicht in die Breite des Containers passen. Auf Mobilgeräten oder, wenn Miniaturansichten in die Breite des Containers passen, werden die Bildlaufschaltflächen nicht angezeigt.

`.s7zoomviewer .s7swatches`

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Containers &quot;swatches&quot;wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col2"> <p>Breite der Muster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Farbfelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Vertikale Farbfelder versetzen sich relativ zum Viewer-Container. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie Muster auf 460 x 100 Pixel ein.

```
.s7zoomviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

Der Abstand zwischen den Musterminiaturen wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col2"> <p> Die Größe des horizontalen und vertikalen Randes um die einzelnen Miniaturansichten. Der tatsächliche Abstand der Miniaturansichten entspricht der Summe des linken und rechten Randes, der für <span class="codeph"> .s7thumbcell festgelegt wurde </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel**

So legen Sie den Abstand sowohl vertikal als auch horizontal auf 10 Pixel fest.

```
.s7zoomviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild der einzelnen Miniaturansicht wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

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
>Miniaturansicht unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden können. Insbesondere `state="selected"` entspricht dies der Miniaturansicht des Bildes, das derzeit in der Haupt-Ansicht angezeigt wird, dem Rest der Miniaturbilder `state="default"` entspricht und beim Bewegen der Maus verwendet `state="over"` wird.

Beispiel: Zum Einrichten von Miniaturbildern mit 56 x 56 Pixel, einem hellgrauen Standardrand und einem dunkelgrauen ausgewählten Rand.

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

Die Darstellung der Schaltflächen für den linken und rechten Bildlauf wird mit den folgenden CSS-Klassenselektoren gesteuert:

`.s7zoomviewer .s7swatches .s7scrollleftbutton`

`.s7zoomviewer .s7swatches .s7scrollrightbutton`

Es ist nicht möglich, Bildlaufschaltflächen mit den CSS-Eigenschaften top, left, bottom und right zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

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
   <td colname="col2"> <p>Höhe der Bildlauftaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können: `up`, `down`, `over`und `disabled`.

Die QuickInfos für Schaltflächen können lokalisiert werden. Siehe [Lokale Anpassung der Elemente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)der Benutzeroberfläche.

Beispiel: Zum Einrichten von Bildlaufschaltflächen mit 56 x 56 Pixeln und unterschiedlicher Grafik für jeden Status.

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

