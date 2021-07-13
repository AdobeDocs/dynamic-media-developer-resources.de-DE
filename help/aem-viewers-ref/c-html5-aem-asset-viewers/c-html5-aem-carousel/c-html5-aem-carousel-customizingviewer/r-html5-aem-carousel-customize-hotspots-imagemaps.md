---
description: Der Viewer zeigt Hotspot-Symbole über der Hauptansicht an Orten an, an denen Hotspots ursprünglich in Dynamic Media von AEM Assets - On-Demand - erstellt wurden.
solution: Experience Manager
title: Hotspots und Imagemaps
feature: Dynamic Media Classic,Viewer,SDK/API,Karussellbanner
role: Developer,User
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---

# Hotspots und Imagemaps{#hotspots-and-image-maps}

Der Viewer zeigt Hotspot-Symbole über der Hauptansicht an Orten an, an denen Hotspots ursprünglich in Dynamic Media von AEM Assets - On-Demand - erstellt wurden.

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
   <td colname="col2"> <p>Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Hotspot-Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Hotspot-Symbols. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Hotspot-Symbol mit 56 x 56 Pixel ein, das für jeden der beiden Symbolstatus ein anderes Bild anzeigt:

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
   <td colname="col2"> <p>Füllfarbe für Imagemap-Bereich. </p> <p>Geben Sie diese Farbe in den Formaten <span class="codeph"> #RGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> oder <span class="codeph"> RGBA(R,G,B,A) </span> an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Füllfarbe für Imagemap-Bereich. </p> <p>Geben Sie diese Farbe in den Formaten <span class="codeph"> #RGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> oder <span class="codeph"> RGBA(R,G,B,A) </span> an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p> Randstil der Imagemap Sollte als " <span class="codeph"> width </span> <span class="codeph"> solid color </span>"angegeben werden, wobei <span class="codeph"> width </span> in Pixel ausgedrückt wird und <span class="codeph"> Farbe </span> als <span class="codeph"> #RGGBB </span>, <span class="codeph"> RGB(R,G,B) &lt;a1 1/&gt; oder <span class="codeph"> RGBA(R,G,B,A) </span>.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie einen transparenten Imagemap-Bereich mit einem schwarzen Rahmen von einem Pixel ein:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
