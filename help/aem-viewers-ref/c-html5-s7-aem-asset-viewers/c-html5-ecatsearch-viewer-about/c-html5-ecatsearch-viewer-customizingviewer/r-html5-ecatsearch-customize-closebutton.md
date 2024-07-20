---
title: Schaltfläche schließen
description: Durch Klicken oder Tippen auf diese Schaltfläche wird die übergeordnete Webseite geschlossen. Diese Schaltfläche wird nur angezeigt, wenn der Parameter closeButton auf 1 gesetzt ist. Diese Schaltfläche ist auf Desktop-Systemen nicht verfügbar. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 8dee7c56-ed60-44e5-a5c9-f404df03861e
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Schaltfläche schließen{#close-button}

Wenn Sie diese Schaltfläche auswählen oder tippen, wird die übergeordnete Webseite geschlossen. Diese Schaltfläche wird nur angezeigt, wenn der Parameter closeButton auf 1 gesetzt ist. Diese Schaltfläche ist auf Desktop-Systemen nicht verfügbar. Mithilfe von CSS können Sie diese Schaltfläche vergrößern, verkleinern und positionieren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7closebutton`

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
>Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, mit der Sie verschiedene Skins auf unterschiedliche Schaltflächenzustände anwenden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Beispiel: Zum Einrichten einer Schließen -Schaltfläche mit einer Größe von 56 x 56 Pixel und einer Positionierung von 4 Pixel vom oberen und rechten Rand der Hauptsteuerleiste. Und schließlich zeigt ein anderes Bild für jeden der vier verschiedenen Schaltflächenstatus an.

```
.s7ecatalogsearchviewer .s7closebutton { 
top:4px; 
right:4px; 
width:56px; 
height:56px; 
} 
.s7ecatalogsearchviewer .s7closebutton [state='up'] { 
background-image:url(images/v2/CloseButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7closebutton [state='over'] {  
background-image:url(images/v2/CloseButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7closebutton [state='down'] {  
background-image:url(images/v2/CloseButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7closebutton [state='disabled'] { 
background-image:url(images/v2/CloseButton_dark_disabled.png); 
}
```
