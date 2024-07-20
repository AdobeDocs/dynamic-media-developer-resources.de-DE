---
title: Schaltfläche "Große vorherige Seite"
description: Wenn Sie diese Schaltfläche auswählen, wird der Benutzer zur vorherigen Seite im Katalog weitergeleitet. Diese Schaltfläche wird in der Hauptsteuerleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 39bf9f23-1950-4920-877e-b07e8df18bdc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Schaltfläche &quot;Große vorherige Seite&quot;{#large-previous-page-button}

Wenn Sie diese Schaltfläche auswählen, wird der Benutzer zur vorherigen Seite im Katalog weitergeleitet. Diese Schaltfläche wird in der Hauptsteuerleiste angezeigt. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton`

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
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Beispiel: Zum Einrichten einer großen Schaltfläche für die vorherige Seite, die 56 x 56 Pixel groß ist, vertikal zentriert und mit dem linken Viewer-Rahmen verankert ist und für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild anzeigt.

```
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton { 
bottom:50%; 
margin-bottom:-28px; 
left:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/LeftButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/LeftButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/LeftButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/LeftButton_dark_disabled.png); 
}
```
