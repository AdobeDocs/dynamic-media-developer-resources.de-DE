---
title: Anpassen des interaktiven Bild-Viewers
description: Die gesamte visuelle Anpassung und die meisten Verhaltensanpassungen für den interaktiven Bild-Viewer werden durch die Erstellung eines benutzerdefinierten CSS vorgenommen.
keywords: Responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: bb3cfe4a-ec60-4c10-82fe-9e4f8f7c586f
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '1287'
ht-degree: 0%

---

# Anpassen des interaktiven Bild-Viewers{#customizing-interactive-image-viewer}

Die gesamte visuelle Anpassung und die meisten Verhaltensanpassungen für den interaktiven Bild-Viewer werden durch die Erstellung eines benutzerdefinierten CSS vorgenommen.

Der vorgeschlagene Workflow besteht darin, die standardmäßige CSS-Datei für den entsprechenden Viewer zu verwenden, sie an einen anderen Speicherort zu kopieren, anzupassen und den Speicherort der angepassten Datei im `style=`-Befehl anzugeben.

Standard-CSS-Dateien befinden sich unter folgendem Speicherort:

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/InteractiveImage.css`

Benutzerdefinierte CSS-Datei muss dieselben Klassendeklarationen enthalten wie die Standarddeklaration. Wenn eine Klassendeklaration ausgelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitstellt.

Eine alternative Möglichkeit, benutzerdefinierte CSS-Regeln bereitzustellen, besteht darin, eingebettete Stile direkt auf der Web-Seite oder in einer der verknüpften externen CSS-Regeln zu verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer `.s7interactiveimage` Klasse seinem Container-DOM-Element zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit dem `style=`-Befehl übergeben wird, verwenden Sie `.s7interactiveimage` -Klasse als übergeordnete Klasse in einem untergeordneten Selektor für Ihre CSS-Regeln. Wenn Sie der Web-Seite eingebettete Stile hinzufügen, qualifizieren Sie diesen Selektor auch mit einer ID des Container-DOM-Elements wie folgt:

`#<containerId>.s7interactiveimage`

## Erstellen von responsivem CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

Es ist möglich, verschiedene Geräte auszuwählen und Größen in CSS einzubetten, damit Ihre Inhalte je nach Gerät eines Benutzers oder einem bestimmten Web-Seiten-Layout unterschiedlich angezeigt werden. Diese Technik umfasst u. a. verschiedene Layouts, Elementgrößen der Benutzeroberfläche und Bildauflösung.

Der Viewer unterstützt zwei Mechanismen zum Erstellen von responsivem entworfenem CSS: CSS-Markierungen und standardmäßige CSS-Medienabfragen. Sie können diese Markierungen oder Abfragen unabhängig voneinander oder zusammen verwenden.

**CSS-Markierungen**

Um das Erstellen von responsivem entworfenem CSS zu erleichtern, unterstützt der Viewer CSS-Markierungen. Diese Markierungen sind spezielle CSS-Klassen, die dem Container-Element der obersten Ebene dynamisch zugewiesen werden. Sie basieren auf der Viewer-Größe zur Laufzeit und dem auf dem aktuellen Gerät verwendeten Eingabetyp.

Die erste Gruppe von CSS-Markern enthält `.s7size_large`-, `.s7size_medium`- und `.s7size_small`. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Wenn der Viewer-Bereich beispielsweise so groß oder gleich wie ein normaler Desktop-Monitor ist, verwenden Sie `.s7size_large`. Wenn sich der Bereich in der Nähe eines allgemeinen Tablet-Geräts befindet, weisen Sie `.s7size_medium` zu. Verwenden Sie für Bereiche, die Mobiltelefonbildschirmen ähneln, `.s7size_small`. Der primäre Zweck dieser CSS-Markierungen besteht darin, verschiedene Benutzeroberflächen-Layouts für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markern enthält `.s7mouseinput` und `.s7touchinput`. Die CSS-`.s7touchinput` wird festgelegt, wenn das aktuelle Gerät über eine Touch-Eingabe verfügt. Andernfalls wird `.s7mouseinput` verwendet. Diese Markierungen sind hauptsächlich dazu gedacht, Benutzeroberflächen-Eingabeelemente mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen zu erstellen, da normalerweise für Touch-Eingaben größere Elemente erforderlich sind.

Im folgenden Beispiel-CSS wird der Zoom der Schaltflächengröße auf Systemen mit Mauseingabe auf 28 x 28 Pixel und auf Touch-Eingabegeräten auf 56 x 56 Pixel eingestellt. Wenn der Viewer noch kleiner ist, wird er auf 20 x 20 Pixel eingestellt.

