---
description: Durch Klicken oder Tippen auf diese Schaltfläche wird die zugehörige Webseite geschlossen. Diese Schaltfläche wird nur angezeigt, wenn der Parameter closeButton auf 1 gesetzt ist. Diese Schaltfläche ist auf Desktop-Systemen nicht verfügbar. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
seo-description: Durch Klicken oder Tippen auf diese Schaltfläche wird die zugehörige Webseite geschlossen. Diese Schaltfläche wird nur angezeigt, wenn der Parameter closeButton auf 1 gesetzt ist. Diese Schaltfläche ist auf Desktop-Systemen nicht verfügbar. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
seo-title: Schaltfläche "Schließen"
solution: Experience Manager
title: Schaltfläche "Schließen"
topic: Dynamic media
uuid: b0de1600-6b02-4b59-aac6-ade0ec6dc087
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 2%

---


# Schließen-Schaltfläche{#close-button}

Durch Klicken oder Tippen auf diese Schaltfläche wird die zugehörige Webseite geschlossen. Diese Schaltfläche wird nur angezeigt, wenn der Parameter closeButton auf 1 gesetzt ist. Diese Schaltfläche ist auf Desktop-Systemen nicht verfügbar. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogviewer .s7closebutton`

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
   <td colname="col2"> <p>Position vom oberen Rand der Hauptsteuerleiste, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand der Hauptsteuerleiste, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand der Hauptsteuerleiste, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position vom unteren Rand der Hauptsteuerleiste, einschließlich Auffüllung. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der Sie verschiedene Skins auf verschiedene Schaltflächenzustände anwenden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Um eine Schaltfläche zum Schließen einzurichten, die 56 x 56 Pixel groß ist, 4 Pixel von der oberen und rechten Kante der Hauptsteuerleiste entfernt ist und ein anderes Bild für jeden der vier verschiedenen Schaltflächenzustände anzeigt.

```
.s7ecatalogviewer .s7closebutton { 
top:4px; 
right:4px; 
width:56px; 
height:56px; 
} 
.s7ecatalogviewer .s7closebutton [state='up'] { 
background-image:url(images/v2/CloseButton_dark_up.png); 
} 
.s7ecatalogviewer .s7closebutton [state='over'] {  
background-image:url(images/v2/CloseButton_dark_over.png); 
} 
.s7ecatalogviewer .s7closebutton [state='down'] {  
background-image:url(images/v2/CloseButton_dark_down.png); 
} 
.s7ecatalogviewer .s7closebutton [state='disabled'] { 
background-image:url(images/v2/CloseButton_dark_disabled.png); 
}
```

