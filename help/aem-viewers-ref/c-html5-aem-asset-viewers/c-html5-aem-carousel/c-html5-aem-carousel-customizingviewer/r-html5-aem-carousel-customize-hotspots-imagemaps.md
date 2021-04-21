---
description: Der Viewer zeigt Hotspot-Symbole über der wichtigsten Ansicht an Orten an, an denen Hotspots ursprünglich in Dynamic Media von AEM Assets - On-Demand - verfasst wurden.
solution: Experience Manager
title: Hotspots und Imagemaps
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 1%

---

# Hotspots und Imagemaps{#hotspots-and-image-maps}

Der Viewer zeigt Hotspot-Symbole über der wichtigsten Ansicht an Orten an, an denen Hotspots ursprünglich in Dynamic Media von AEM Assets - On-Demand - verfasst wurden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Hotspot-Symbols wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7carouselviewer .s7imagemapeffect .s7icon
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
   <td colname="col2"> <p>Hotspot-Symbolgrafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Hotspot-Symbolbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Hotspot-Symbols. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Hotspot-Symbol mit 56 x 56 Pixel ein, das für jeden der beiden verschiedenen Symbolstatus ein anderes Bild anzeigt:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**CSS-Eigenschaften des Imagemap-Bereichs**

Das Erscheinungsbild des Imagemap-Bereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>Füllfarbe des Imagemap-Bereichs. </p> <p>Geben Sie diese Farbe in den Formaten <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> oder <span class="codeph"> RGBA(R,G,B,A) </span> an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Füllfarbe des Imagemap-Bereichs. </p> <p>Geben Sie diese Farbe in den Formaten <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> oder <span class="codeph"> RGBA(R,G,B,A) </span> an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p> Randstil für Imagemap-Bereiche. Sollte als "<span class="codeph"> width </span> <span class="codeph"> solid color </span>"angegeben werden, wobei <span class="codeph"> width </span> in Pixel und <span class="codeph"> color </span> als <span class="codeph"> #RGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> 1/&gt; oder <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie einen transparenten Imagemap-Bereich mit einem schwarzen Rand von einem Pixel ein:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
