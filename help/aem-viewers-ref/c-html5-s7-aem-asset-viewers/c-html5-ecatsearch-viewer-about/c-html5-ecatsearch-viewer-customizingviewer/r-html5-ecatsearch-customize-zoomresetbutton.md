---
title: Zurücksetzen-Schaltfläche für Zoom
description: Durch Klicken auf diese Schaltfläche wird ein Bild in der Hauptansicht zurückgesetzt. Diese Schaltfläche wird auf Desktop-Systemen und Tablets in der Hauptsteuerleiste angezeigt. Auf Mobiltelefonen wird diese Schaltfläche in der unteren Mitte über dem Bild angezeigt. Sie wird jedoch nicht angezeigt, wenn sich das Bild im zurückgesetzten Zustand befindet. Sie können diese Schaltfläche mithilfe von CSS skalieren, anpassen und positionieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d5aa9e9d-4d7e-428c-a43f-d2b4c9e59777
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Zurücksetzen-Schaltfläche für Zoom{#zoom-reset-button}

Durch Klicken auf diese Schaltfläche wird ein Bild in der Hauptansicht zurückgesetzt. Diese Schaltfläche wird auf Desktop-Systemen und Tablets in der Hauptsteuerleiste angezeigt. Auf Mobiltelefonen wird diese Schaltfläche in der unteren Mitte über dem Bild angezeigt. Sie wird jedoch nicht angezeigt, wenn sich das Bild im zurückgesetzten Zustand befindet. Sie können diese Schaltfläche mithilfe von CSS skalieren, anpassen und positionieren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogsearchviewer .s7zoomresetbutton`

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
   <td colname="col2"> <p>Position am oberen Rand der Hauptsteuerleiste (auf Desktops und Tablets) oder des Viewers (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Position am rechten Rand der Hauptsteuerleiste (auf Desktops und Tablets) oder des Viewers (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand der Hauptsteuerleiste (auf Desktops und Tablets) oder des Viewers (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Position am unteren Rand der Hauptsteuerleiste (auf Desktops und Tablets) oder des Viewers (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: So richten Sie eine Zurücksetzen-Schaltfläche für den Zoom ein, die 28 x 28 Pixel groß ist und (auf dem Desktop) 4 Pixel vom unteren Rand und 47 Pixel vom rechten Rand der Hauptsteuerleiste entfernt positioniert ist. Schließlich zeigt für jeden der vier verschiedenen Schaltflächenzustände ein eigenes Bild an.

```
.s7ecatalogsearchviewer .s7zoomresetbutton { 
bottom:4px; 
right:47px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='up'] { 
background-image:url(images/v2/ZoomResetButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='over'] {  
background-image:url(images/v2/ZoomResettButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='down'] {  
background-image:url(images/v2/ZoomResetButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='disabled'] { 
background-image:url(images/v2/ZoomResetButton_dark_disabled.png); 
}
```
