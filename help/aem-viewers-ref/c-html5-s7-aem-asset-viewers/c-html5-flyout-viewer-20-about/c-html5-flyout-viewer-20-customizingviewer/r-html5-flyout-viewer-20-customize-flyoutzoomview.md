---
title: Flyout-Zoom-Ansicht
description: Die Hauptansicht besteht aus dem statischen Bild und dem gezoomten Bild, das in der Flyout-Ansicht angezeigt wird. Sie besteht außerdem aus dem markierten Navigationsbereich, der über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die über dem statischen Bild angezeigt wird.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Flyout-Zoom-Ansicht{#flyout-zoom-view}

Die Hauptansicht besteht aus dem statischen Bild und dem gezoomten Bild, das in der Flyout-Ansicht angezeigt wird. Sie besteht außerdem aus dem markierten Navigationsbereich, der über dem statischen Bild angezeigt wird, und der Tipp-Meldung, die über dem statischen Bild angezeigt wird.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn die Abmessungen des angezeigten Bildes nicht mit den Abmessungen der Flyout-Zoom-Ansicht übereinstimmen, wird der Bildinhalt im Anzeigebereich des Rechtecks der Flyout-Zoom-Ansicht zentriert.

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

**CSS-Eigenschaften der Flyout-Ansicht**

Das Erscheinungsbild der Flyout-Ansicht wird mit der folgenden CSS-Klassenauswahl gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> Die horizontale Position der Flyout-Ansicht, relativ zur oberen linken Ecke der Hauptansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Position der Flyout-Ansicht relativ zur oberen linken Ecke der Hauptansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Flyout-Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Flyout-Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Der Rahmen der Flyout-Ansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um eine Flyout-Ansicht auf 600 x 400 Pixel einzurichten, die mit einem Offset von 100 Pixel rechts von der Hauptansicht von 512 x 288 angezeigt wird, wie im vorherigen Beispiel gezeigt:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**CSS-Eigenschaften der Hervorhebung in der Hauptansicht**

Das Erscheinungsbild der Hervorhebung in der Hauptansicht wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Es ist möglich, Hintergrund, Rahmen, Transparenz und ähnliche Attribute mithilfe von CSS zu steuern. Die Größe und Position des Hervorhebungs-DOM-Elements wird jedoch von der Viewer-Logik verwaltet. Das Überschreiben über CSS wird nicht unterstützt.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Die Farbe der Markierung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft </span> </p> </td> 
   <td colname="col2"> <p> Deckkraft hervorheben. </p> <p>Verwenden Sie für Internet Explorer 8 <span class="codeph"> filter:alpha(opacity-..); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Die Randhervorhebung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Einrichten einer grünen Hervorhebung mit 40 % Transparenz und einem roten Rahmen von einem Pixel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**CSS-Eigenschaften des Cursors**

Wenn der Parameter `highlightmode` auf `cursor` gesetzt ist, wird die Hervorhebung in der Hauptansicht durch die Bilddarstellung des Cursors mit fester Größe ersetzt, die mit dem CSS-Klassenselektor gesteuert wird:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

Es ist möglich, das Hintergrundbild und die Größe mithilfe von CSS zu steuern.

Zu den anwendbaren CSS-Eigenschaften gehören:

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Cursorgrafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Cursorbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Cursorhöhe. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cursor unterstützt die &quot;`input`&quot;-Attributauswahl, mit der verschiedene Cursorgrafiken und -größen auf verschiedene Geräte angewendet werden können. Insbesondere entspricht `input="mouse"` den Desktop-Systemen und `input="touch"` den Touch-Geräten.

**CSS-Eigenschaften der Überlagerung**

Wenn der Parameter `overlay` auf `1` gesetzt ist, wird der Bereich um den Hervorhebungsrahmen oder das Cursorbild mit dem CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Überlagerungsfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft </span> </p> </td> 
   <td colname="col2"> <p>Überlagerungsdeckkraft. </p> </td> 
  </tr> 
 </tbody> 
</table>

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

Die Tipp-Nachricht kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) .

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