```
.s7interactiveimage.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7interactiveimage.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7interactiveimage.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

Um Geräte mit unterschiedlicher Pixeldichte anzusprechen, müssen Sie CSS-Medienabfragen verwenden. Der folgende Medienabfrageblock würde CSS-spezifische Elemente für Bildschirme mit hoher Dichte enthalten:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Die Verwendung von CSS-Markern ist die flexibelste Methode zum Erstellen von responsivem entworfenem CSS, da Sie damit nicht nur die Bildschirmgröße des Geräts, sondern auch die tatsächliche Viewer-Größe auswählen können, was für responsive Design-Layouts nützlich ist.

Sie können die standardmäßige Viewer-CSS-Datei als Beispiel für einen Ansatz mit CSS-Markern verwenden.

**CSS-Medienabfragen**

Sie können die Geräteerkennung auch durchführen, indem Sie reine CSS-Medienabfragen verwenden. Alles, was in einem bestimmten Medienabfrageblock eingeschlossen ist, wird nur angewendet, wenn es auf einem entsprechenden Gerät ausgeführt wird.

Bei der Anwendung auf mobile Viewer verwenden Sie vier CSS-Medienabfragen, die in Ihrem CSS definiert sind, in der unten aufgeführten Reihenfolge:

1. Enthält nur für alle Touch-Geräte spezifische Regeln.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
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

## CSS-Sprites {#section-9b6d8d601cb441d08214dada7bb4eddc}

Viele Elemente der Viewer-Benutzeroberfläche werden mit Bitmap-Grafiken formatiert und weisen mehr als einen eindeutigen visuellen Status auf. Ein gutes Beispiel ist eine Schaltfläche, die normalerweise mindestens drei verschiedene Status aufweist: `up`, `over` und `down`. Jedem Status muss ein eigenes Bitmap-Bildmaterial zugewiesen werden.

Bei einem klassischen Ansatz für die Formatierung hätte das CSS für jeden Status des Benutzeroberflächenelements einen separaten Verweis auf die einzelne Bilddatei auf dem Server. Im Folgenden finden Sie ein Beispiel für die CSS-Formatierung einer Zoom-In-Schaltfläche:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

Der Nachteil dieses Ansatzes besteht darin, dass die Endbenutzerin bzw. der Endbenutzer flackert oder eine verzögerte Antwort der Benutzeroberfläche erfährt, wenn das Element zum ersten Mal interagiert wird. Diese Aktion tritt auf, weil das Bildmaterial für den neuen Elementstatus noch nicht heruntergeladen wurde. Außerdem kann dieser Ansatz leichte negative Auswirkungen auf die Leistung haben, da die Anzahl der HTTP-Aufrufe an den Server zunimmt.

CSS-Sprites sind ein anderer Ansatz, bei dem Bildgrafiken für alle Elementstatus in einer einzigen PNG-Datei namens „Sprite“ zusammengefasst werden. Ein solches „Sprite“ weist alle visuellen Zustände für das angegebene Element nacheinander auf. Beim Formatieren eines Elements der Benutzeroberfläche mit Sprites wird für alle verschiedenen Status in CSS auf dasselbe Sprite-Bild verwiesen. Außerdem wird die `background-position`-Eigenschaft für jeden Status verwendet, um anzugeben, welcher Teil des „Sprite“-Bildes verwendet wird. Sie können ein „Sprite“-Bild auf jede geeignete Weise strukturieren. Betrachter haben sie normalerweise vertikal gestapelt.

Im Folgenden finden Sie ein „Sprite“-basiertes Beispiel für die Formatierung derselben Zoom-In-Schaltfläche zuvor:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Allgemeine Hinweise und Hinweise zu Stilen {#section-95855dccbbc444e79970f1aaa3260b7b}

* Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung der `!IMPORTANT`-Regel nicht unterstützt, um Viewer-Elemente zu gestalten. Insbesondere sollte `!IMPORTANT` Regel nicht verwendet werden, um Standard- oder Laufzeitstile zu überschreiben, die vom Viewer oder Viewer-SDK bereitgestellt werden. Dies liegt daran, dass sich dies auf das Verhalten der richtigen Komponenten auswirken kann. Stattdessen sollten Sie CSS-Selektoren mit der richtigen Spezifität verwenden, um CSS-Eigenschaften festzulegen, die in diesem Viewers-Referenzhandbuch dokumentiert sind.
* Alle Pfade zu externen Assets innerhalb von CSS werden gegen den CSS-Speicherort aufgelöst, nicht gegen den HTML-Seitenspeicherort des Viewers. Beachten Sie diese Regel, wenn Sie das Standard-CSS an einen anderen Speicherort kopieren. Kopieren Sie entweder die Standard-Assets oder aktualisieren Sie alle Pfade in der benutzerdefinierten CSS-Datei.
* Das bevorzugte Format für Bitmap-Grafiken ist PNG.
* Bitmap-Grafiken werden Benutzeroberflächenelementen mithilfe der `background-image`-Eigenschaft zugewiesen.
* Die `width`- und `height` eines Benutzeroberflächenelements definieren dessen logische Größe. Die Größe der an `background-image` übergebenen Bitmap hat keine Auswirkungen auf die logische Größe.
* Um die hohe Pixeldichte hochauflösender Bildschirme wie Retina zu verwenden, geben Sie Bitmap-Grafiken doppelt so groß wie die Elementgröße der logischen Benutzeroberfläche an. Wenden Sie dann die Eigenschaft `-webkit-background-size:contain` an, um den Hintergrund auf die Elementgröße der logischen Benutzeroberfläche herunterzuskalieren.
* Um eine Schaltfläche aus der Benutzeroberfläche zu entfernen, fügen Sie `display:none` zu ihrer CSS-Klasse hinzu.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Sie Transparenz benötigen, verwenden Sie das Format `rgba(R,G,B,A)`. Andernfalls können Sie das Format `#RRGGBB` verwenden.

## Allgemeine Elemente der Benutzeroberfläche {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Im Folgenden finden Sie die Referenzdokumentation zu Benutzeroberflächenelementen, die für den Videobild-Viewer gilt:
