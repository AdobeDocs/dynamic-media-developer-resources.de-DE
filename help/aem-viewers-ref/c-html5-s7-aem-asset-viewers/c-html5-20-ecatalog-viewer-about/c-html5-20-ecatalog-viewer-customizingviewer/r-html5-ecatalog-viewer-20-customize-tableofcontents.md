---
description: Das Inhaltsverzeichnis ist eine Schaltfläche in der Hauptsteuerungsleiste. Wenn diese Option aktiviert ist, wird ein Dropdownfeld mit einer Liste von Seitenindizes und -beschriftungen angezeigt.
seo-description: Das Inhaltsverzeichnis ist eine Schaltfläche in der Hauptsteuerungsleiste. Wenn diese Option aktiviert ist, wird ein Dropdownfeld mit einer Liste von Seitenindizes und -beschriftungen angezeigt.
seo-title: Inhaltsverzeichnis
solution: Experience Manager
title: Inhaltsverzeichnis
topic: Dynamic media
uuid: e5da89b4-fd3f-41ab-bc55-d43c2999d4b7
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 2%

---


# Inhaltsverzeichnis{#table-of-contents}

Das Inhaltsverzeichnis ist eine Schaltfläche in der Hauptsteuerungsleiste. Wenn diese Option aktiviert ist, wird ein Dropdownfeld mit einer Liste von Seitenindizes und -beschriftungen angezeigt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Je nach Konfiguration kann die Liste alle im Katalog vorhandenen Seiten oder nur die Seiten mit expliziten Bezeichnungen enthalten. Wenn die Liste auf Desktop-Systemen länger als die verfügbare Bildschirmgröße ist, wird rechts eine Bildlaufleiste angezeigt.

