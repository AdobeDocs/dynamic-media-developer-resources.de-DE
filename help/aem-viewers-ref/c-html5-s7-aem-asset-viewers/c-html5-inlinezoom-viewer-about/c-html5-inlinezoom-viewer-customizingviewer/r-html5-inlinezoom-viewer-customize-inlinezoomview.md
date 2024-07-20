---
title: Flyout-Zoom-Ansicht
description: Die Hauptansicht besteht aus dem statischen Bild und dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird. Es besteht auch aus der Tipp-Meldung, die auf dem statischen Bild angezeigt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Flyout-Zoom-Ansicht{#flyout-zoom-view}

Die Hauptansicht besteht aus dem statischen Bild und dem gezoomten Bild, das in der Flyout-Ansicht über dem statischen Bild angezeigt wird. Es besteht auch aus der Tipp-Meldung, die auf dem statischen Bild angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften der Hauptansicht**

Das Erscheinungsbild der Hauptansicht wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Die Hintergrundfarbe der Hauptansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Hauptansicht transparent zu machen:

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

Es ist möglich, Schriftstil, Größe, Erscheinungsbild und vertikalen Versatz über CSS zu konfigurieren. Die horizontale Ausrichtung wird jedoch von der Viewer-Logik verwaltet. Das Überschreiben durch CSS mit den Eigenschaften `left` oder `right` wird nicht unterstützt.

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
   <td colname="col2"> <p>Versatz unten in der Hauptansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p>Auffüllung um den Nachrichtentext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfüllfarbe des Nachrichtentextes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundrahmenradius des Nachrichtentextes </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft </span> </p> </td> 
   <td colname="col2"> <p>Hintergrunddeckkraft des Nachrichtentextes. </p> <p>Verwenden Sie für Internet Explorer 8 <span class="codeph"> filter:alpha(opacity-..) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Tipp-Nachricht kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) .

.

Beispiel: Zum Einrichten einer halbtransparenten Tipp-Meldung mit weißer Arial® 12-px-Schriftart, 50 Pixel Offset vom unteren Rand der Hauptansicht, Abstand und gerundeter Rahmen:

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
