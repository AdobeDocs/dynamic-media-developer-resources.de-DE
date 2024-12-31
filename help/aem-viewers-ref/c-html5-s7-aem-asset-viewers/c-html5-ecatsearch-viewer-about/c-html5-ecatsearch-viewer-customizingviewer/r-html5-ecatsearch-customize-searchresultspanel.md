---
title: Suchergebnisbedienfeld
description: Das Suchergebnisbedienfeld besteht aus dem Eingabefeld für die Suche oben und dem Hauptbereich, in dem Informationsmeldungen oder Suchergebnisse angezeigt werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# Suchergebnisbedienfeld{#search-results-panel}

Das Suchergebnisbedienfeld besteht aus dem Eingabefeld für die Suche oben und dem Hauptbereich, in dem Informationsmeldungen oder Suchergebnisse angezeigt werden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Wenn das Bedienfeld aktiv ist, wird die Benutzeroberfläche des Viewers mit einer halbtransparenten Füllung abgedeckt. Die Farbe und Deckkraft dieser Füllung wird mit dem folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Farbe der Überlagerung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Deckkraft der Farbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Suchergebnisfenster nimmt immer die gesamte verfügbare Viewer-Höhe ein. Sie können jedoch die Breite konfigurieren. Sie können die Breite auf einen absoluten Pixel-Wert festlegen, bei dem es sich um eine Standardeinstellung für Breakpoints mit mittlerer und großer Größe handelt. Sie können auch die Breite auf 100 % festlegen, damit das Suchergebnisbedienfeld den gesamten Viewer-Bereich einnimmt. Die Breite des Bedienfelds wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**CSS-Eigenschaft des Suchergebnisbereichs**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Breite des Suchergebnisbereichs. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel : So richten Sie ein Suchergebnisbedienfeld mit einer Breite von 250 Pixel für große und mittelgroße Breakpoints ein und verwenden ein Bedienfeld mit voller Größe für einen kleinen Breakpoint:

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

Der obere Rand des Bedienfelds Suchergebnisse ist für das Sucheingabefeld vorgesehen. Der Abstand an den Seiten des Eingabefelds wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**CSS-Eigenschaften des Sucheingabe-Containers**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Auffüllung um das Eingabefeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Sucheingabefeld wird durch den folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> Abstand - </span> </p> </td> 
   <td colname="col2"> <p> Der innere Abstand zwischen den Eingabefeldgrenzen und dem Eingabetext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen des Sucheingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rand des Sucheingabefelds </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Größe der Textschriftart. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Sucheingabefeld mit einer Höhe von 0 Pixel und einer Textschriftart von 14 Pixel ein:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

Die Suchschaltfläche links neben dem Sucheingabefeld in Form des „Lookglass“ wird standardmäßig durch die folgende CSS-Klassenauswahl gesteuert:

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**CSS-Eigenschaften der Sucheingabe-Schaltfläche**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Eingabe-Suchschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Eingabe-Suchschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Die URL zum Bild des „Lookglass“-Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundgröße </span> </p> </td> 
   <td colname="col2"> <p>Die Größe des „Spiegel“-Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen der Eingabe-Suchschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rand der Eingabe-Suchschaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Suchschaltfläche mit einem „Look-Glass“-Symbol mit 26 x 26 Pixeln ein: 30 Pixel groß mit einem 1-Pixel-Rahmen:

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

Das Suchergebnisfenster zeigt möglicherweise eine Eingabeaufforderung in Textform an, wenn die Funktion zum ersten Mal aufgerufen wird. Außerdem wird eine Meldung angezeigt, wenn die Suche eines Benutzers keine Ergebnisse zurückgegeben hat. In allen Fällen wird Text im Hauptteil des Suchergebnisbereichs angezeigt und durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**CSS-Eigenschaften der Suchinformationen**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Name der Textschriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> für die <span class="codeph">-Ausrichtung </p> </td> 
   <td colname="col2"> <p>Horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgrad des Textes. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Dieses Textbedienfeld unterstützt die `state`-Attributauswahl, mit der Sie verschiedene Stile auf verschiedene Textnachrichten anwenden können. Insbesondere entspricht `state='prompt'` der Textaufforderung, die angezeigt wird, wenn das Bedienfeld zum ersten Mal aufgerufen wird. Die `state='results'` entspricht dem Text mit Informationen zu Suchtreffern. Und schließlich entspricht der `state='no_results'` dem Text, der angezeigt wird, wenn die Suchanfrage keine Ergebnisse zurückgegeben hat.

Der Nachrichtentext kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel - So richten Sie ein Textfeld ein, das eine graue 18-Pixel-Schriftart verwendet:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

Suchergebnisse werden für Seiten mit Suchtreffern als einzelne Spalte oder einzelne Miniaturansichtszeile gerendert. Der Abstand zwischen Suchergebnisminiaturen wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**CSS-Eigenschaften der Miniaturbilderzellen**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Größe des vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand zwischen den Miniaturen entspricht der Summe der oberen und unteren Ränder, die für <span class="codeph"> s7thumbcell-</span> festgelegt sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie einen Zehn-Pixel-Abstand ein:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild einzelner Miniaturen wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**CSS-Eigenschaften der Miniatur**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniatur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen der Miniatur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Für Miniaturen mit einer Größe von 215 x 129 Pixeln ist der Standardrahmen hellgrau und der ausgewählte Rahmen dunkelgrau:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

Das Erscheinungsbild der Miniaturbildbeschriftung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**CSS-Eigenschaften der Bezeichnung**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Name der Textschriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße des Textes. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie Beschriftungen ein, die die Schriftart 12 Pixel, Grau, Helvetica® verwenden:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

Auf Systemen, die eine Mauseingabe verwenden, werden unten im Suchergebnisbereich zwei Bildlaufschaltflächen angezeigt, mit denen Benutzer durch die Suchergebnisse scrollen können. Die Darstellung der Bildlaufschaltflächen nach oben und unten wird mit den folgenden CSS-Klassenselektoren gesteuert:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Scroll-Schaltflächen können nicht mit den CSS-Eigenschaften „oben“, „links“, „unten“ und „rechts“ positioniert werden. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der Schaltflächen Nach oben und Nach unten**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf `"up"`-, `"down"`-, `"over"`- und `"disabled"` angewendet werden können.

Die QuickInfos für die Schaltfläche können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: So richten Sie eine Scroll-Up-Schaltfläche mit einer Größe von 125 x 35 Pixel ein, die für jeden Status unterschiedliche Grafiken aufweist:

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
