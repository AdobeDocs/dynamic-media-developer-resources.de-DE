---
description: Durch Klicken oder Tippen auf diese Schaltfläche wird ein Bild in der Ansicht vergrößert. Diese Schaltfläche wird in der Hauptsteuerungsleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Bildschirmgröße zu speichern. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
solution: Experience Manager
title: Schaltfläche "Vergrößern"
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 2%

---


# Einzoomen-Schaltfläche{#zoom-in-button}

Durch Klicken oder Tippen auf diese Schaltfläche wird ein Bild in der Ansicht vergrößert. Diese Schaltfläche wird in der Hauptsteuerungsleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Bildschirmgröße zu speichern. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7zoominbutton`

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
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Um eine Zoomschaltfläche einzurichten, die 28 x 28 Pixel groß ist, 4 Pixel von unten und 103 Pixel von der rechten Kante der Hauptsteuerungsleiste positioniert ist und für jeden der vier verschiedenen Schaltflächenzustände ein anderes Bild anzeigt.

```
.s7ecatalogsearchviewer .s7zoominbutton { 
bottom:4px; 
right:103px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='up'] { 
background-image:url(images/v2/ZoomInButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='disabled'] { 
background-image:url(images/v2/ZoomInButton_dark_disabled.png); 
}
```

