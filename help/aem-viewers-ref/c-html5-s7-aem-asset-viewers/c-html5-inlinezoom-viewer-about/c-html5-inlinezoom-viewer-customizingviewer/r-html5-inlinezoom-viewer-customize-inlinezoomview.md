---
description: Die Haupt-Ansicht besteht aus dem statischen Bild, dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die über dem statischen Bild angezeigt wird.
seo-description: Die Haupt-Ansicht besteht aus dem statischen Bild, dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die über dem statischen Bild angezeigt wird.
seo-title: Flyout-Zoom-Ansicht
solution: Experience Manager
title: Flyout-Zoom-Ansicht
topic: Dynamic media
uuid: a918c775-a36a-44e8-9ca4-90cb8f5c3a5e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 2%

---


# Flyout-Zoom-Ansicht{#flyout-zoom-view}

Die Haupt-Ansicht besteht aus dem statischen Bild, dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die über dem statischen Bild angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften der Haupt-Ansicht**

Das Erscheinungsbild der Hauptklasse wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Die Hintergrundfarbe der Haupt-Ansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So machen Sie die Ansicht transparent:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**CSS-Eigenschaften der Tippmeldung**

Das Erscheinungsbild der Tipp-Meldung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Es ist möglich, Schriftstil, Größendarstellung und vertikalen Versatz mithilfe von CSS zu konfigurieren. Die horizontale Ausrichtung wird jedoch von der Viewer-Logik verwaltet. Das Überschreiben durch CSS mit den Eigenschaften `left` oder `right` wird nicht unterstützt.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Versatz unten in der Haupt-Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Umrandung des Nachrichtentextes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfüllfarbe des Nachrichtentextes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Rahmenradius des Nachrichtentextes im Hintergrund </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrunddeckkraft des Nachrichtentextes. </p> <p>Verwenden Sie für Internet Explorer 8 <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Tippmeldung kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27).

.

Beispiel: So richten Sie eine halbtransparente Tipp-Meldung mit einer weißen Arial-12-Pixel-Schrift ein, die um 50 Pixel vom unteren Rand der Ansicht, einer Auffüllung und einem gerundeten Rand versetzt ist:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```

