---
description: Im Inline-Zoom-Modus besteht die Hauptansicht aus dem statischen Ansicht, dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die über dem statischen Bild angezeigt wird.
seo-description: Im Inline-Zoom-Modus besteht die Hauptansicht aus dem statischen Ansicht, dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die über dem statischen Bild angezeigt wird.
seo-title: Flyout-Zoom-Ansicht
solution: Experience Manager
title: Flyout-Zoom-Ansicht
topic: Dynamic media
uuid: c4c94432-7b6f-40a8-ae5f-9423234f3656
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 5%

---


# Flyout-Zoom-Ansicht{#flyout-zoom-view}

Im Inline-Zoom-Modus besteht die Hauptansicht aus dem statischen Ansicht, dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die über dem statischen Bild angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Hauptklasse wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7flyoutzoomview
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
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

Das Erscheinungsbild der Tipp-Meldung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

Sie können Schriftschnitt, Größendarstellung und vertikalen Offset mithilfe von CSS konfigurieren. Die horizontale Ausrichtung wird jedoch von der Viewer-Logik verwaltet. Das Überschreiben durch CSS mit den Eigenschaften `left` oder `right` wird nicht unterstützt.

**CSS-Eigenschaften der Tippmeldung**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfüllfarbe der Nachricht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius des Nachrichtenhintergrunds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Versatz unten in der Haupt-Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Farbe des Tipp-Textes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrunddeckkraft der Nachricht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Umrandung des Nachrichtentextes. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Tippmeldung kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Beispiel: Um eine halbtransparente Tipp-Meldung mit einer weißen Arial-12-Pixel-Schrift einzurichten, werden 50 Pixel vom unteren Rand der Ansicht, der Auffüllung und einem gerundeten Rand versetzt:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
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

