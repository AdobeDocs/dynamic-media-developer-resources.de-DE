---
description: Im Inline-Zoom-Modus besteht die Hauptansicht aus dem statischen Bild, dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die auf dem statischen Bild angezeigt wird.
solution: Experience Manager
title: Flyout-Zoom-Ansicht
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: 46c91d1f-5809-4270-a06d-5068d20a6341
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 4%

---

# Flyout-Zoom-Ansicht{#flyout-zoom-view}

Im Inline-Zoom-Modus besteht die Hauptansicht aus dem statischen Bild, dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die auf dem statischen Bild angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Hauptansicht wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col2"> <p> Die Hintergrundfarbe der Hauptansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Hauptansicht transparent zu machen:

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

Es ist möglich, Schriftstil, Größenaussehen und vertikalen Versatz über CSS zu konfigurieren. Die horizontale Ausrichtung wird jedoch von der Viewer-Logik verwaltet. Das Überschreiben durch CSS mit den Eigenschaften `left` oder `right` wird nicht unterstützt.

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
   <td colname="col2"> <p>Füllfarbe für den Nachrichtenhintergrund. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Radius des Nachrichtenhintergrunds </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Versatz unten in der Hauptansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe für Tipps. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie  </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft  </span> </p> </td> 
   <td colname="col2"> <p> Deckkraft des Nachrichtenhintergrunds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Auffüllung um den Nachrichtentext. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Tipp-Nachricht kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Beispiel: So richten Sie eine halbtransparente Tipp-Meldung mit weißer Arial-12-px-Schriftart ein, die 50 Pixel vom unteren Rand der Hauptansicht, des Abstands und eines gerundeten Rahmens entfernt ist:

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
