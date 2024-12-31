---
title: Inhaltsverzeichnis
description: Das Inhaltsverzeichnis ist eine Schaltfläche, die in der Hauptsteuerleiste positioniert wird. Wenn aktiviert, wird ein Dropdown-Bedienfeld mit einer Liste von Seitenindizes und Beschriftungen angezeigt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 9b61e269-201d-4083-9c47-0b73d55aa6ed
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 0%

---

# Inhaltsverzeichnis{#table-of-contents}

Das Inhaltsverzeichnis ist eine Schaltfläche, die in der Hauptsteuerleiste positioniert wird. Wenn aktiviert, wird ein Dropdown-Bedienfeld mit einer Liste von Seitenindizes und Beschriftungen angezeigt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Basierend auf der Konfiguration kann die Liste alle Seiten enthalten, die im Katalog vorhanden sind, oder nur die Seiten, für die explizite Kennzeichnungen definiert sind. Auf Desktop-Systemen wird rechts eine Bildlaufleiste angezeigt, wenn die Liste länger ist als die verfügbare Bildschirmgröße.

Die Position und Größe der Inhaltsverzeichnisschaltfläche in der Viewer-Benutzeroberfläche werden mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer .s7tableofcontents
```

**CSS-Eigenschaften des Inhaltsverzeichnisses**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Der Versatz vom oberen Rand der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rand links </span> </p> </td> 
   <td colname="col2"> <p> Der Abstand zur nächsten Schaltfläche auf der linken Seite oder zur linken Seite der Steuerleiste, wenn es sich um die erste Schaltfläche in einer Zeile handelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Schaltfläche für das Inhaltsverzeichnis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p> Die Höhe der Schaltfläche für das Inhaltsverzeichnis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel : Zum Einrichten einer Schaltfläche für das Inhaltsverzeichnis, die 4 Pixel vom unteren Rand und 43 Pixel vom linken Rand der Hauptsteuerleiste entfernt positioniert wird. Die Größe beträgt 28 x 28 Pixel, und für jeden der vier verschiedenen Schaltflächenstatus wird ein anderes Bild angezeigt:

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

Das Erscheinungsbild des Dropdown-Bedienfelds wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**CSS-Eigenschaften des Dropdown-Bedienfelds**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe des Dropdown-Bedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Interner Versatz zwischen den Bereichsgrenzen und dem Inhalt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Legen Sie Schatten um das Bedienfeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Es ist nicht möglich, die Größe oder Position des Dropdown-Bedienfelds aus CSS zu steuern. Die Komponente verwaltet ihr Layout programmgesteuert.

Beispiel: Ein Dropdown-Bedienfeld mit einem halbtransparenten schwarzen Hintergrund, einem 5-Pixel-Rand um den Inhalt und einem Schlagschatten wird eingerichtet:

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

Das Erscheinungsbild der einzelnen Elemente wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**CSS-Eigenschaften des Elements**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Elements. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Interner Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ein Dropdown-Listenelement unterstützt den `state`-Attributselektor , der verwendet werden kann, um verschiedene Skins auf den Mauszeiger und ausgewählte Elementzustände anzuwenden.

Beispiel: Ein Dropdown-Element mit einer Helvetica®-Schriftart von 14 Pixel und einer Höhe von 19 Pixel einrichten. Ein Element hat beim Bewegen des Mauszeigers einen dunkelgrauen Hintergrund und bei Auswahl einen hellgrauen Hintergrund:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Ein -Element, das den Seitenindex anzeigt, wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**CSS-Eigenschaften des Seitenindex**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> Minimale Elementbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> Maximale Elementbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Abstand rechts </span> </p> </td> 
   <td colname="col2"> <p> Abstand zwischen Seitenindex und Seitenbeschriftung. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Es ist möglich, den Seitenindex vollständig auszublenden, indem Sie `display:none` für die `s7index` CSS-Klasse festlegen.

Beispiel 1: Einrichten eines Seitenindexes mit einer Mindestbreite von 40 Pixel, einer maximalen Breite von 70 Pixel und einem 5-Pixel-Rand auf der rechten Seite:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Beispiel 2: Ausblenden des Seitenindex:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

Die Seitenbeschriftung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**CSS-Eigenschaften der Seitenbeschriftung**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> Minimale Elementbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> Maximale Elementbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - Richten Sie einen Seitenindex mit einer Mindestbreite von 40 Pixel und einer maximalen Breite von 240 Pixel ein:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Wenn es mehr Elemente gibt, als vertikal in das Dropdown-Bedienfeld passen können, und das System ein Desktop ist, rendert die Komponente eine vertikale Bildlaufleiste auf der rechten Seite des Bedienfelds. Das Erscheinungsbild des Bildlaufleistenbereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Bildlaufleiste, die vom oberen Rand des Bedienfeldbereichs versetzt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Bildlaufleiste, die vom unteren Rand des Bedienfeldbereichs versetzt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p> Der horizontale Bildlaufbalken, der vom rechten Rand des Bedienfeldbereichs versetzt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - Richten Sie eine Bildlaufleiste ein, die 28 Pixel breit ist und keinen Rand für den oberen, rechten oder unteren Bereich des Bedienfelds hat:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

Die Bildlaufleistenspur ist der Bereich zwischen den oberen und unteren Bildlaufschaltflächen. Die Komponente legt automatisch die Position und Höhe der Spur fest. Die Spur wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**CSS-Eigenschaften der Scroll-Spur**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Spurbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der Spur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie eine Bildlaufleistenspur ein, die 28 Pixel breit ist und einen halbtransparenten grauen Hintergrund hat:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Der Daumen der Bildlaufleiste bewegt sich vertikal innerhalb des Bereichs der Bildlaufspur. Seine vertikale Position wird durch die Komponentenlogik gesteuert. Die Höhe der Daumen ändert sich jedoch nicht dynamisch je nach Inhaltsmenge. Sie können die Höhe der Miniaturen und andere Aspekte mit dem folgenden CSS-Klassenselektor konfigurieren:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**CSS-Eigenschaften des Thumb der Bildlaufleiste**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Daumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Daumenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Abstand zwischen dem oberen Ende der Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Der vertikale Abstand zwischen dem unteren Ende der Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt den `state`-Attributselektor , mit dem verschiedene Skins auf die `up`-, `down`-, `over`- und `disabled` angewendet werden können.

Beispiel: Richten Sie einen Thumb für die Bildlaufleiste ein, der 28 x 45 Pixel groß ist, oben und unten 10 Pixelränder aufweist und für jeden Status unterschiedliche Grafiken aufweist:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

Die Darstellung der oberen und unteren Bildlaufschaltflächen wird mit den folgenden CSS-Klassenselektoren gesteuert:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Es ist nicht möglich, die Bildlaufschaltflächen mit den Eigenschaften CSS `top`, `left`, `bottom` und `right` zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der Schaltfläche Nach oben scrollen und Nach unten scrollen**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
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
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Button unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf die Schaltflächenzustände `up`, `down`, `over` und `disabled` angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel - Richten Sie Scroll-Schaltflächen ein, die eine Größe von 28 x 32 Pixeln haben und unterschiedliche Grafiken für jeden Status aufweisen:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
