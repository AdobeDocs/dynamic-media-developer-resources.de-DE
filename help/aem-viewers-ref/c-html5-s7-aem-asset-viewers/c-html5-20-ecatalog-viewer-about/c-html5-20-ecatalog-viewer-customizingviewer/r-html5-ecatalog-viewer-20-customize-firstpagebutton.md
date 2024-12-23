---
title: Schaltfläche „Erste Seite“
description: Durch Klicken oder Tippen auf diese Schaltfläche gelangen die Benutzenden zur ersten Seite im Katalog. Diese Schaltfläche wird in der Hauptsteuerleiste auf Desktop-Systemen und Tablets angezeigt. Bei Mobiltelefonen wird sie zu einer sekundären Steuerleiste hinzugefügt. Sie können diese Schaltfläche mithilfe von CSS skalieren, anpassen und positionieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 50ebf51f-aa51-4778-8956-f969c30443aa
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Schaltfläche „Erste Seite“{#first-page-button}

Wenn Sie diese Schaltfläche auswählen oder darauf tippen, gelangen die Benutzenden zur ersten Seite im Katalog. Diese Schaltfläche wird in der Hauptsteuerleiste auf Desktop-Systemen und Tablets angezeigt. Bei Mobiltelefonen wird sie zu einer sekundären Steuerleiste hinzugefügt. Sie können diese Schaltfläche mithilfe von CSS skalieren, anpassen und positionieren.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit dem folgenden CSS-Klassenselektor gesteuert:

`.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton`

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
   <td colname="col2"> <p>Position am oberen Rand der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Position am rechten Rand der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Position am unteren Rand der Hauptsteuerleiste (auf Desktop-Systemen und Tablets) oder der sekundären Steuerleiste (auf Mobiltelefonen), einschließlich Auffüllung. </p> </td> 
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
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: So richten Sie eine Schaltfläche für die erste Seite ein, die 28 x 28 Pixel groß ist und 4 Pixel vom unteren Rand und 220 Pixel vom linken Rand der Hauptsteuerleiste entfernt positioniert ist. Schließlich zeigt für jeden der vier verschiedenen Schaltflächenzustände ein eigenes Bild an.

```
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton { 
bottom:4px; 
left:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/FirstPageButton_dark_up.png); 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/FirstPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/FirstPageButton_dark_down.png); 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/FirstPageButton_dark_disabled.png); 
}
```
