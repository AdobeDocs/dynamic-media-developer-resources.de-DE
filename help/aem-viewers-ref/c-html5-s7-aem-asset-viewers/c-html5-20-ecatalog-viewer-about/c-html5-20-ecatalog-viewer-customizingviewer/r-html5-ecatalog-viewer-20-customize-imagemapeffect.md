---
description: Je nach dem Wert des Parameters mode zeigt der Viewer Imagemap-Symbole über der Ansicht an Orten an, an denen Maps ursprünglich im Scene7 Publishing System erstellt wurden, oder rendert exakte Bereiche, die mit der Form der ursprünglichen Imagemaps übereinstimmen.
seo-description: Je nach dem Wert des Parameters mode zeigt der Viewer Imagemap-Symbole über der Ansicht an Orten an, an denen Maps ursprünglich im Scene7 Publishing System erstellt wurden, oder rendert exakte Bereiche, die mit der Form der ursprünglichen Imagemaps übereinstimmen.
seo-title: Imagemap-Effekt
solution: Experience Manager
title: Imagemap-Effekt
topic: Dynamic media
uuid: 193d2f4e-77a2-4741-bf36-90ca31c600c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Image map effect{#image-map-effect}

Je nach dem Wert des Parameters mode zeigt der Viewer Imagemap-Symbole über der Ansicht an Orten an, an denen Maps ursprünglich im Scene7 Publishing System erstellt wurden, oder rendert exakte Bereiche, die mit der Form der ursprünglichen Imagemaps übereinstimmen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Imagemap-Symbols wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>Die `s7mapoverlay` CSS-Klasse, mit der Imagemap-Symbole in der Vergangenheit formatiert wurden, ist jetzt veraltet. verwenden `s7icon` .

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Imagemap-Symbol-Grafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Imagemap-Symbols in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Imagemap-Symbols in Pixel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Das Symbol &quot;Imagemap&quot;unterstützt die `state` Attributauswahl, mit der Sie verschiedene Skins auf die Symbolzustände &quot; `default` und&quot;anwenden können `active`.

Beispiel: Richten Sie ein Imagemap-Symbol mit 28 x 28 Pixeln ein, das für jeden der beiden verschiedenen Symbolstatus ein anderes Bild anzeigt.

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Siehe auch [Unterstützung](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)von Imagemaps.

Das Erscheinungsbild des Imagemap-Bereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background </span> </p> </td> 
   <td colname="col2"> <p> Füllfarbe des Imagemap-Bereichs. </p> <p>Wird im Format #RRGGBB, RGB(R,G,B) oder RGBA(R,G,B,A) angegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Füllfarbe des Imagemap-Bereichs. </p> <p>Wird im Format #RRGGBB, RGB(R,G,B) oder RGBA(R,G,B,A) angegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p> Randstil für Imagemap-Bereiche. </p> <p>Wird als <span class="codeph"> Volltonfarbe <span class="varname"> angegeben </span><span class="varname"> , wobei die </span></span>Breite in Pixel und die-Farbe <span class="codeph"> <span class="varname"> </span> </span> <span class="codeph"> <span class="varname"> </span> </span> als #RRGBB, RGB(R,G,B) oder RGBA(R,G,B,A) angegeben wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie einen transparenten Imagemap-Bereich mit schwarzem `1` Pixel-Rand ein:

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

