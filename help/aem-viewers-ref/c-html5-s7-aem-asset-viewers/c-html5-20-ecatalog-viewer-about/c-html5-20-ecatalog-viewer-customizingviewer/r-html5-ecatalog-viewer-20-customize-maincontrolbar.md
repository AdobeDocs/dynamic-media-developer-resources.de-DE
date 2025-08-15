---
title: Hauptsteuerleiste
description: Die Hauptsteuerleiste ist der rechteckige Bereich auf Desktop-Systemen und Tablets, der alle Steuerelemente der Benutzeroberfläche (mit Ausnahme von Schaltflächen für große Seiten) enthält, die für den E-Katalog-Viewer verfügbar sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 4db16599-ede0-47ae-bb5a-840655d3620b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Hauptsteuerleiste{#main-control-bar}

Die Hauptsteuerleiste ist der rechteckige Bereich auf Desktop-Systemen und Tablets, der alle Steuerelemente der Benutzeroberfläche (mit Ausnahme von Schaltflächen für große Seiten) enthält, die für den E-Katalog-Viewer verfügbar sind.

Auf Mobiltelefonen werden weiterhin die Schaltflächen Miniaturansichten, Inhaltsverzeichnis, Herunterladen, Drucken, Favoriten, Social Share, Vollbild und Schließen gespeichert. Die Schaltflächen „Erste Seite“ und „Letzte Seite“ sowie die Seitenanzeige werden jedoch aus der Hauptsteuerleiste entfernt und stattdessen zur sekundären Steuerleiste hinzugefügt. Standardmäßig wird die Hauptsteuerleiste oben im Viewer-Bereich auf Desktop-Systemen und Mobiltelefonen angezeigt und auf Tablets an das Ende des Viewer-Bereichs verschoben. Dazu wird immer die gesamte verfügbare Viewer-Breite benötigt. Es ist möglich, die Farbe, Höhe und vertikale Position im CSS relativ zum Viewer-Container zu ändern.

Das Erscheinungsbild der Hauptsteuerleiste wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position oben im Viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Position am unteren Rand des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Hauptsteuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der Hauptsteuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Einrichten einer grauen Hauptsteuerleiste, die 36 Pixel hoch ist und sich oben im Viewer-Container befindet.

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

Die Hauptsteuerleiste unterstützt eine optionale Bildlauffunktion. Er wird aktiviert, wenn die Viewer-Breite zu klein ist und nicht genügend Platz für alle in der Steuerleiste voreingestellten Schaltflächen vorhanden ist. In diesem Fall wird rechts in der Steuerleiste eine Pfeilschaltfläche mit zwei Status angezeigt. Durch Klicken oder Tippen auf diese Schaltfläche werden alle Elemente der Steuerleiste je nach Zustand der Bildlaufschaltfläche nach links oder rechts verschoben. Der Hauptanwendungsfall für diese Funktion sind mobile Geräte mit kleinen Bildschirmen im Hochformat.

Die Bildlauffunktion ist für die Hauptsteuerleiste aktiviert und für die sekundäre Steuerleiste deaktiviert. Die Funktion wird mithilfe des folgenden CSS-Klassenselektors ein- und ausgeschaltet:

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Bei <span class="codeph"> statischen </span> ist die Bildlauffunktion deaktiviert. </p> <p>Legen Sie diese Eigenschaft auf <span class="codeph"> absolute </span> fest, um die Bildlauffunktion zu aktivieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Scroll-Schaltfläche wird einem speziellen Container-Element hinzugefügt, das die Schaltfläche ordnungsgemäß positioniert. Auf diese Weise können Sie den Bereich um die Schaltfläche anders gestalten als den Rest des Hintergrunds der Steuerleiste, falls die Höhe der Bildlaufschaltfläche kleiner als die Höhe der Steuerleiste ist.

Das Erscheinungsbild dieses Scroll-Button-Containers wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Normalerweise sollte gleich oder größer als die Breite der Bildlaufschaltfläche selbst sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Container-Hintergrundfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können die Bildlaufschaltfläche selbst mithilfe von CSS in der Größe anpassen und mit der Haut versehen.

Das Erscheinungsbild dieser Schaltfläche wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p>Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state` und `selected`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können. Insbesondere entspricht `state="selected"` dem anfänglichen Scroll-Button-Zustand, wenn es möglich ist, den Inhalt der Steuerleiste nach links zu scrollen. Das Attribut `state="default"` entspricht dem Status, wenn der Inhalt ganz nach links gescrollt wird, und die Scroll-Schaltfläche schlägt vor, ihn wieder in den ursprünglichen Status zurückzuversetzen.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

**Beispiel** - Zum Aktivieren der Bildlauffunktion in der Hauptsteuerleiste für Mobiltelefone. Richten Sie außerdem eine Bildlaufschaltfläche mit 64 x 64 Pixeln ein, die für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild anzeigt, wenn ausgewählt oder nicht ausgewählt:

```
.s7ecatalogviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
