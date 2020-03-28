---
description: Muster bestehen aus einer Reihe von Miniaturbildern mit optionalen Bildlaufschaltflächen auf der linken und rechten Seite.
seo-description: Muster bestehen aus einer Reihe von Miniaturbildern mit optionalen Bildlaufschaltflächen auf der linken und rechten Seite.
seo-title: Muster
solution: Experience Manager
title: Muster
topic: Dynamic media
uuid: 92360088-7199-49c3-80ee-e175d234a78e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Muster{#swatches}

Muster bestehen aus einer Reihe von Miniaturbildern mit optionalen Bildlaufschaltflächen auf der linken und rechten Seite.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Bildlaufschaltflächen sind nur dann auf dem Desktop sichtbar, wenn alle Miniaturansichten nicht in die Breite des Containers passen. Auf Mobilgeräten oder, wenn Miniaturansichten in die Breite des Containers passen, werden keine Bildlaufschaltflächen angezeigt.

**CSS-Eigenschaften der Muster**

Das Erscheinungsbild des Containers &quot;swatches&quot;wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col2"> <p>Die Höhe der Muster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Die vertikalen Farbfelder versetzen sich relativ zum Viewer-Container. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie Muster auf 460 x 100 Pixel ein:

```
.s7flyoutviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

**CSS-Eigenschaften des Abstands des Miniaturansichten-Farbfelds**

Der Abstand zwischen den Musterminiaturen wird mit der CSS-Klassenauswahl gesteuert:

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
   <td colname="col2"> <p> Die Größe des horizontalen und vertikalen Randes um die einzelnen Miniaturansichten. Der tatsächliche Abstand der Miniaturansichten entspricht der Summe des linken und rechten Randes, der für <span class="codeph"> .s7thumbcell festgelegt wurde </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So legen Sie den Abstand sowohl vertikal als auch horizontal auf 10 Pixel fest:

```
.s7flyoutviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

**CSS-Eigenschaften der Miniaturansichten**

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
   <td colname="col2"> <p>Der Rand der Miniaturansichten. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Die Miniaturansicht unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden. Insbesondere `state="selected"` entspricht dies der Miniaturansicht des Bildes, das derzeit in der Haupt-Ansicht angezeigt wird, dem Rest der Miniaturbilder `state="default"` entspricht und beim Bewegen der Maus verwendet `state="over"` wird.

Beispiel: Zum Einrichten von Miniaturbildern mit 56 x 56 Pixel, einem hellgrauen Standardrand und einem dunkelgrauen Rahmen:

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

Die Darstellung der Schaltflächen für den Bildlauf nach links und rechts wird mit den folgenden CSS-Klassenselektoren gesteuert:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton 
.s7flyoutviewer .s7swatches .s7scrollrightbutton
```

Es ist nicht möglich, Bildlaufschaltflächen mithilfe von CSS `top`, `left`, `bottom`und `right` -Eigenschaften zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

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
   <td colname="col2"> <p>Die Höhe der Bildlauftaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#section-b0af39db1af74561aea9fddcc8cdc2c7" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf Schaltflächenzustände `up`, `down`, `over`und `disabled`angewendet werden.

Die QuickInfos für Schaltflächen können lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) der Benutzeroberfläche.

Beispiel: So richten Sie Bildlaufschaltflächen ein, die 56 x 56 Pixel groß sind und für jeden Status ein anderes Bildmaterial aufweisen:

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

