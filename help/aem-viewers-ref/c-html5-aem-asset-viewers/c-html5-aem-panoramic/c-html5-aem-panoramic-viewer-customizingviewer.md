---
title: Anpassen des Panorama-Viewers
description: Die visuelle Anpassung und die meisten Verhaltensanpassungen für den Panorama-Viewer erfolgen durch die Erstellung eines benutzerdefinierten CSS.
keywords: responsive
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

Die visuelle Anpassung und die meisten Verhaltensanpassungen erfolgen durch die Erstellung eines benutzerdefinierten CSS.

Der vorgeschlagene Workflow besteht darin, die Standard-CSS-Datei für den entsprechenden Viewer zu übernehmen, sie an einen anderen Speicherort zu kopieren, sie anzupassen und den Speicherort der angepassten Datei im Befehl `style=` anzugeben.

Standard-CSS-Dateien finden Sie unter folgendem Speicherort:

`<s7viewers_root>/html5/PanoramicViewer.css`

Benutzerdefinierte CSS-Dateien müssen dieselben Klassendeklarationen wie die Standarddeklaration enthalten. Wenn eine Klassendeklaration weggelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitstellt.

Alternativ können Sie benutzerdefinierte CSS-Regeln bereitstellen, indem Sie eingebettete Stile direkt auf der Webseite oder in einer verknüpften externen CSS-Regel verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer dem Container-DOM-Element die Klasse `.s7panoramicviewer` zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit dem Befehl `style=` übergeben wird, verwenden Sie die Klasse `.s7panoramicviewer` als übergeordnete Klasse in der untergeordneten Auswahl für Ihre CSS-Regeln. Wenn Sie eingebettete Stile auf der Web-Seite verwenden, qualifizieren Sie diesen Selektor zusätzlich wie folgt mit einer ID des Container-DOM-Elements:

`#<containerId>.s7panoramicviewer.`


## Allgemeine Hinweise und Hinweise zu Stilen {#section-95855dccbbc444e79970f1aaa3260b7b}

* Alle Pfade zu externen Assets innerhalb von CSS werden mit dem CSS-Speicherort aufgelöst, nicht mit dem Viewer-HTML-Seitenspeicherort. Berücksichtigen Sie dies beim Kopieren der Standard-CSS an einen anderen Speicherort: Möglicherweise müssen auch die Standard-Assets kopiert oder Pfade in der benutzerdefinierten CSS aktualisiert werden.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Transparenz erforderlich ist, wird das Format `rgba(R,G,B,A)` vorgeschlagen. Andernfalls ist Transparenz nicht erforderlich `#RRGGBB` kann verwendet werden.

Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung der Regel `!IMPORTANT` nicht unterstützt, um Viewer-Elemente zu gestalten. Insbesondere sollte die Regel `!IMPORTANT` nicht verwendet werden, um Standard- oder Laufzeitstile zu überschreiben, die vom Viewer- oder Viewer-SDK bereitgestellt werden, da sie sich auf das richtige Komponentenverhalten auswirken kann. Stattdessen sollten CSS-Selektoren mit entsprechender Spezifität verwendet werden, um in diesem Referenzhandbuch dokumentierte CSS-Eigenschaften festzulegen.

## CSS für Panorama-Viewer {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Hauptanzeige-Bereich**
Der Hauptansichtsbereich ist der Bereich, der vom Panoramabild belegt ist.  Normalerweise wird sie an den verfügbaren Gerätebildschirm angepasst, wenn keine Größe angegeben ist.

Das Erscheinungsbild des Anzeigebereichs wird mit der CSS-Klassenauswahl gesteuert:
`.s7panoramicviewer`

Zu den anwendbaren CSS-Eigenschaften gehören:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> die Breite des Viewers; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Höhe des Viewers; </span> </p> </td> 
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

**Panoramaansicht**
Hauptansicht besteht aus dem Panoramabild.

Das Erscheinungsbild der Hauptansicht wird mit dem CSS-Klassenselektor gesteuert:
`.s7panoramicviewer .s7panoramicview`

Zu den anwendbaren CSS-Eigenschaften gehören:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Hintergrundfarbe der Hauptansicht; </span> </p> </td> 
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
