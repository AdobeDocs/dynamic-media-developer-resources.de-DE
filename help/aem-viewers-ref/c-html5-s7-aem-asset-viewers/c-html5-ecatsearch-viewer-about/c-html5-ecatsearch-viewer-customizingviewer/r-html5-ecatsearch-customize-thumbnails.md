---
title: Miniaturen
description: Miniaturen bestehen aus einem Raster von Miniaturbildern mit einer optionalen Bildlaufleiste auf der rechten Seite, um einen vertikalen Bildlauf zu ermöglichen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 25032917-237c-4227-92bd-ce66a6d003a0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# Miniaturen{#thumbnails}

Miniaturen bestehen aus einem Raster von Miniaturbildern mit einer optionalen Bildlaufleiste auf der rechten Seite, um einen vertikalen Bildlauf zu ermöglichen.

Das Umschalten zwischen Miniaturen erfolgt durch Klicken auf die Schaltfläche Miniaturen in der Hauptsteuerleiste. Wenn Miniaturansichten aktiv sind, werden sie im modalen Modus angezeigt, der über der Viewer-Benutzeroberfläche überlagert ist. Durch die Viewer-Logik wird die Größe des Containers für Miniaturen automatisch auf den gesamten Viewer-Bereich geändert.

Das Erscheinungsbild des Containers für Miniaturen wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7thumbnailgridview`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Versatz des Containers für Miniaturen vom oberen Rand des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Der obere Rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rand links </span> </p> </td> 
   <td colname="col2"> <p>Der linke Rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rand rechts </span> </p> </td> 
   <td colname="col2"> <p>Der rechte Rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rand unten </span> </p> </td> 
   <td colname="col2"> <p>Der untere Rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Bereichs Miniaturen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - Sie können Miniaturen so einrichten, dass sie einen Abstand von 32 Pixeln von oben, 5 Pixeln Seitenrändern links und rechts und 8 Pixeln Seitenrändern unten und mit `0xDDDDDD` Hintergrund haben.

```
.s7ecatalogsearchviewer .s7thumbnailgridview { 
 top: 32px; 
 margin-left: 5px; 
 margin-right: 5px; 
 margin-bottom: 8px; 
 background-color: rgb(221, 221, 221); 
}
```

Der Abstand zwischen Miniaturen wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumbcell`

<table id="table_1D93AB60E57F49A8838EA825CD6B7897"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Größe des horizontalen und vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand zwischen horizontalen Miniaturen entspricht der Summe aus dem linken und rechten Rand, die für <span class="codeph"> s7thumbcell-</span> festgelegt ist. Der vertikale Abstand zwischen den Miniaturen entspricht der Summe aus dem oberen und unteren Rand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - Zum Festlegen eines Bereichs von 10 Pixel sowohl vertikal als auch horizontal.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild einzelner Miniaturansichten wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb`

<table id="table_1D973EA6C36947F092AAA16CFE9B44A1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Der Rahmen der Miniatur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der Miniaturansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Auf Touch-Geräten kann der Viewer bei einer Drehung in den Hochformat-Modus die Größe der Miniaturen auf die Hälfte der konfigurierten Größe reduzieren, falls er beschließt, die Katalogstreuung in einzelne Seiten aufzuteilen.

>[!NOTE]
>
>„Miniaturansicht“ unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichtszustände angewendet werden können. Insbesondere entspricht `state="selected"` der Miniatur für das Bild, das derzeit in der Hauptansicht angezeigt wird, `state="default"` entspricht dem Rest der Miniaturen, und `state="over"` wird beim Bewegen des Mauszeigers verwendet.

Beispiel: So richten Sie Miniaturen mit einer Größe von 120 x 85 Pixel ein, die einen weißen Hintergrund, einen hellgrauen Standardrahmen und einen dunkelgrauen ausgewählten Rahmen aufweisen.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb { 
 width:120px; 
 height:85px; 
 background-color: rgb(255, 255, 255); 
 border: solid 1px #999999; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb[state="selected"]{ 
 border: solid 2px #666666; 
}
```

Das Erscheinungsbild der Miniaturbildbeschriftung wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7label`

<table id="table_E242176042F247F8B51A0D5ADB645E20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - zum Einrichten von Beschriftungen für die Verwendung der Helvetica®-Schriftart mit 14 Pixeln.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 12px; 
}
```

Wenn mehr Miniaturen vorhanden sind, als vertikal in die Ansicht passen, wird die vertikale Bildlaufleiste auf der rechten Seite gerendert. Das Erscheinungsbild des Bildlaufleistenbereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar`

<table id="table_F05EC87CD9A946DB9B4B2B48E0784168"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Bildlaufleiste, die vom oberen Rand des Bereichs „Miniaturen“ versetzt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Die vertikale Bildlaufleiste, die vom unteren Rand des Bereichs „Miniaturen“ versetzt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p> Der horizontale Bildlaufbalken, der vom rechten Rand des Bereichs Miniaturen versetzt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Bildlaufleiste ein, die 28 Pixel breit ist und einen 8-Pixel-Rand vom oberen, rechten und unteren Rand des Bereichs „Miniaturen“ aufweist.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar { 
 top:8px; 
 bottom:8px; 
 right:8px; 
 width:28px; 
}
```

Die Bildlaufleistenspur ist der Bereich zwischen den oberen und unteren Bildlaufschaltflächen. Die Komponente legt automatisch die Position und Höhe der Spur fest. Die Spur wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack`

<table id="table_EF1B91F9E984451EB0AB48175D917726"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite der Bildlaufleistenspur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Hintergrundfarbe der Bildlaufleistenspur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Bildlaufleistenspur ein, die 28 Pixel breit ist und einen halbtransparenten grauen Hintergrund hat.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Der Daumen der Bildlaufleiste bewegt sich vertikal innerhalb des Bereichs der Bildlaufspur. Die vertikale Position wird vollständig durch die Komponentenlogik gesteuert, die Daumenhöhe ändert sich jedoch je nach Inhaltsmenge nicht dynamisch. Die Höhe des Daumens und andere Aspekte werden mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb`

<table id="table_5C791F6E90E64E7A9F1DB7C9B2FDC528"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Ziehpunkts der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Miniaturansicht der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Der vertikale Abstand zwischen dem oberen Rand der Bildlaufleisten-Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Der vertikale Abstand zwischen dem unteren Rand der Bildlaufleisten-Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt den `state`-Attributselektor , mit dem verschiedene Skins auf die Miniaturstatus `up`, `down`, `over` und `disabled` angewendet werden können.

Beispiel - Zum Einrichten eines Thumbs für eine Bildlaufleiste mit 28 x 45 Pixel, mit 10 Pixel-Rändern oben und unten und unterschiedlichen Bildmaterialien für jeden Status.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

Die Darstellung der oberen und unteren Bildlaufschaltflächen wird mit den folgenden CSS-Klassenselektoren gesteuert:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton`

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton`

Es ist nicht möglich, die Bildlaufschaltflächen mit den Eigenschaften CSS `top`, `left`, `bottom` und `right` zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

<table id="table_89E64A138ABF463F9650BB454F22D530"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltflächen unterstützen den `state`-Attributselektor , mit dem verschiedene Skins auf die verschiedenen Schaltflächenzustände `up`, `down`, `over` und `disabled` angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: So richten Sie Bildlaufschaltflächen ein, die 28 x 32 Pixel groß sind und für jeden Status unterschiedliche Grafiken aufweisen.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
