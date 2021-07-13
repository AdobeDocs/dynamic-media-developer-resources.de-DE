---
description: Durch Klicken oder Tippen auf diese Schaltfläche gelangen Benutzer zur nächsten Seite im Katalog. Diese Schaltfläche wird in der Hauptsteuerleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
solution: Experience Manager
title: Schaltfläche "Weiter"
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5d1bee54-ec16-40fe-9653-ba7e02774cbb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 2%

---

# Schaltfläche &quot;Weiter&quot;{#large-next-page-button}

Durch Klicken oder Tippen auf diese Schaltfläche gelangen Benutzer zur nächsten Seite im Katalog. Diese Schaltfläche wird in der Hauptsteuerleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton`

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Um eine große Schaltfläche für die nächste Seite einzurichten, die 56 x 56 Pixel groß ist, vertikal zentriert ist und mit dem rechten Viewer-Rahmen verankert ist, und für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild anzuzeigen.

```
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton { 
bottom:50%; 
margin-bottom:-28px; 
right:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/RightButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/RightButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/RightButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7ecatrightbutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/RightButton_dark_disabled.png); 
}
```
