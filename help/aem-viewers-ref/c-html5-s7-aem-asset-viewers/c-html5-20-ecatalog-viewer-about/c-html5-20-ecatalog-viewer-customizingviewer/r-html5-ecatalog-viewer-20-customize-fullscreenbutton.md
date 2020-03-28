---
description: Verursacht, dass der Viewer den Vollbildmodus aufruft oder verlässt, wenn der Benutzer darauf klickt. Diese Schaltfläche wird in der Hauptsteuerungsleiste angezeigt. Diese Schaltfläche wird nicht angezeigt, wenn der Viewer im Popupmodus funktioniert und das System keinen nativen Vollbildmodus unterstützt. Sie können die Größe, die Skin und die Position der Schaltfläche mithilfe von CSS festlegen.
seo-description: Verursacht, dass der Viewer den Vollbildmodus aufruft oder verlässt, wenn der Benutzer darauf klickt. Diese Schaltfläche wird in der Hauptsteuerungsleiste angezeigt. Diese Schaltfläche wird nicht angezeigt, wenn der Viewer im Popupmodus funktioniert und das System keinen nativen Vollbildmodus unterstützt. Sie können die Größe, die Skin und die Position der Schaltfläche mithilfe von CSS festlegen.
seo-title: Schaltfläche "Vollbild"
solution: Experience Manager
title: Schaltfläche "Vollbild"
topic: Dynamic media
uuid: 1ee32e71-78bc-4cb2-858c-083c750ff1c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Full screen button{#full-screen-button}

Verursacht, dass der Viewer den Vollbildmodus aufruft oder verlässt, wenn der Benutzer darauf klickt. Diese Schaltfläche wird in der Hauptsteuerungsleiste angezeigt. Diese Schaltfläche wird nicht angezeigt, wenn der Viewer im Popupmodus funktioniert und das System keinen nativen Vollbildmodus unterstützt. Sie können die Größe, die Skin und die Position der Schaltfläche mithilfe von CSS festlegen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogviewer .s7fullscreenbutton`

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
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl die `state` als auch die `selected` Attributselektoren, die verwendet werden können, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden. Insbesondere `selected='true'` entspricht dies dem Status &quot;Vollbild&quot;und `selected='false'` dem Status &quot;normal&quot;.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) der Benutzeroberfläche.

Beispiel: Zum Einrichten einer Vollbildschaltfläche mit 28 x 28 Pixeln, die 4 Pixel vom unteren Rand und 5 Pixel vom rechten Rand der Hauptsteuerungsleiste positioniert ist, und zum Anzeigen eines anderen Bilds für jeden der vier verschiedenen Schaltflächenzustände, wenn diese ausgewählt oder nicht ausgewählt sind.

```
.s7ecatalogviewer .s7fullscreenbutton { 
bottom:4px; 
right:5px; 
width:28px; 
height:28px; 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

