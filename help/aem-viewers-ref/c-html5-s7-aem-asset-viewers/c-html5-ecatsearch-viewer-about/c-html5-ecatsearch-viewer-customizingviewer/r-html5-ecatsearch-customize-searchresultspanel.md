---
title: Suchergebnisbereich
description: Das Suchergebnisbedienfeld besteht aus dem Sucheingabefeld oben und dem Hauptbereich, in dem Informationsmeldungen oder Suchergebnisse angezeigt werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# Suchergebnisbereich{#search-results-panel}

Das Suchergebnisbedienfeld besteht aus dem Sucheingabefeld oben und dem Hauptbereich, in dem Informationsmeldungen oder Suchergebnisse angezeigt werden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Wenn das Bedienfeld aktiv ist, wird die Viewer-Benutzeroberfläche mit einer halbtransparenten Füllung abgedeckt. Die Farbe und Deckkraft dieser Füllung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Farbe der Überlagerung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft </span> </p> </td> 
   <td colname="col2"> <p>Deckkraft der Farbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Suchergebnisbedienfeld belegt immer die gesamte verfügbare Viewer-Höhe. Sie können jedoch die Breite konfigurieren. Sie können die Breite auf einen absoluten Pixelwert einstellen, der eine Standardeinstellung für mittlere und große Breakpoints ist. Alternativ können Sie die Breite auf 100 % festlegen, damit der Suchergebnisbereich den gesamten Viewer-Bereich einnimmt. Die Bereichsbreite wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**CSS-Eigenschaft des Suchergebnisspeicherplatzes**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breite des Suchergebnisbereichs. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um ein Suchergebnisbedienfeld mit einer Breite von 250 Pixel für große und mittelgroße Breakpoints einzurichten, verwenden Sie ein Bedienfeld mit voller Größe für einen kleinen Breakpoint:

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

Oben im Suchergebnisbereich befindet sich das Sucheingabefeld. Der Abstand auf den Seiten des Eingabefelds wird durch die folgende CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**CSS-Eigenschaften des Sucheingabecontainers**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p> Auffüllung um das Eingabefeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Eingabefeld für die Suche wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**CSS-Eigenschaften des Sucheingabefelds**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Sucheingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p> Der innere Abstand zwischen dem Eingabefeldbereich und dem Eingabetext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand des Sucheingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Rand des Sucheingabefelds </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Größe der Textschriftart. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Sucheingabefelds mit 0 Pixel Höhe und 14 Pixel Textschrift:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

Die Suchschaltfläche links neben dem Sucheingabefeld in Form des standardmäßig &quot;Look-glass&quot;wird durch den folgenden CSS-Klassenselektor gesteuert:

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**CSS-Eigenschaften der Sucheingabeschaltfläche**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Sucheingabeschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Sucheingabeschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Die URL zum "Look-glass"-Symbolbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-size </span> </p> </td> 
   <td colname="col2"> <p>Die Größe des Symbols "Aussehendes Glas". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand der Sucheingabeschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Rand der Sucheingabeschaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie eine Suchschaltfläche mit einem 26 x 26 Pixel &quot;Look-glass&quot;-Symbol ein; eine Größe von 30 Pixel mit einem 1 Pixel langen Rahmen:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

Im Suchergebnisbereich wird möglicherweise eine Textaufforderung angezeigt, wenn die Funktion zum ersten Mal aufgerufen wird. Außerdem wird eine Meldung angezeigt, wenn die Suche eines Benutzers keine Ergebnisse zurückgegeben hat. In allen Fällen wird Text im Hauptteil des Bedienfelds für Suchergebnisse angezeigt und über die folgende CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**CSS-Eigenschaften der Suchinformationen**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Name der Textschriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Dieser Textbereich unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Stile auf verschiedene Textnachrichten angewendet werden können. Insbesondere entspricht `state='prompt'` der Textaufforderung, die angezeigt wird, wenn das Bedienfeld zum ersten Mal aufgerufen wird. Der `state='results'` entspricht dem Text mit Informationen zu Suchtreffern. Und schließlich entspricht der `state='no_results'` dem Text, der angezeigt wird, wenn die Suchabfrage keine Ergebnisse zurückgegeben hat.

Der Nachrichtentext kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Beispiel - So richten Sie ein Textfeld ein, das eine graue 18-Pixel-Schriftart verwendet:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

Suchergebnisse werden als einzelne Spalte oder einzelne Zeile von Miniaturansichten für Seiten mit Suchtreffern gerendert. Der Abstand zwischen den Miniaturansichten der Suchergebnisse wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**CSS-Eigenschaften der Miniaturansichten**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Die Größe des vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand der Miniaturansichten entspricht der Summe der oberen und unteren Ränder, die für <span class="codeph"> .s7thumbcell </span> festgelegt wurden. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie einen Abstand von zehn Pixeln ein:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild einzelner Miniaturansichten wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**CSS-Eigenschaften der Miniaturansicht**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
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

Beispiel: Um Miniaturansichten mit 215 x 129 Pixel einzurichten, weisen einen hellgrauen Standardrahmen und einen dunkelgrauen ausgewählten Rahmen auf:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

Das Erscheinungsbild der Miniaturansichtsbeschriftung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**CSS-Eigenschaften des Titels**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Name der Textschriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Größe der Textschriftart. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie Beschriftungen ein, die 12 Pixel, grau, Helvetica®-Schriftart verwenden:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

Auf Systemen, die die Mauseingabe verwenden, werden unten im Suchergebnisbereich zwei Bildlauftasten angezeigt, um durch die Suchergebnisse zu blättern. Das Erscheinungsbild der Bildlaufschaltflächen nach oben und unten wird mithilfe der folgenden CSS-Klassenselektoren gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Es ist nicht möglich, Bildlaufschaltflächen mithilfe der CSS-Eigenschaften oben, links, unten und rechts zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der Scroll-Schaltflächen nach oben und unten**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
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
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf die Schaltflächenzustände `"up"`, `"down"`, `"over"` und `"disabled"` angewendet werden können.

Die QuickInfos für Schaltflächen können lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Beispiel - So richten Sie eine Bildlaufschaltfläche ein, die 125 x 35 Pixel groß ist und für jeden Status unterschiedliche Grafiken aufweist:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```
