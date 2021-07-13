---
description: Das Inhaltsverzeichnis ist eine Schaltfläche in der Hauptsteuerleiste. Wenn diese Option aktiviert ist, wird ein Dropdown-Fenster mit einer Liste von Seitenindizes und -beschriftungen angezeigt.
solution: Experience Manager
title: Inhaltsverzeichnis
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: bc597c68-b86c-4577-9d24-6999eccada78
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 1%

---

# Inhaltsverzeichnis{#table-of-contents}

Das Inhaltsverzeichnis ist eine Schaltfläche in der Hauptsteuerleiste. Wenn diese Option aktiviert ist, wird ein Dropdown-Fenster mit einer Liste von Seitenindizes und -beschriftungen angezeigt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Basierend auf der Konfiguration kann die Liste alle Seiten enthalten, die im Katalog vorhanden sind, oder nur die Seiten, für die explizite Beschriftungen definiert sind. Auf Desktop-Systemen wird rechts eine Bildlaufleiste angezeigt, wenn die Liste länger als die verfügbare Bildschirmgröße ist.

Die Position und Größe der Inhaltsverzeichnisschaltfläche in der Viewer-Benutzeroberfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7tableofcontents
```

**CSS-Eigenschaften des Inhaltsverzeichnisses**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz am oberen Rand der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Der Abstand zur nächsten Schaltfläche auf der linken Seite oder zur linken Seite der Steuerleiste, wenn dies die erste Schaltfläche in einer Zeile ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Inhaltsverzeichnisschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Die Höhe der Inhaltsverzeichnisschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Richten Sie eine Inhaltsverzeichnisschaltfläche ein, die 4 Pixel vom unteren Rand und 43 Pixel vom linken Rand der Hauptsteuerungsleiste entfernt angeordnet ist. ist 28 x 28 Pixel groß und für jeden der vier Schaltflächenstatus wird ein anderes Bild angezeigt:

```
.s7ecatalogsearchviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

Das Erscheinungsbild des Dropdown-Bedienfelds wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel
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
   <td colname="col2"> <p> Interner Versatz zwischen den Bereichsgrenzen und dem Inhalt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-Shadow  </span> </p> </td> 
   <td colname="col2"> <p> Schlagschatten um das Bedienfeld herum. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Die Größe oder Position des Dropdown-Bedienfelds kann nicht über CSS gesteuert werden. die Komponente ihr Layout programmgesteuert verwaltet.

Beispiel: Einrichten eines Dropdown-Bedienfelds mit einem halbtransparenten schwarzen Hintergrund, einer 5-Pixel-Ränder um den Inhalt und einem Schlagschatten:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

Das Erscheinungsbild der einzelnen Elemente wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item
```

**CSS-Eigenschaften des Elements**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie  </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Elements. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Interner Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Das Dropdown-Listenelement unterstützt den Attributselektor `state`, der verwendet werden kann, um verschiedene Skins auf den Mauszeiger und die ausgewählten Elementstatus anzuwenden.

Beispiel: Richten Sie ein Dropdown-Element mit einer Helvetica-Schrift mit 14 Pixel und einer Höhe von 19 Pixel ein. Ein Element hat beim Bewegen des Mauszeigers einen dunkelgrauen Hintergrund und bei Auswahl einen hellgrauen Hintergrund:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Ein Element, das den Seitenindex anzeigt, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index
```

**CSS-Eigenschaften des Seitenindex**

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
>Es ist möglich, den Seitenindex vollständig auszublenden, indem Sie `display:none` für die CSS-Klasse `s7index` festlegen.

Beispiel 1: Richten Sie einen Seitenindex mit einer Mindestbreite von 40 Pixel, einer maximalen Breite von 70 Pixel und einem Rand von 5 Pixel auf der rechten Seite ein:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Beispiel 2 - Seiten-Index ausblenden:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

Die Seitenbeschriftung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label
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
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Wenn mehr Elemente vorhanden sind, die im Dropdown-Bedienfeld vertikal angepasst werden können, und das System ein Desktop ist, rendert die Komponente eine vertikale Bildlaufleiste auf der rechten Seite des Bedienfelds. Das Erscheinungsbild des Bildlaufleistenbereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar
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
   <td colname="col2"> <p> Der Versatz der vertikalen Bildlaufleiste am oberen Rand des Bedienfeldbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz der vertikalen Bildlaufleiste am unteren Rand des Bedienfeldbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Der horizontale Versatz der Bildlaufleiste vom rechten Rand des Bedienfeldbereichs. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie eine Bildlaufleiste ein, die 28 Pixel breit ist und keinen Rand für den oberen, rechten oder unteren Bereich des Bedienfelds hat:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

Die Bildlaufleisten-Spur ist der Bereich zwischen den oberen und unteren Bildlauftasten. Die Komponente legt automatisch die Position und Höhe der Spur fest. Die Verfolgung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
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
   <td colname="col2"> <p>Die Hintergrundfarbe der Verfolgung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie eine Bildlaufleiste ein, die 28 Pixel breit ist und einen halbtransparenten grauen Hintergrund hat:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Der Bildlaufleisten-Daumen bewegt sich innerhalb des Bildlaufverfolgungsbereichs vertikal. Seine vertikale Position wird durch die Komponentenlogik gesteuert. Die Thumb-Höhe ändert sich jedoch nicht dynamisch in Abhängigkeit von der Menge des Inhalts. Sie können die Daumenhöhe und andere Aspekte mit dem folgenden CSS-Klassenselektor konfigurieren:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
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
   <td colname="col1"> <p> <span class="codeph"> Auffüllung  </span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Abstand zwischen dem oberen Ende des Gleises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom  </span> </p> </td> 
   <td colname="col2"> <p>Der vertikale Abstand zwischen dem unteren Ende des Gleises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt den Attributselektor `state`, der verwendet werden kann, um verschiedene Skins auf die Faustregeln `up`, `down`, `over` und `disabled` anzuwenden.

Beispiel: Richten Sie einen Bildlaufleisten-Daumen ein, der 28 x 45 Pixel groß ist, oben und unten 10 Pixel Ränder aufweist und für jeden Status unterschiedliche Grafiken aufweist:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

Das Erscheinungsbild der oberen und unteren Bildlaufschaltflächen wird mithilfe der folgenden CSS-Klassenselektoren gesteuert:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Es ist nicht möglich, die Bildlauftasten mithilfe der CSS-Eigenschaften `top`, `left`, `bottom` und `right` zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der Schaltfläche &quot;Nach oben scrollen und nach unten scrollen&quot;**

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
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Button unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf die Schaltflächenzustände `up`, `down`, `over` und `disabled` angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Richten Sie Bildlaufschaltflächen ein, die 28 x 32 Pixel groß sind und für jeden Status unterschiedliche Grafiken aufweisen:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
