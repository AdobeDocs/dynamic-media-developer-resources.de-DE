---
title: Anpassen des Flyout-Viewers
description: Anpassen des Flyout-Viewers
keywords: Responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b7898044-5178-4cdf-ab52-9996a61a3a35
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1272'
ht-degree: 0%

---

# Anpassen des Flyout-Viewers{#customizing-flyout-viewer}

Die visuelle Anpassung und die meisten Verhaltensanpassungen werden durch die Erstellung eines benutzerdefinierten CSS durchgeführt.

Der vorgeschlagene Workflow besteht darin, die standardmäßige CSS-Datei für den entsprechenden Viewer zu verwenden, sie an einen anderen Speicherort zu kopieren, anzupassen und den Speicherort der angepassten Datei im `style=`-Befehl anzugeben.

Standard-CSS-Dateien befinden sich unter folgendem Speicherort:

`<s7_viewers_root>/html5/FlyoutViewer.css`

Benutzerdefinierte CSS-Datei muss dieselben Klassendeklarationen enthalten wie die Standarddeklaration. Wenn eine Klassendeklaration ausgelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitstellt.

Eine alternative Möglichkeit, benutzerdefinierte CSS-Regeln bereitzustellen, besteht darin, eingebettete Stile direkt auf der Web-Seite oder in einer der verknüpften externen CSS-Regeln zu verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer `.s7flyoutviewer` Klasse seinem Container-DOM-Element zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit `style=` Befehl übergeben wird, verwenden Sie `.s7flyoutviewer` Klasse als übergeordnete Klasse in einem untergeordneten Selektor für Ihre CSS-Regeln. Wenn Sie eingebettete Stile auf der Web-Seite verwenden, qualifizieren Sie diesen Selektor auch mit einer ID des Container-DOM-Elements wie folgt:

`#<containerId>.s7flyoutviewer`

## Erstellen von responsivem CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Es ist möglich, verschiedene Geräte auszuwählen und Größen in CSS einzubetten, damit Ihre Inhalte je nach Gerät eines Benutzers oder einem bestimmten Web-Seiten-Layout unterschiedlich angezeigt werden. Diese Funktion umfasst u. a. verschiedene Web-Seiten-Layouts, Elementgrößen der Benutzeroberfläche und Bildauflösung.

Der Viewer unterstützt zwei Methoden zum Erstellen von responsivem entworfenem CSS: CSS-Markierungen und standardmäßige CSS-Medienabfragen. Sie können diese Methoden unabhängig voneinander oder gemeinsam verwenden.

**CSS-Markierungen**

Um das Erstellen von responsivem entworfenem CSS zu erleichtern, unterstützt der Viewer CSS-Markierungen, die spezielle CSS-Klassen dynamisch dem Viewer-Container-Element der obersten Ebene zugewiesen werden. Die Zuweisung basiert auf der Laufzeit-Viewer-Größe und dem auf dem aktuellen Gerät verwendeten Eingabetyp.

Die erste Gruppe von CSS-Markern umfasst `.s7size_large`-, `.s7size_medium`- und `.s7size_small`. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Das heißt, der Viewer-Bereich ist gleich oder größer als die Größe eines herkömmlichen Desktop-Monitors, `.s7size_large` verwendet wird. Wenn der Bereich ähnlich groß wie ein herkömmliches Tablet-Gerät ist, wird `.s7size_medium` zugewiesen. Für Bereiche, die Mobiltelefonbildschirmen ähnlich sind, ist `.s7size_small` festgelegt. Der primäre Zweck dieser CSS-Markierungen besteht darin, verschiedene Benutzeroberflächen-Layouts für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markern umfasst `.s7mouseinput` und `.s7touchinput`. Die Markierung `.s7touchinput` wird gesetzt, wenn das aktuelle Gerät über Touch-Eingabefunktionen verfügt; andernfalls wird `.s7mouseinput` verwendet. Diese Markierungen dienen dazu, Eingabeelemente der Benutzeroberfläche mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen zu erstellen, da normalerweise für Touch-Eingaben größere Elemente erforderlich sind. In Fällen, in denen das Gerät sowohl über Mauseingabe- als auch über Touch-Funktionen verfügt, ist `.s7touchinput` festgelegt und der Viewer rendert eine Touch-optimierte Benutzeroberfläche.

