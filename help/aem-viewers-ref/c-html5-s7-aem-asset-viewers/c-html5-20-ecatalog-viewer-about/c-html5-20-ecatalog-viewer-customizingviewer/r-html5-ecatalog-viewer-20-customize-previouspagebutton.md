---
title: Schaltfläche "Vorherige Seite"
description: Wenn Sie auf diese Schaltfläche klicken oder tippen, wird der Benutzer zur vorherigen Seite im Katalog weitergeleitet. Diese Schaltfläche wird in der Hauptsteuerleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cc0e8c18-f9c1-4451-9fbe-3b082f78a7ec
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 2%

---

# Schaltfläche &quot;Vorherige Seite&quot;{#previous-page-button}

Wenn Sie auf diese Schaltfläche klicken oder tippen, wird der Benutzer zur vorherigen Seite im Katalog weitergeleitet. Diese Schaltfläche wird in der Hauptsteuerleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand der Hauptkontrollleiste, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand der Hauptkontrollleiste, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand der Hauptkontrollleiste, einschließlich des Abstands. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position vom unteren Rand der Hauptkontrollleiste, einschließlich Abstand. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: Um eine Schaltfläche für die vorherige Seite einzurichten, die 28 x 28 Pixel groß ist und 4 Pixel vom unteren Rand und 250 Pixel vom rechten Rand der Hauptsteuerungsleiste entfernt ist. Und schließlich zeigt ein anderes Bild für jeden der vier verschiedenen Schaltflächenstatus an.

```
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton { 
bottom:4px; 
left:250px; 
width:32px; 
height:32px; 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_up.png); 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_over.png); 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_down.png); 
} 
.s7ecatalogviewer .s7toolbarleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_disabled.png); 
}
```
