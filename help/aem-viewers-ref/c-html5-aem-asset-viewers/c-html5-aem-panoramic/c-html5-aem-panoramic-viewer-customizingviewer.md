---
title: Panorama-Viewer anpassen
description: Die gesamte visuelle Anpassung und die meisten Verhaltensanpassungen für den Panorama-Viewer werden durch die Erstellung eines benutzerdefinierten CSS vorgenommen.
keywords: Responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Anpassen des Video360 Viewer{#customizing-video-viewer}

Die gesamte visuelle Anpassung und die meisten Verhaltensanpassungen werden durch die Erstellung eines benutzerdefinierten CSS vorgenommen.

Der vorgeschlagene Workflow besteht darin, die standardmäßige CSS-Datei für den entsprechenden Viewer zu verwenden, sie an einen anderen Speicherort zu kopieren, anzupassen und den Speicherort der angepassten Datei im `style=`-Befehl anzugeben.

Standard-CSS-Dateien befinden sich unter folgendem Speicherort:

`<s7viewers_root>/html5/PanoramicViewer.css`

Benutzerdefinierte CSS-Datei muss dieselben Klassendeklarationen enthalten wie die Standarddeklaration. Wenn eine Klassendeklaration ausgelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitstellt.

Eine alternative Möglichkeit, benutzerdefinierte CSS-Regeln bereitzustellen, besteht darin, eingebettete Stile direkt auf der Web-Seite oder in einer der verknüpften externen CSS-Regeln zu verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer `.s7panoramicviewer` Klasse seinem Container-DOM-Element zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit `style=` Befehl übergeben wird, verwenden Sie `.s7panoramicviewer` Klasse als übergeordnete Klasse in einem untergeordneten Selektor für Ihre CSS-Regeln. Wenn Sie eingebettete Stile auf der Web-Seite verwenden, qualifizieren Sie diesen Selektor zusätzlich mit einer ID des Container-DOM-Elements wie folgt:

`#<containerId>.s7panoramicviewer.`


## Allgemeine Hinweise und Hinweise zu Stilen {#section-95855dccbbc444e79970f1aaa3260b7b}

* Alle Pfade zu externen Assets innerhalb von CSS werden gegen den CSS-Speicherort aufgelöst, nicht gegen den HTML-Seitenspeicherort des Viewers. Berücksichtigen Sie dies, wenn Sie das Standard-CSS an einen anderen Speicherort kopieren: Es kann erforderlich sein, entweder auch die Standard-Assets zu kopieren oder Pfade innerhalb des benutzerdefinierten CSS zu aktualisieren.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Transparenz erforderlich ist, wird `rgba(R,G,B,A)` Format empfohlen. Andernfalls ist keine Transparenz erforderlich `#RRGGBB` kann verwendet werden.

Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung `!IMPORTANT` Regel nicht unterstützt, um Viewer-Elemente zu gestalten. Insbesondere sollte `!IMPORTANT` Regel nicht verwendet werden, um vom Viewer oder Viewer-SDK bereitgestellte Standard- oder Laufzeitstile zu überschreiben, da dies das ordnungsgemäße Komponentenverhalten beeinflussen kann. Stattdessen sollten CSS-Selektoren mit der richtigen Spezifität verwendet werden, um CSS-Eigenschaften festzulegen, die in diesem Referenzhandbuch dokumentiert sind.

## Panorama-Viewer-CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Hauptanzeigebereich**
Der Hauptansichtsbereich ist der Bereich, in dem sich das Panoramabild befindet.  Normalerweise wird festgelegt, dass der Bildschirm auf den verfügbaren Gerätebildschirm angepasst wird, wenn keine Größe angegeben ist.

Das Erscheinungsbild des Anzeigebereichs wird mit dem CSS-Klassenselektor gesteuert:
`.s7panoramicviewer`

Zu den geltenden CSS-Eigenschaften gehören:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> die Breite des Viewers </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> die Höhe des Viewers </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel:
So richten Sie einen Viewer mit einer Größe von 1024 x 512 Pixel ein.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Panoramablick**
Die Hauptansicht besteht aus dem Panoramabild.

Das Erscheinungsbild der Hauptansicht wird mit dem CSS-Klassenselektor gesteuert:
`.s7panoramicviewer .s7panoramicview`

Zu den geltenden CSS-Eigenschaften gehören:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> die Hintergrundfarbe der Hauptansicht </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel:
So machen Sie die Hauptansicht transparent:

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
