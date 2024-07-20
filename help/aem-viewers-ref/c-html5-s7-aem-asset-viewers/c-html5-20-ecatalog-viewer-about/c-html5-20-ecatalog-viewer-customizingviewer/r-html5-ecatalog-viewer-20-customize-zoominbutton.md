---
title: Schaltfläche "Vergrößern"
description: Durch Klicken oder Tippen auf diese Schaltfläche wird ein Bild in der Hauptansicht vergrößert. Diese Schaltfläche wird in der Hauptsteuerleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 6eda6e0f-f588-43b9-b135-3b78fc40b8b3
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---

# Schaltfläche &quot;Vergrößern&quot;{#zoom-in-button}

Durch Auswahl oder Tippen auf diese Schaltfläche wird ein Bild in der Hauptansicht vergrößert. Diese Schaltfläche wird in der Hauptsteuerleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogviewer .s7zoominbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand der Hauptkontrollleiste, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand der Hauptkontrollleiste, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
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
>Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Beispiel: Um eine Zoom-Schaltfläche einzurichten, die 28 x 28 Pixel groß ist und 4 Pixel von der unteren Seite und 103 Pixel von der rechten Kante der Hauptsteuerungsleiste positioniert ist. Und schließlich zeigt ein anderes Bild für jeden der vier verschiedenen Schaltflächenstatus an.

```
.s7ecatalogviewer .s7zoominbutton { 
bottom:4px; 
right:103px; 
width:28px; 
height:28px; 
} 
.s7ecatalogviewer .s7zoominbutton [state='up'] { 
background-image:url(images/v2/ZoomInButton_dark_up.png); 
} 
.s7ecatalogviewer .s7zoominbutton [state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png); 
} 
.s7ecatalogviewer .s7zoominbutton [state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png); 
} 
.s7ecatalogviewer .s7zoominbutton [state='disabled'] { 
background-image:url(images/v2/ZoomInButton_dark_disabled.png); 
}
```
