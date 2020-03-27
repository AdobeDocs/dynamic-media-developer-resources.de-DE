---
description: Durch Klicken oder Tippen auf diese Schaltfläche gelangen Sie zur vorherigen Seite im Katalog. Diese Schaltfläche wird in der Hauptsteuerungsleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Bildschirmgröße zu speichern. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
seo-description: Durch Klicken oder Tippen auf diese Schaltfläche gelangen Sie zur vorherigen Seite im Katalog. Diese Schaltfläche wird in der Hauptsteuerungsleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Bildschirmgröße zu speichern. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
seo-title: Schaltfläche "Vorherige Seite"
solution: Experience Manager
title: Schaltfläche "Vorherige Seite"
topic: Dynamic media
uuid: 6ba16329-ce24-4a06-970e-cfcd35a8b2f0
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Schaltfläche &quot;Vorherige Seite&quot;{#previous-page-button}

Durch Klicken oder Tippen auf diese Schaltfläche gelangen Sie zur vorherigen Seite im Katalog. Diese Schaltfläche wird in der Hauptsteuerungsleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Bildschirmgröße zu speichern. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton`

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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) der Benutzeroberfläche.

Beispiel: Um eine Schaltfläche für eine vorherige Seite einzurichten, die 28 x 28 Pixel groß ist, 4 Pixel vom unteren Rand und 250 Pixel vom rechten Rand der Hauptsteuerungsleiste positioniert ist und ein anderes Bild für jeden der vier verschiedenen Schaltflächenzustände anzeigt.

```
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton { 
bottom:4px; 
left:250px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_disabled.png); 
}
```