Die Position und Größe der Inhaltsverzeichnisschaltfläche in der Benutzeroberfläche des Viewers werden mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7tableofcontents
```

**CSS-Eigenschaften des Inhaltsverzeichnisses**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Der Offset vom oberen Rand der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Der Abstand zur nächsten Schaltfläche links oder zur linken Seite der Steuerungsleiste, wenn dies die erste Schaltfläche in einer Zeile ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Inhaltsverzeichnisses. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Die Höhe der Inhaltsverzeichnis-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Legen Sie eine Inhaltsverzeichnis-Schaltfläche fest, die 4 Pixel von der unteren Seite und 43 Pixel von der linken Seite der Hauptsteuerungsleiste positioniert wird. Die Größe beträgt 28 x 28 Pixel, und für jeden der vier Schaltflächenzustände wird ein anderes Bild angezeigt:

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

Das Erscheinungsbild des Dropdown-Bedienfelds wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**CSS-Eigenschaften des Dropdown-Bedienfelds**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe des Dropdown-Bedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Interner Offset zwischen den Bereichsgrenzen und dem Inhalt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow  </span> </p> </td> 
   <td colname="col2"> <p> Schlagschatten um das Bedienfeld </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Die Größe oder Position des Dropdown-Bedienfelds kann nicht über CSS gesteuert werden; die Komponente ihr Layout programmgesteuert verwaltet.

Beispiel: Richten Sie ein Dropdown-Bedienfeld ein, das einen halbtransparenten schwarzen Hintergrund, einen Rand von 5 Pixeln um den Inhalt und einen Schlagschatten hat:

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

Das Erscheinungsbild der einzelnen Elemente wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**CSS-Eigenschaften des Elements**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Elements. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Interne Auffüllung. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Dropdown-Listen unterstützen die Attributauswahl `state`, mit der verschiedene Skins auf den Status &quot;Cursor darüber&quot;und &quot;Ausgewählte Elemente&quot;angewendet werden können.

Beispiel: Richten Sie ein Dropdown-Element mit einer Helvetica 14 Pixel und einer Höhe von 19 Pixel ein. Ein Element hat einen dunkelgrauen Hintergrund beim Bewegen der Maus und einen hellgrauen Hintergrund, wenn ausgewählt:

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

Ein Element, das den Seitenindex anzeigt, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**CSS-Eigenschaften des Seitenindexes**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width  </span> </p> </td> 
   <td colname="col2"> <p> Mindestelementbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width  </span> </p> </td> 
   <td colname="col2"> <p> Maximale Elementbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right  </span> </p> </td> 
   <td colname="col2"> <p> Abstand zwischen dem Seitenindex und der Seitenbeschriftung. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Es ist möglich, den Seitenindex vollständig auszublenden, indem `display:none` für die CSS-Klasse `s7index` eingestellt wird.

Beispiel 1: Richten Sie einen Seitenindex mit einer Mindestbreite von 40 Pixel, einer maximalen Breite von 70 Pixel und einem Rand von 5 Pixel auf der rechten Seite ein:

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

Die Seitenbeschriftung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**CSS-Eigenschaften der Seitenbeschriftung**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width  </span> </p> </td> 
   <td colname="col2"> <p> Mindestelementbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width  </span> </p> </td> 
   <td colname="col2"> <p> Maximale Elementbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie einen Seitenindex mit einer Mindestbreite von 40 Pixel und einer maximalen Breite von 240 Pixel ein:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Wenn mehr Elemente vorhanden sind, als vertikal in das Dropdown-Feld passen können und das System ein Desktop ist, rendert die Komponente eine vertikale Bildlaufleiste auf der rechten Seite des Bedienfelds. Das Erscheinungsbild des Bildlaufleistenbereichs wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Bildlaufleiste wird vom oberen Rand des Bedienfeldbereichs versetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Bildlaufleiste wird vom unteren Rand des Bedienfeldbereichs versetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Die horizontale Bildlaufleiste wird vom rechten Rand des Bedienfeldbereichs versetzt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie eine Bildlaufleiste ein, die 28 Pixel breit ist und keinen Rand für den oberen, rechten oder unteren Bereich des Bedienfelds hat:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

Die Bildlaufleistenspur ist der Bereich zwischen den Schaltflächen für den oberen und unteren Bildlauf. Die Komponente legt automatisch die Position und Höhe der Leiste fest. Die Spur wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**CSS-Eigenschaften der Bildlaufspur**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Die Spurbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Trackhintergrundfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie eine Bildlaufleistenspur ein, die 28 Pixel breit und einen halbtransparenten grauen Hintergrund hat:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Der Bildlaufleistenminiaturbereich bewegt sich vertikal innerhalb des Bildlaufspurbereichs. Seine vertikale Position wird durch die Komponentenlogik gesteuert. Die Höhe des Thumbs ändert sich jedoch nicht dynamisch je nach Inhaltsmenge. Sie können die Thumb-Höhe und andere Aspekte mit der folgenden CSS-Klassenauswahl konfigurieren:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Die Daumenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Die Daumenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top  </span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Umrandung zwischen der Oberkante der Leiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom  </span> </p> </td> 
   <td colname="col2"> <p>Die vertikale Umrandung zwischen dem unteren Ende der Leiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt die Attributauswahl `state`, die verwendet werden kann, um verschiedene Skins auf die Miniaturzustände `up`, `down`, `over` und `disabled` anzuwenden.

Beispiel: Richten Sie ein Bildlauffeld ein, das 28 x 45 Pixel groß ist, oben und unten 10 Pixel breit ist und für jeden Status ein anderes Bildmaterial enthält:

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

Das Erscheinungsbild der Schaltflächen für den oberen und unteren Bildlauf wird mithilfe der folgenden CSS-Klassenselektoren gesteuert:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Die Bildlaufschaltflächen können nicht mit den Eigenschaften CSS `top`, `left`, `bottom` und `right` positioniert werden. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der Schaltfläche &quot;Nach oben&quot;und &quot;Nach unten&quot;**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Die Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Die Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Button unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf die Schaltflächenzustände `up`, `down`, `over` und `disabled` angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Richten Sie Bildlaufschaltflächen ein, die 28 x 32 Pixel groß sind und für jeden Status ein anderes Bildmaterial haben:

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

