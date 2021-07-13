---
description: Je nach Wert des Parameter mode zeigt der Viewer Imagemap-Symbole über der Hauptansicht an Stellen an, an denen Karten ursprünglich in Dynamic Media Classic erstellt wurden, oder rendert exakte Bereiche, die mit der Form der Originalbildzuordnungen übereinstimmen.
solution: Experience Manager
title: Bild-Map-Effekt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 873fc387-1d2a-4d74-b85e-fcbb13b691c5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# Bild-Map-Effekt{#image-map-effect}

Je nach Wert des Parameter mode zeigt der Viewer Imagemap-Symbole über der Hauptansicht an Stellen an, an denen Karten ursprünglich in Dynamic Media Classic erstellt wurden, oder rendert exakte Bereiche, die mit der Form der Originalbildzuordnungen übereinstimmen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Imagemap-Symbols wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>Die CSS-Klasse `s7mapoverlay`, die in der Vergangenheit zum Formatieren von Imagemap-Symbolen verwendet wurde, wird jetzt nicht mehr unterstützt. Verwenden Sie stattdessen `s7icon` .

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
   <td colname="col2"> <p>Bildzuordnungssymbol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bildzuordnungssymbolbreite in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Imagemap-Symbols in Pixel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Das Symbol &quot;Imagemap&quot;unterstützt die Attributauswahl `state`, mit der Sie verschiedene Skins auf die Symbolstatus `default` und `active` anwenden können.

Beispiel: Richten Sie ein Imagemap-Symbol mit 28 x 28 Pixel ein, das für jeden der beiden verschiedenen Symbolstatus ein anderes Bild anzeigt.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Siehe auch [Unterstützung von Imagemaps](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

Das Erscheinungsbild des Imagemap-Bereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
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
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p> Füllfarbe für Imagemap-Bereich. </p> <p>Wird im Format #RGGBB, RGB(R,G,B) oder RGBA(R,G,B,A) angegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Füllfarbe für Imagemap-Bereich. </p> <p>Wird im Format #RGGBB, RGB(R,G,B) oder RGBA(R,G,B,A) angegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p> Randstil der Imagemap </p> <p>Wird angegeben als <span class="codeph"> <span class="varname"> Breite </span> Feste <span class="varname"> Farbe </span> </span>, wobei <span class="codeph"> <span class="varname"> Breite </span> </span> in Pixel und <span class="codeph"> <span class="varname"> Farbe </span> </span> festgelegt ist. #RRGGBB, RGB(R,G,B) oder RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie einen transparenten Imagemap-Bereich mit `1` Pixelschwarzrahmen ein:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
