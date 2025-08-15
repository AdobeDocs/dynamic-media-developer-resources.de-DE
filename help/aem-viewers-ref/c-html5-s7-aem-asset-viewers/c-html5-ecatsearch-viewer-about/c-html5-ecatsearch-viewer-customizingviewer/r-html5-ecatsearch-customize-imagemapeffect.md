---
title: Imagemap-Effekt
description: Abhängig vom Wert des Modusparameters zeigt der Viewer Imagemap-Symbole über der Hauptansicht an Orten an, an denen Karten ursprünglich in Dynamic Media Classic erstellt wurden, oder rendert exakte Regionen, die der Form von Originalbildkarten entsprechen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 873fc387-1d2a-4d74-b85e-fcbb13b691c5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Imagemap-Effekt{#image-map-effect}

Abhängig vom Wert des Modusparameters zeigt der Viewer Imagemap-Symbole über der Hauptansicht an Orten an, an denen Karten ursprünglich in Dynamic Media Classic erstellt wurden, oder rendert exakte Regionen, die der Form von Originalbildkarten entsprechen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Imagemap-Symbols wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>Die `s7mapoverlay` CSS-Klasse, die in der Vergangenheit zum Formatieren von Imagemap-Symbolen verwendet wurde, ist jetzt veraltet. Verwenden Sie stattdessen `s7icon`.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Imagemap-Symbol für Bildmaterial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Imagemap-Symbols in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Imagemap-Symbols in Pixel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Das Imagemap-Symbol unterstützt die `state`-Attributauswahl, mit der Sie verschiedene Skins auf die Symbolstatus von `default` und `active` anwenden können.

Beispiel: Richten Sie ein Imagemap-Symbol mit 28 x 28 Pixeln ein, das für jeden der beiden verschiedenen Symbolstatus ein anderes Bild anzeigt.

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

Das Erscheinungsbild des Imagemap-Bereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Füllfarbe des Imagemap-Bereichs. </p> <p>Wird im #RRGGBB-, RGB(R,G,B)- oder RGBA(R,G,B,A)-Format angegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Füllfarbe des Imagemap-Bereichs. </p> <p>Wird im #RRGGBB-, RGB(R,G,B)- oder RGBA(R,G,B,A)-Format angegeben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Rahmenstil der Imagemap-Region. </p> <p>Wird angegeben als <span class="codeph"> <span class="varname"> Breite </span> einfarbigen <span class="varname"> </span> </span>, wobei <span class="codeph"> <span class="varname"> Breite </span> </span> in Pixel ausgedrückt wird und <span class="codeph"> <span class="varname"> Farbe </span> als #RRGGBB, RGB(R,G,B) oder RGBA(R,G,B,A) eingestellt </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel : Richten Sie einen transparenten Imagemap-Bereich mit `1` Pixel schwarzem Rahmen ein:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
