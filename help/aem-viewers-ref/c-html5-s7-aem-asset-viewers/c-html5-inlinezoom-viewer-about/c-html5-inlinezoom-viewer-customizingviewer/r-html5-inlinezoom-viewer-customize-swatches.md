---
title: Farbfelder
description: Muster bestehen aus einer Zeile von Miniaturbildern mit optionalen Bildlauftasten auf der linken und rechten Seite.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: bd385b06-b8d6-4c6e-83fd-65a3d1c105c5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 2%

---

# Farbfelder{#swatches}

Muster bestehen aus einer Zeile von Miniaturbildern mit optionalen Bildlauftasten auf der linken und rechten Seite.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Bildlaufschaltflächen sind nur dann auf dem Desktop sichtbar, wenn alle Miniaturansichten nicht in die Breite des Containers passen. Auf Mobilgeräten oder wenn Miniaturansichten in die Container-Breite passen, werden keine Bildlauftasten angezeigt.

**CSS-Eigenschaften der Muster**

Das Erscheinungsbild des Farbmuster-Containers wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7flyoutviewer .s7swatches
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
   <td colname="col2"> <p> Die Breite der Farbfelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Farbfelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Die vertikalen Farbfelder versetzen sich relativ zum Viewer-Container. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten von Farbfeldern auf 460 x 100 Pixel:

```
.s7flyoutviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

**CSS-Eigenschaften des Abstands der Miniaturansichten für Muster**

Der Abstand zwischen Musterminiaturansichten wird mit dem CSS-Klassenselektor gesteuert:

```
.s7flyoutviewer .s7swatches .s7thumbcell
```

<table id="table_70FAD50E38EB4647B8FAB832F552BBB8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
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

Beispiel: Zum Festlegen eines Abstands von 10 Pixel sowohl vertikal als auch horizontal:

```
.s7flyoutviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

**CSS-Eigenschaften der Muster für Miniaturansichten**

Das Erscheinungsbild der einzelnen Miniaturansichten wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7flyoutviewer .s7swatches .s7thumb
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Miniaturansichten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Miniaturansichten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Der Rahmen der Miniaturansichten. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniaturansichten unterstützen die `state` -Attributauswahl, die verwendet wird, um verschiedene Skins auf verschiedene Miniaturansichten anzuwenden. Insbesondere `state="selected"` entspricht der Miniaturansicht für das Bild, das derzeit in der Hauptansicht angezeigt wird, `state="default"` dem Rest der Miniaturansichten entspricht und `state="over"` wird beim Bewegen der Maus verwendet.

Beispiel: Zum Einrichten von Miniaturansichten mit 56 x 56 Pixel, einem hellgrauen Standardrahmen und einem dunkelgrauen ausgewählten Rahmen:

```
.s7flyoutviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7flyoutviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7flyoutviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

**CSS-Eigenschaften der Schaltflächen für den linken und rechten Bildlauf**

Das Erscheinungsbild der linken und rechten Bildlaufschaltflächen wird mit den folgenden CSS-Klassenselektoren gesteuert:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton 
.s7flyoutviewer .s7swatches .s7scrollrightbutton
```

Es ist nicht möglich, Bildlaufschaltflächen mithilfe von CSS zu positionieren `top`, `left`, `bottom`, und `right` Eigenschaften. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#section-b0af39db1af74561aea9fddcc8cdc2c7" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` Attributauswahl, die verwendet wird, um verschiedene Skins auf Schaltflächenstatus anzuwenden `up`, `down`, `over`, und `disabled`.

Die QuickInfos für Schaltflächen können lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) für weitere Informationen.

Beispiel: Zum Einrichten von Bildlaufschaltflächen mit einer Größe von 56 x 56 Pixel und unterschiedlicher Grafik für jeden Status:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
