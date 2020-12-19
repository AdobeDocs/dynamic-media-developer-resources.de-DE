---
description: Die Hauptsteuerungsleiste ist der rechteckige Bereich auf Desktop-Systemen und Tablets, der alle Steuerelemente der Benutzeroberfläche (mit Ausnahme der Schaltflächen "Große Seite") enthält, die für den E-Katalog-Viewer verfügbar sind.
seo-description: Die Hauptsteuerungsleiste ist der rechteckige Bereich auf Desktop-Systemen und Tablets, der alle Steuerelemente der Benutzeroberfläche (mit Ausnahme der Schaltflächen "Große Seite") enthält, die für den E-Katalog-Viewer verfügbar sind.
seo-title: Hauptsteuerleiste
solution: Experience Manager
title: Hauptsteuerleiste
topic: Dynamic media
uuid: 0900f678-d7ec-4653-bc8a-21b8da7d5044
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 1%

---


# Hauptsteuerleiste{#main-control-bar}

Die Hauptsteuerungsleiste ist der rechteckige Bereich auf Desktop-Systemen und Tablets, der alle Steuerelemente der Benutzeroberfläche (mit Ausnahme der Schaltflächen &quot;Große Seite&quot;) enthält, die für den E-Katalog-Viewer verfügbar sind.

Auf Mobiltelefonen werden weiterhin Miniaturansichten, Inhaltsverzeichnisse, Download-, Druck-, Favoriten-, Social Sharing-, Vollbild- und Schließen-Schaltflächen gespeichert. Die Schaltflächen &quot;Erste Seite&quot;und &quot;Letzte Seite&quot;und &quot;Seitenanzeige&quot;werden jedoch aus der Hauptsteuerleiste entfernt und stattdessen der sekundären Steuerleiste hinzugefügt. Standardmäßig wird die Hauptsteuerungsleiste auf Desktop-Systemen und Mobiltelefonen oben im Viewer-Bereich angezeigt und auf Tablets nach unten verschoben. Es nimmt immer die gesamte verfügbare Viewer-Breite in Anspruch. Sie können die Farbe, Höhe und vertikale Position im CSS relativ zum Viewer-Container ändern.

Das Erscheinungsbild der Hauptsteuerleiste wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position oben im Viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position am unteren Rand des Viewers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Hauptsteuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der Hauptsteuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** : Zur Einrichtung einer grauen Hauptkontrollleiste, die 36 Pixel hoch und oben im Viewer-Container positioniert ist.

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

Die Hauptsteuerungsleiste unterstützt eine optionale Bildlauffunktion. Es wird aktiviert, wenn die Viewer-Breite zu klein ist und nicht genügend Platz für alle Schaltflächen in der Steuerungsleiste vorhanden ist. In diesem Fall wird rechts in der Steuerungsleiste eine Pfeiltaste mit zwei Status angezeigt. Wenn Sie auf diese Schaltfläche klicken oder darauf tippen, werden je nach Status der Bildlaufschaltfläche alle Elemente der Steuerleiste nach links oder rechts durchlaufen. Der primäre Anwendungsfall für diese Funktion sind Mobilgeräte mit kleinen Bildschirmen im Hochformat.

Die Bildlauffunktion ist für die Hauptsteuerleiste aktiviert und für die sekundäre Steuerleiste deaktiviert. Die Funktion ist mithilfe der folgenden CSS-Klassenauswahl aktiviert und deaktiviert:

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
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p>Bei Festlegung auf <span class="codeph"> static </span> ist die Bildlauffunktion deaktiviert. </p> <p>Legen Sie diese Eigenschaft auf <span class="codeph"> absolut </span> fest, um die Bildlauffunktion zu aktivieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Bildlauftaste wird einem speziellen Container hinzugefügt, der die Schaltfläche korrekt positioniert und es Ihnen ermöglicht, den Schaltflächenbereich anders zu gestalten als den übrigen Hintergrund der Steuerleiste, falls die Höhe der Bildlauftaste kleiner als die Höhe der Steuerleiste ist.

Das Erscheinungsbild dieses Containers für die Bildlaufschaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Normalerweise sollte gleich oder größer als die Breite der Bildlaufschaltfläche selbst sein. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Containers. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können die Bildlauftaste per CSS verkleinern und per Skin bearbeiten.

Das Erscheinungsbild dieser Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributselektoren `state` und `selected`, mit denen verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können. Insbesondere entspricht `state="selected"` dem Anfangszustand der Bildlaufschaltfläche, wenn der Inhalt der Steuerleiste nach links durchlaufen werden kann; `state="default"` entspricht dem Status, in dem der Inhalt bis ganz nach links durchlaufen wird und die Bildlauftaste vorschlägt, ihn zum Ausgangszustand zurückzukehren.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

**Beispiel** : Um die Bildlauffunktion in der Hauptsteuerleiste für Mobiltelefone zu aktivieren und eine Bildlauftaste mit 64 x 64 Pixel einzurichten, die ein anderes Bild für jeden der vier verschiedenen Schaltflächenzustände anzeigt, wenn diese ausgewählt oder nicht ausgewählt sind:

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

