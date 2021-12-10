---
title: Hauptsteuerleiste
description: Die Hauptsteuerleiste ist der rechteckige Bereich auf Desktop-Systemen und Tablets, der alle Steuerelemente der Benutzeroberfläche (mit Ausnahme der Schaltflächen "Große Seite") enthält, die für den eCatalog Search-Viewer verfügbar sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cee6a4d4-4099-4bc8-9d67-00a1e963a139
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 1%

---

# Hauptsteuerleiste{#main-control-bar}

Die Hauptsteuerleiste ist der rechteckige Bereich auf Desktop-Systemen und Tablets, der alle Steuerelemente der Benutzeroberfläche (mit Ausnahme der Schaltflächen &quot;Große Seite&quot;) enthält, die für den eCatalog Search-Viewer verfügbar sind.

Auf Mobiltelefonen werden weiterhin die Schaltflächen Miniaturansichten, Inhaltsverzeichnis, Download, Drucken, Favoriten, Social-Freigabe, Vollbild und Schließen angezeigt. Die Schaltflächen &quot;Erste Seite&quot;und &quot;Letzte Seite&quot;und &quot;Seitenanzeige&quot;werden jedoch aus der Hauptsteuerleiste entfernt und stattdessen der sekundären Steuerleiste hinzugefügt. Standardmäßig wird die Hauptsteuerleiste im Viewer-Bereich auf Desktop-Systemen und Mobiltelefonen oben angezeigt und auf Tablets an den unteren Rand des Viewer-Bereichs verschoben. Es benötigt immer die gesamte verfügbare Viewer-Breite. Es ist möglich, die Farbe, Höhe und vertikale Position im CSS relativ zum Viewer-Container zu ändern.

Das Erscheinungsbild der Hauptsteuerleiste wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7controlbar`

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der Hauptsteuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - um eine graue Hauptkontrollleiste einzurichten, die 36 Pixel groß ist und sich oben im Viewer-Container befindet.

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

Die Hauptsteuerleiste unterstützt eine optionale Bildlauffunktion. Sie wird aktiviert, wenn die Viewer-Breite zu klein ist und nicht genügend Platz für alle Schaltflächen in der Steuerleiste vorhanden ist. In diesem Fall wird rechts in der Steuerleiste eine Zwei-Status-Pfeilschaltfläche angezeigt. Durch Klicken oder Tippen auf diese Schaltfläche werden je nach Status der Bildlaufschaltfläche alle Elemente der Kontrollleiste nach links oder rechts gescrollt. Das primäre Anwendungsbeispiel für diese Funktion sind Mobilgeräte mit kleinen Bildschirmen im Hochformat.

Die Bildlauffunktion ist für die Hauptsteuerleiste aktiviert und für die sekundäre Steuerleiste deaktiviert. Die Funktion wird mit der folgenden CSS-Klassenauswahl aktiviert und deaktiviert:

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

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
   <td colname="col2"> <p>Wenn auf <span class="codeph"> statisch </span> die Bildlauffunktion deaktiviert ist. </p> <p>Legen Sie diese Eigenschaft auf <span class="codeph"> absolute </span> , um die Bildlauffunktion zu aktivieren. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Bildlaufschaltfläche wird einem speziellen Container-Element hinzugefügt, das die Schaltfläche richtig positioniert. Damit können Sie den Bereich um die Schaltfläche anders gestalten als den Rest des Hintergrunds der Kontrollleiste, falls die Höhe der Bildlaufschaltfläche kleiner als die Höhe der Kontrollleiste ist.

Das Erscheinungsbild dieses Scroll-Schaltflächen-Containers wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Container-Hintergrundfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können die Bildlaufschaltfläche selbst über CSS anpassen und anordnen.

Das Erscheinungsbild dieser Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` und `selected` -Attributselektoren, die verwendet werden können, um verschiedene Skins auf unterschiedliche Schaltflächenzustände anzuwenden. Insbesondere `state="selected"` entspricht dem anfänglichen Status der Bildlaufschaltfläche , wenn der Inhalt der Kontrollleiste nach links verschoben werden kann. Die `state="default"` entspricht dem Status, wenn der Inhalt vollständig nach links gescrollt wird und die Bildlaufschaltfläche darauf hinweist, dass er wieder in den ursprünglichen Zustand versetzt wird.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

**Beispiel** - So aktivieren Sie die Bildlauffunktion in der Hauptsteuerleiste für Mobiltelefone. Richten Sie eine Bildlaufschaltfläche von 64 x 64 Pixel ein, die für jeden der vier Schaltflächenstatus ein anderes Bild anzeigt, wenn diese ausgewählt sind oder nicht:

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
