---
description: Der Rotationsindikator wird über dem Bereich der Ansicht überlagert. Es wird angezeigt, wenn sich das Bild in einem Reset-Zustand befindet und es hängt auch vom iconeffect-Parameter ab.
seo-description: Der Rotationsindikator wird über dem Bereich der Ansicht überlagert. Es wird angezeigt, wenn sich das Bild in einem Reset-Zustand befindet und es hängt auch vom iconeffect-Parameter ab.
seo-title: Effekt "Ansicht drehen"
solution: Experience Manager
title: Effekt "Ansicht drehen"
topic: Dynamic media
uuid: 33445a3d-51dc-47a4-a8d1-87d25ea001e1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# Effekt &quot;Ansicht drehen&quot;{#spin-view-icon-effect}

Der Rotationsindikator wird über dem Bereich der Ansicht überlagert. Es wird angezeigt, wenn sich das Bild in einem Reset-Zustand befindet und es hängt auch vom iconeffect-Parameter ab.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7spinview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Rotationsanzeigegrafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Rotationsanzeigebreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Rotationsindikators. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Rotationsanzeiger unterstützt den Attributselektor `state`, der bei eindimensionalen Rotationsset auf `spin_1D` und bei mehrdimensionalen Rotationsset auf `spin_2D` eingestellt ist.

Beispiel: Zum Einrichten eines Zoomindikators für 100 x 100 Pixel.

```
.s7mixedmediaviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```

