---
title: Zurücksetzen-Schaltfläche für Zoom
description: Durch Klicken oder Tippen auf diese Schaltfläche wird ein Bild in der Hauptansicht zurückgesetzt. Sie können diese Schaltfläche mithilfe von CSS skalieren, anpassen und positionieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 18663c1f-5645-41c7-bf26-241ad7c2c3b5
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# Zurücksetzen-Schaltfläche für Zoom{#zoom-reset-button}

Durch Auswählen oder Tippen auf diese Schaltfläche wird ein Bild in der Hauptansicht zurückgesetzt. Sie können diese Schaltfläche mithilfe von CSS skalieren, anpassen und positionieren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7zoomviewer .s7zoomresetbutton
```

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
   <td colname="col2"> <p>Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand aus, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand aus, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Position ab dem unteren Rand, einschließlich Abstand. </p> </td> 
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
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: So richten Sie eine Zurücksetzen-Schaltfläche für den Zoom ein, die 32 x 32 Pixel groß ist und sechs Pixel vom oberen und rechten Rand des Viewers entfernt positioniert ist. Schließlich zeigt für jeden der vier verschiedenen Schaltflächenzustände ein eigenes Bild an.

```
.s7zoomviewer .s7zoomresetbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7zoomviewer .s7zoomresetbutton [state='up'] { 
background-image:url(images/v2/ZoomResetButton_dark_up.png); 
} 
.s7zoomviewer .s7zoomresetbutton [state='over'] {  
background-image:url(images/v2/ZoomResettButton_dark_over.png); 
} 
.s7zoomviewer .s7zoomresetbutton [state='down'] {  
background-image:url(images/v2/ZoomResetButton_dark_down.png); 
} 
.s7zoomviewer .s7zoomresetbutton [state='disabled'] { 
background-image:url(images/v2/ZoomResetButton_dark_disabled.png); 
}
```
