---
description: Die Hauptansicht besteht aus dem statischen Bild, dem gezoomten Bild in der Flyout-Ansicht, dem markierten Navigationsbereich über dem statischen Bild und der Tipp-Meldung, die auf dem statischen Ansicht angezeigt wird.
seo-description: Die Hauptansicht besteht aus dem statischen Bild, dem gezoomten Bild in der Flyout-Ansicht, dem markierten Navigationsbereich über dem statischen Bild und der Tipp-Meldung, die auf dem statischen Ansicht angezeigt wird.
seo-title: Flyout-Zoom-Ansicht
solution: Experience Manager
title: Flyout-Zoom-Ansicht
topic: Dynamic media
uuid: 35c60228-3044-442b-a8e2-e13d0bd306a5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 2%

---


# Flyout-Zoom-Ansicht{#flyout-zoom-view}

Die Hauptansicht besteht aus dem statischen Bild, dem gezoomten Bild in der Flyout-Ansicht, dem markierten Navigationsbereich über dem statischen Bild und der Tipp-Meldung, die auf dem statischen Ansicht angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn die Abmessungen des angezeigten Bildes nicht mit den Abmessungen der Flyout-Zoom-Ansicht übereinstimmen, wird der Bildinhalt innerhalb des Rechteckanzeigebereichs der Flyout-Zoom-Ansicht zentriert.

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

**CSS-Eigenschaften der Flyout-Ansicht**

Das Erscheinungsbild der Flyout-Ansicht wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p> Die horizontale Position der Flyout-Ansicht, relativ zur oberen linken Ecke der Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Position der Flyout-Ansicht, relativ zur oberen linken Ecke der Haupt-Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Flyout-Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Flyout-Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Der Rand der Flyout-Ansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Flyout-Ansicht auf 600 x 400 Pixel ein, die mit 100 Pixel Abstand rechts von der im vorherigen Beispiel gezeigten 512 x 288-Ansicht angezeigt wird:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**CSS-Eigenschaften der Hervorhebung in der Haupt-Ansicht**

Das Erscheinungsbild der Hervorhebung in der Haupt-Ansicht wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Es ist möglich, Hintergrund, Rahmen, Transparenz und ähnliche Attribute mithilfe von CSS zu steuern. Die Größe und Position des DOM-Elements für das Hervorheben wird jedoch von der Viewer-Logik verwaltet. Das Überschreiben durch CSS wird nicht unterstützt.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Die Farbe der Hervorhebung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft  </span> </p> </td> 
   <td colname="col2"> <p> Markieren Sie Deckkraft. </p> <p>Verwenden Sie für Internet Explorer 8 <span class="codeph"> filter:alpha(opacity-..) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Die Randhervorhebung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie grüne Hervorhebung mit 40 % Transparenz und einem roten Rand von einem Pixel ein:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**CSS-Eigenschaften des Cursors**

Wenn der Parameter `highlightmode` auf `cursor` festgelegt ist, werden die Hervorhebungen in der Hauptversion durch die Cursorgrafik mit fester Ansicht ersetzt, die mit der CSS-Klassenauswahl gesteuert wird:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

Es ist möglich, das Hintergrundbild und die Größe mithilfe von CSS zu steuern.

Zu den CSS-Eigenschaften gehören:

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Cursorgrafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Cursorbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Cursorhöhe. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cursor unterstützt die Attributauswahl `input`, mit der verschiedene Cursorgrafiken und -größen auf verschiedene Geräte angewendet werden können. Insbesondere entspricht `input="mouse"` den Desktop-Systemen und `input="touch"` den Touch-Geräten.

**CSS-Eigenschaften der Überlagerung**

Wenn der Parameter `overlay` auf `1` eingestellt ist, wird der Bereich um den Markierungsrahmen oder das Cursorbild mit dem CSS-Klassenselektor gesteuert:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Überlagerungsfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft  </span> </p> </td> 
   <td colname="col2"> <p>Deckkraft der Überlagerung. </p> </td> 
  </tr> 
 </tbody> 
</table>

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

Die Tippmeldung kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27).

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