Das folgende Beispiel-CSS legt den Zoom der Schaltflächengröße auf Systemen mit Mauseingabe auf 28 x 28 Pixel und auf Touch-Geräten auf 56 x 56 Pixel fest. Darüber hinaus wird die Schaltfläche vollständig ausgeblendet, wenn die Viewer-Größe klein wird:

```
.s7flyoutviewer.s7mouseinput .s7swatches .s7thumb {  
 width: 28px; 
 height: 28px; 
} 
.s7flyoutviewer.s7touchinput .s7swatches .s7thumb {  
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer.s7size_small .s7swatches {  
 visibility: hidden; 
}
```

Verwenden Sie CSS-Medienabfragen, um Geräte mit einer anderen Pixeldichte auszuwählen. Der folgende Medienabfrageblock würde CSS enthalten, das für Bildschirme mit hoher Dichte spezifisch ist:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Die Verwendung von CSS-Markern ist die flexibelste Methode zum Erstellen von responsivem entworfenem CSS. Der Grund dafür ist, dass Sie damit nicht nur die Bildschirmgröße des Geräts, sondern auch die tatsächliche Viewer-Größe auswählen können, was für responsive Web-Seiten-Layouts nützlich sein kann.

**CSS-Medienabfragen**

Die Geräteerkennung kann auch mit reinen CSS-Medienabfragen durchgeführt werden. Alles, was in einem bestimmten Medienabfrageblock eingeschlossen ist, wird nur angewendet, wenn es auf einem entsprechenden Gerät ausgeführt wird.

Verwenden Sie bei der Anwendung auf mobile Viewer vier CSS-Medienabfragen, die in Ihrer CSS-Datei in der folgenden Reihenfolge definiert sind:

1. Enthält nur für alle Touch-Geräte spezifische Regeln.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. Enthält nur Regeln, die speziell für Tablets mit hochauflösenden Bildschirmen gelten.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Enthält nur für alle Mobiltelefone spezifische Regeln.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Enthält nur Regeln, die speziell für Mobiltelefone mit hochauflösenden Bildschirmen gelten.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Mithilfe eines Ansatzes für Medienabfragen sollten Sie CSS mit Device Sensing wie folgt organisieren:

* Zunächst werden im Desktop-spezifischen Abschnitt alle Eigenschaften definiert, die entweder Desktop-spezifisch sind oder für alle Bildschirme gelten.
* Zweitens werden die vier Medienabfragen in der oben definierten Reihenfolge ausgeführt und bieten CSS-Regeln, die für den entsprechenden Gerätetyp spezifisch sind.

Es ist nicht erforderlich, in jeder Medienabfrage das gesamte Viewer-CSS zu duplizieren. Nur Eigenschaften, die für bestimmte Geräte spezifisch sind, werden in einer Medienabfrage neu definiert.

## CSS-Sprites {#section-0711ece44a4740168cfd7624c9010bd1}

Viele Elemente der Viewer-Benutzeroberfläche werden mit Bitmap-Grafiken formatiert und weisen mehr als einen eindeutigen visuellen Status auf. Ein gutes Beispiel ist eine Schaltfläche, die normalerweise mindestens drei verschiedene Status hat: „oben“, „vorbei“ und „unten“. Jedem Status muss ein eigenes Bitmap-Bildmaterial zugewiesen werden.

