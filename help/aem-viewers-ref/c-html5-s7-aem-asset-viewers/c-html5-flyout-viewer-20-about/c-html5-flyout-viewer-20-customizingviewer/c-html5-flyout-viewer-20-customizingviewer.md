---
title: Anpassen des Flyout-Viewers
description: Anpassen des Flyout-Viewers
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b7898044-5178-4cdf-ab52-9996a61a3a35
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Anpassen des Flyout-Viewers{#customizing-flyout-viewer}

Alle visuellen Anpassungen und die meisten Verhaltensanpassungen werden durch die Erstellung eines benutzerdefinierten CSS vorgenommen.

Der vorgeschlagene Workflow besteht darin, die Standard-CSS-Datei für den entsprechenden Viewer zu übernehmen, sie an einen anderen Speicherort zu kopieren, sie anzupassen und den Speicherort der angepassten Datei im `style=` Befehl.

Standard-CSS-Dateien finden Sie unter folgendem Speicherort:

`<s7_viewers_root>/html5/FlyoutViewer.css`

Benutzerdefinierte CSS-Dateien müssen dieselben Klassendeklarationen wie die Standarddeklaration enthalten. Wenn eine Klassendeklaration weggelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitstellt.

Alternativ können Sie benutzerdefinierte CSS-Regeln bereitstellen, indem Sie eingebettete Stile direkt auf der Webseite oder in einer verknüpften externen CSS-Regel verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer `.s7flyoutviewer` -Klasse zu ihrem Container-DOM-Element hinzu. Wenn Sie eine externe CSS-Datei verwenden, die mit `style=` Befehl, verwenden `.s7flyoutviewer` -Klasse als übergeordnete Klasse im untergeordneten Selektor für Ihre CSS-Regeln. Wenn Sie eingebettete Stile auf der Web-Seite verwenden, qualifizieren Sie diesen Selektor wie folgt mit einer ID des Container-DOM-Elements:

`#<containerId>.s7flyoutviewer`

## Erstellen von responsiv gestaltetem CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Es ist möglich, verschiedene Geräte anzusprechen und Größen in CSS einzubetten, damit Ihre Inhalte je nach Gerät eines Benutzers oder Layout einer bestimmten Webseite unterschiedlich angezeigt werden. Diese Funktion umfasst, aber nicht ausschließlich, verschiedene Webseitenlayouts, Elementgrößen der Benutzeroberfläche und die Auflösung von Grafiken.

Der Viewer unterstützt zwei Methoden zum Erstellen von responsivem entworfenem CSS: CSS-Markierungen und Standard-CSS-Medienabfragen. Sie können diese Methoden unabhängig oder gemeinsam verwenden.

**CSS-Markierungen**

Um responsives CSS zu erstellen, unterstützt der Viewer CSS-Markierungen, die spezielle CSS-Klassen enthalten, die dynamisch dem Viewer-Container-Element der obersten Ebene zugewiesen werden. Die Zuweisung basiert auf der Laufzeit-Viewer-Größe und dem Eingabetyp, der auf dem aktuellen Gerät verwendet wird.

Die erste Gruppe von CSS-Markern umfasst `.s7size_large`, `.s7size_medium`und `.s7size_small` Klassen. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Das heißt, wenn der Viewer-Bereich gleich oder größer als die Größe eines gemeinsamen Desktop-Monitors ist `.s7size_large` verwendet wird; wenn der Bereich nahe an einem gemeinsamen Tablet-Gerät liegt `.s7size_medium` zugewiesen wurde. In Bereichen, die Mobiltelefonbildschirmen ähneln, `.s7size_small` festgelegt ist. Der Hauptzweck dieser CSS-Markierungen besteht darin, verschiedene Benutzeroberflächen-Layouts für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markern umfasst `.s7mouseinput` und `.s7touchinput`. Die Markierung `.s7touchinput` festgelegt ist, wenn das aktuelle Gerät über Touch-Eingabefunktionen verfügt; andernfalls `.s7mouseinput` verwendet. Diese Markierungen dienen zur Erstellung von Eingabeelementen der Benutzeroberfläche mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen, da Touch-Eingaben normalerweise größere Elemente erfordern. In Fällen, in denen das Gerät sowohl über Maus- als auch Touch-Funktionen verfügt `.s7touchinput` festgelegt ist und der Viewer eine Touch-optimierte Benutzeroberfläche rendert.

Im folgenden Beispiel-CSS wird die Größe der Zoom-Schaltfläche auf 28 x 28 Pixel bei Systemen mit Mauseingabe und auf Touch-Geräten auf 56 x 56 Pixel eingestellt. Darüber hinaus wird die Schaltfläche vollständig ausgeblendet, wenn die Viewer-Größe klein wird:

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

Verwenden Sie CSS-Medienabfragen, um Geräte mit einer anderen Pixeldichte als Ziel auszuwählen. Der folgende Medienabfrageblock enthält CSS, das speziell für High-Density-Screens geeignet ist:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Die Verwendung von CSS-Markern ist die flexibelste Methode zum Erstellen von responsiv gestaltetem CSS. Der Grund dafür ist, dass Sie damit nicht nur die Bildschirmgröße des Geräts, sondern auch die tatsächliche Viewer-Größe bestimmen können, was für responsive Webseitenlayouts nützlich sein kann.

**CSS-Medienabfragen**

Die Geräteerkennung kann auch mit reinen CSS-Medienabfragen durchgeführt werden. Alles, was in einem bestimmten Medienabfrageblock eingeschlossen ist, wird nur angewendet, wenn er auf einem entsprechenden Gerät ausgeführt wird.

Verwenden Sie bei Anwendung auf Mobile Viewer vier CSS-Medienabfragen, die in Ihrem CSS in der folgenden Reihenfolge definiert sind:

1. Enthält nur Regeln, die für alle Touch-Geräte spezifisch sind.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. Enthält nur Regeln für Tablets mit hochauflösenden Bildschirmen.

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

1. Enthält nur Regeln für Mobiltelefone mit hochauflösenden Bildschirmen.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Mithilfe eines Medienabfrageansatzes sollten Sie CSS mit Geräteerkennung wie folgt organisieren:

* Zunächst werden im Desktop-spezifischen Abschnitt alle Eigenschaften definiert, die entweder Desktop-spezifisch oder für alle Bildschirme gemeinsam sind.
* Zweitens entsprechen die vier Medienabfragen der oben definierten Reihenfolge und enthalten CSS-Regeln, die für den entsprechenden Gerätetyp spezifisch sind.

Es ist nicht erforderlich, die gesamte Viewer-CSS in jeder Medienabfrage zu duplizieren. Innerhalb einer Medienabfrage werden nur Eigenschaften neu definiert, die für bestimmte Geräte spezifisch sind.

## CSS-Sprites {#section-0711ece44a4740168cfd7624c9010bd1}

Viele Elemente der Viewer-Benutzeroberfläche werden mit Bitmap-Grafiken formatiert und weisen mehr als einen bestimmten visuellen Status auf. Ein gutes Beispiel ist eine Schaltfläche mit normalerweise mindestens drei verschiedenen Status: &quot;up&quot;, &quot;over&quot;und &quot;down&quot;. Jeder Status erfordert eine eigene Bitmap-Grafik, die zugewiesen wird.

Bei einem klassischen Stil würde CSS für jeden Status des Benutzeroberflächenelements einen separaten Verweis auf die einzelne Bilddatei auf dem Server haben. Im Folgenden finden Sie ein Beispiel-CSS für die Formatierung der Bildlaufschaltfläche:

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

Der Nachteil dieses Ansatzes besteht darin, dass der Endbenutzer flackernde oder verzögerte Antworten auf die Benutzeroberfläche erfährt, wenn das Element zum ersten Mal mit interagiert wird. Diese Aktion tritt auf, da die Bildgrafik für den neuen Elementstatus noch nicht heruntergeladen wurde. Dieser Ansatz kann sich aufgrund der gestiegenen Anzahl an HTTP-Aufrufen an den Server auch geringfügig negativ auf die Leistung auswirken.

CSS-Sprites ist ein anderer Ansatz, bei dem Bildgrafiken für alle Elementzustände in einer PNG-Datei namens &quot;Sprite&quot;kombiniert werden. Ein solches &quot;Sprite&quot;hat alle visuellen Status für das jeweilige Element, das nacheinander positioniert wird. Beim Formatieren eines Benutzeroberflächenelements mit Sprites wird für alle verschiedenen Status in CSS auf dasselbe Sprite-Bild verwiesen. Außerdem wird die `background-position` -Eigenschaft wird für jeden Status verwendet, um anzugeben, welcher Teil des &quot;Sprite&quot;-Bildes verwendet wird. Sie können ein &quot;Sprite&quot;-Bild auf jede geeignete Weise strukturieren. Normalerweise wird sie von Viewern vertikal gestapelt. Nachfolgend finden Sie ein &quot;sprite&quot;-basiertes Beispiel für die Formatierung derselben Bildlaufschaltfläche von oben:

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

* Wenn Sie die Viewer-Benutzeroberfläche mit CSS anpassen, verwenden Sie die `!IMPORTANT` -Regel wird nicht unterstützt, um Viewer-Elemente zu formatieren. Insbesondere `!IMPORTANT` -Regel sollte nicht verwendet werden, um Standard- oder Laufzeitstile zu überschreiben, die vom Viewer- oder Viewer-SDK bereitgestellt werden. Der Grund dafür ist, dass dies das Verhalten von richtigen Komponenten beeinflussen kann. Stattdessen sollten Sie CSS-Selektoren mit der richtigen Spezifität verwenden, um CSS-Eigenschaften festzulegen, die in diesem Referenzhandbuch dokumentiert sind.
* Alle Pfade zu externen Assets innerhalb von CSS werden mit dem CSS-Speicherort aufgelöst, nicht mit dem Viewer-HTML-Seitenspeicherort. Beachten Sie diese Regel, wenn Sie die Standard-CSS an einen anderen Speicherort kopieren. Kopieren Sie entweder die standardmäßigen Assets sowie oder aktualisieren Sie Pfade innerhalb des benutzerdefinierten CSS.
* Das bevorzugte Format für Bitmap-Grafiken ist PNG.
* Bitmap-Grafiken werden den Elementen der Benutzeroberfläche mithilfe der `background-image` -Eigenschaft.
* Die `width` und `height` -Eigenschaften eines Benutzeroberflächenelements definieren die logische Größe. Die Größe der Bitmap, die an `background-image` hat keine Auswirkungen auf die logische Größe.
* Um die hohe Pixeldichte von hochauflösenden Bildschirmen wie Retina zu verwenden, geben Sie Bitmap-Grafiken doppelt so groß an wie die Elementgröße der logischen Benutzeroberfläche. Wenden Sie dann die `-webkit-background-size:contain` -Eigenschaft, um den Hintergrund auf die Elementgröße der logischen Benutzeroberfläche herunterzuskalieren.
* Um eine Schaltfläche aus der Benutzeroberfläche zu entfernen, fügen Sie `display:none` zu seiner CSS-Klasse hinzu.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Sie Transparenz benötigen, verwenden Sie das Format `rgba(R,G,B,A)`. Andernfalls können Sie das Format `#RRGGBB`.

## Allgemeine Benutzeroberflächen-Elemente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Im Folgenden finden Sie die Referenzdokumentation zu Elementen der Benutzeroberfläche, die für den Flyout-Viewer gilt:

* [Flyout-Zoom-Ansicht](r-html5-flyout-viewer-20-customize-flyoutzoomview.md)
* [Fokushervorhebung](r-html5-flyout-viewer-20-customize-focushighlight.md)
* [Hauptanzeige-Bereich](r-html5-flyout-viewer-20-customize-mainviewerarea.md)
* [Muster](r-html5-flyout-viewer-20-customize-swatches.md)
* [QuickInfos](r-html5-flyout-viewer-20-customize-tooltips.md)
