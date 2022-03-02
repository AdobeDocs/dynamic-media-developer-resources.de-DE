---
title: Bild-Map-Effekt
description: Je nach Wert des Parameter mode zeigt der Viewer Imagemap-Symbole über der Hauptansicht an Stellen an, an denen Maps ursprünglich in Dynamic Media Classic erstellt wurden. Oder sie rendert exakte Bereiche, die mit der Form der ursprünglichen Imagemaps übereinstimmen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3816118f-4eb7-4436-9f54-155dde077734
source-git-commit: 6087b48b898e93e605c3873cbd5132b74d04225f
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# Bild-Map-Effekt{#image-map-effect}

Je nach Wert des Parameter mode zeigt der Viewer Imagemap-Symbole über der Hauptansicht an Stellen an, an denen Maps ursprünglich in Dynamic Media Classic erstellt wurden. Oder sie rendert exakte Bereiche, die mit der Form der ursprünglichen Imagemaps übereinstimmen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Imagemap-Symbols wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>Die `s7mapoverlay` Die CSS-Klasse, die in der Vergangenheit zum Formatieren von Imagemap-Symbolen verwendet wurde, wird jetzt nicht mehr unterstützt. use `s7icon` anstatt.

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
   <td colname="col2"> <p>Bildzuordnungssymbol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
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
>Das Symbol &quot;Imagemap&quot;unterstützt `state` -Attributauswahl, mit der Sie verschiedene Skins auf die Symbolstatus von `default` und `active`.

Beispiel: Richten Sie ein Imagemap-Symbol mit 28 x 28 Pixel ein, das für jeden der beiden verschiedenen Symbolstatus ein anderes Bild anzeigt.

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

Siehe auch [Unterstützung von Imagemaps](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

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
   <td colname="col2"> <p> Füllfarbe für Imagemap-Bereich. </p> <p>Wird im Format #RGGBB, RGB(R,G,B) oder RGBA(R,G,B,A) angegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Füllfarbe für Imagemap-Bereich. </p> <p>Wird im Format #RGGBB, RGB(R,G,B) oder RGBA(R,G,B,A) angegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p> Randstil der Imagemap </p> <p>Angegeben als <span class="codeph"> <span class="varname"> width </span> solid <span class="varname"> color </span> </span>, wobei <span class="codeph"> <span class="varname"> width </span> </span> wird in Pixel ausgedrückt und <span class="codeph"> <span class="varname"> color </span> </span> wird als #RGGBB, RGB(R,G,B) oder RGBA(R,G,B,A) festgelegt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Einrichten eines transparenten Imagemap-Bereichs mit `1` Pixelschwarzer Rahmen :

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