Bei einem klassischen Stilansatz hätte das CSS für jeden Status des Benutzeroberflächenelements einen separaten Verweis auf eine einzelne Bilddatei auf dem Server. Im Folgenden finden Sie ein Beispiel-CSS für die Formatierung der Bildlaufschaltfläche:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-image:url(images/v2/ScrollLeftButton_up.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-image:url(images/v2/ScrollLeftButton_down.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-image:url(images/v2/ScrollLeftButton_disabled.png);  
}
```

Der Nachteil dieses Ansatzes besteht darin, dass die Endbenutzerin bzw. der Endbenutzer flackert oder eine verzögerte Antwort der Benutzeroberfläche erfährt, wenn das Element zum ersten Mal interagiert wird. Diese Aktion tritt auf, weil das Bildmaterial für den neuen Elementstatus noch nicht heruntergeladen wurde. Außerdem kann dieser Ansatz leichte negative Auswirkungen auf die Leistung haben, da die Anzahl der HTTP-Aufrufe an den Server zunimmt.

CSS-Sprites sind ein anderer Ansatz, bei dem Bildgrafiken für alle Elementstatus in einer einzigen PNG-Datei namens „Sprite“ zusammengefasst werden. Ein solches „Sprite“ weist alle visuellen Zustände für das angegebene Element nacheinander auf. Beim Formatieren eines Elements der Benutzeroberfläche mit Sprites wird für alle verschiedenen Status in CSS auf dasselbe Sprite-Bild verwiesen. Außerdem wird die `background-position`-Eigenschaft für jeden Status verwendet, um anzugeben, welcher Teil des „Sprite“-Bildes verwendet wird. Sie können ein „Sprite“-Bild auf jede geeignete Weise strukturieren. Betrachter haben sie normalerweise vertikal gestapelt. Nachfolgend finden Sie ein Beispiel für die Gestaltung derselben Scroll-Schaltfläche von oben nach dem Sprite-Prinzip:

```
.s7flyoutviewer .s7scrollleftbutton[state]  { 
    background-image: url(images/v2/ScrollLeftButton_light_sprite.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-position: -56px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-position: -0px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-position: -56px -448px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-position: -0px -448px;  
}
```

## Allgemeine Hinweise und Hinweise zu Stilen {#section-95855dccbbc444e79970f1aaa3260b7b}

* Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung der `!IMPORTANT`-Regel nicht unterstützt, um Viewer-Elemente zu gestalten. Insbesondere sollte `!IMPORTANT` Regel nicht verwendet werden, um Standard- oder Laufzeitstile zu überschreiben, die vom Viewer oder Viewer-SDK bereitgestellt werden. Der Grund dafür ist, dass dies das Verhalten der richtigen Komponenten beeinträchtigen kann. Stattdessen sollten Sie CSS-Selektoren mit der richtigen Spezifität verwenden, um CSS-Eigenschaften festzulegen, die in diesem Referenzhandbuch dokumentiert sind.
* Alle Pfade zu externen Assets innerhalb von CSS werden gegen den CSS-Speicherort aufgelöst, nicht gegen den HTML-Seitenspeicherort des Viewers. Beachten Sie diese Regel, wenn Sie das Standard-CSS an einen anderen Speicherort kopieren. Kopieren Sie entweder die Standard-Assets oder aktualisieren Sie die Pfade innerhalb des benutzerdefinierten CSS.
* Das bevorzugte Format für Bitmap-Grafiken ist PNG.
* Bitmap-Grafiken werden Benutzeroberflächenelementen mithilfe der `background-image`-Eigenschaft zugewiesen.
* Die `width`- und `height` eines Benutzeroberflächenelements definieren dessen logische Größe. Die Größe der an `background-image` übergebenen Bitmap hat keine Auswirkungen auf die logische Größe.
* Um die hohe Pixeldichte hochauflösender Bildschirme wie Retina zu verwenden, geben Sie Bitmap-Grafiken doppelt so groß wie die Elementgröße der logischen Benutzeroberfläche an. Wenden Sie dann die Eigenschaft `-webkit-background-size:contain` an, um den Hintergrund auf die Elementgröße der logischen Benutzeroberfläche herunterzuskalieren.
* Um eine Schaltfläche aus der Benutzeroberfläche zu entfernen, fügen Sie `display:none` zu ihrer CSS-Klasse hinzu.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Sie Transparenz benötigen, verwenden Sie das Format `rgba(R,G,B,A)`. Andernfalls können Sie das Format `#RRGGBB` verwenden.

## Allgemeine Elemente der Benutzeroberfläche {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Im Folgenden finden Sie die Referenzdokumentation zu Benutzeroberflächenelementen, die für den Flyout-Viewer gilt:

* [Flyout-Zoomansicht](r-html5-flyout-viewer-20-customize-flyoutzoomview.md)
* [Fokushervorhebung](r-html5-flyout-viewer-20-customize-focushighlight.md)
* [Haupt-Viewer-Bereich](r-html5-flyout-viewer-20-customize-mainviewerarea.md)
* [Farbfelder](r-html5-flyout-viewer-20-customize-swatches.md)
* [QuickInfos](r-html5-flyout-viewer-20-customize-tooltips.md)
