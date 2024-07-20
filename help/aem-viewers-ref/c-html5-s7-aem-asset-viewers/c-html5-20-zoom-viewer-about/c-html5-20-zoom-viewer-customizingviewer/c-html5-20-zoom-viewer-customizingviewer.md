---
title: Zoom-Viewer anpassen
description: Die visuelle Anpassung und die meisten Verhaltensanpassungen für den Zoom-Viewer erfolgen durch Erstellen eines benutzerdefinierten CSS.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 336bf68c-6110-4ce8-85b4-28d7397044c2
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 0%

---

# Zoom-Viewer anpassen{#customizing-zoom-viewer}

Die visuelle Anpassung und die meisten Verhaltensanpassungen für den Zoom-Viewer erfolgen durch Erstellen eines benutzerdefinierten CSS.

Der vorgeschlagene Workflow besteht darin, die Standard-CSS-Datei für den entsprechenden Viewer zu übernehmen, sie an einen anderen Speicherort zu kopieren, sie anzupassen und den Speicherort der angepassten Datei im Befehl `style=` anzugeben.

Standard-CSS-Dateien finden Sie unter folgendem Speicherort:

`<s7_viewers_root>/html5/ZoomViewer_light.css`

Der Viewer wird mit zwei nativen CSS-Dateien für helle und dunkle Farbschemata geliefert. Die &quot;helle&quot;Version wird standardmäßig verwendet, Sie können jedoch mithilfe des folgenden Standard-CSS zur &quot;dunklen&quot;Version wechseln:

`<s7_viewers_root>/html5/ZoomViewer_dark.css`

Benutzerdefinierte CSS-Dateien müssen dieselben Klassendeklarationen wie die Standarddeklaration enthalten. Wenn eine Klassendeklaration weggelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitstellt.

Alternativ können Sie benutzerdefinierte CSS-Regeln bereitstellen, indem Sie eingebettete Stile direkt auf der Webseite oder in einer verknüpften externen CSS-Regel verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer dem Container-DOM-Element die Klasse `.s7zoomviewer` zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit dem Befehl `style=` übergeben wird, verwenden Sie die Klasse `.s7zoomviewer` als übergeordnete Klasse in der untergeordneten Auswahl für Ihre CSS-Regeln. Wenn Sie eingebettete Stile auf der Web-Seite verwenden, qualifizieren Sie diesen Selektor wie folgt mit einer ID des Container-DOM-Elements:

`#<containerId>.s7zoomviewer`

## Erstellen von responsiv gestaltetem CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

Es ist möglich, verschiedene Geräte anzusprechen und die Größe in CSS einzubetten, damit Ihre Inhalte je nach Gerät eines Benutzers oder Webseitenlayout unterschiedlich angezeigt werden. Dieses Targeting umfasst verschiedene Layouts, die Elementgrößen der Benutzeroberfläche und die Auflösung von Grafiken, ist jedoch nicht darauf beschränkt.

Der Viewer unterstützt zwei Möglichkeiten zum Erstellen von responsiv gestaltetem CSS: CSS-Markierungen und Standard-CSS-Medienabfragen. Sie können diese Mechanismen unabhängig oder gemeinsam verwenden.

**CSS-Markierungen**

Um das Erstellen von responsiv entworfenen CSS zu unterstützen, unterstützt der Viewer CSS-Markierungen. Diese Markierungen sind spezielle CSS-Klassen. Diese Klassen werden dem Viewer-Container-Element der obersten Ebene dynamisch basierend auf der Laufzeit-Viewer-Größe und dem Eingabetyp zugewiesen, der auf dem aktuellen Gerät verwendet wird.

Die erste Gruppe von CSS-Markern umfasst die Klassen `.s7size_large`, `.s7size_medium` und `.s7size_small`. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Wenn der Viewer-Bereich gleich oder größer als die Größe eines allgemeinen Desktop-Monitors ist, wird `.s7size_large` verwendet. Wenn der Bereich nahe an einem gemeinsamen Tablet-Gerät liegt, wird `.s7size_medium` zugewiesen. Für Bereiche, die ähnlich wie Mobiltelefonbildschirme sind, ist `.s7size_small` eingestellt. Der Hauptzweck dieser CSS-Markierungen besteht darin, verschiedene Benutzeroberflächen-Layouts für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markern enthält `.s7mouseinput` und `.s7touchinput`. Die Markierung `.s7touchinput` wird gesetzt, wenn das aktuelle Gerät Touch-Eingabefunktionen aufweist. Andernfalls wird `.s7mouseinput` verwendet. Diese Markierungen dienen hauptsächlich dazu, Benutzeroberflächen-Eingabeelemente mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen zu erstellen, da Touch-Eingaben normalerweise größere Elemente erfordern. Falls das Gerät sowohl über eine Maus- als auch Touch-Funktion verfügt, wird `.s7touchinput` eingestellt und der Viewer rendert eine Touch-optimierte Benutzeroberfläche.

Im folgenden Beispiel-CSS wird die Größe der Zoom-Schaltfläche auf 28 x 28 Pixel bei Systemen mit Mauseingabe und auf Touch-Geräten auf 56 x 56 Pixel eingestellt. Darüber hinaus wird die Schaltfläche vollständig ausgeblendet, wenn die Viewer-Größe zu klein wird:

```
.s7zoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7zoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7zoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Um Geräte mit unterschiedlicher Pixeldichte als Ziel festzulegen, müssen Sie CSS-Medienabfragen verwenden. Der folgende Medienabfrageblock würde CSS-spezifische Daten für Bildschirme mit hoher Dichte enthalten:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Die Verwendung von CSS-Markierungen ist die flexibelste Methode zum Erstellen von responsiv gestaltetem CSS, da Sie damit nicht nur die Bildschirmgröße des Geräts, sondern auch die tatsächliche Viewer-Größe bestimmen können, was für responsive Designlayouts nützlich ist.

Sie können die standardmäßige Viewer-CSS-Datei als Beispiel für einen CSS-Marker-Ansatz verwenden.

**CSS-Medienabfragen**

Sie können die Geräteerkennung auch mit reinen CSS-Medienabfragen durchführen. Alles, was in einem bestimmten Medienabfrageblock eingeschlossen ist, wird nur angewendet, wenn er auf einem entsprechenden Gerät ausgeführt wird.

Wenn Sie auf Mobile Viewer angewendet werden, verwenden Sie vier CSS-Medienabfragen, die in Ihrem CSS definiert sind, in der unten aufgeführten Reihenfolge:

1. Enthält nur für alle Touch-Geräte spezifische Regeln.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
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

## CSS-Sprites {#section-9b6d8d601cb441d08214dada7bb4eddc}

Viele Elemente der Viewer-Benutzeroberfläche werden mit Bitmap-Grafiken formatiert und weisen mehr als einen bestimmten visuellen Status auf. Ein gutes Beispiel ist eine Schaltfläche mit normalerweise mindestens drei verschiedenen Status: &quot;up&quot;, &quot;over&quot;und &quot;down&quot;. Jeder Status erfordert eine eigene Bitmap-Grafik, die zugewiesen wird.

Bei einem klassischen Stil würde CSS für jeden Status des Benutzeroberflächenelements einen separaten Verweis auf die einzelne Bilddatei auf dem Server haben. Im Folgenden finden Sie ein Beispiel-CSS für die Formatierung der Zoom-in-Schaltfläche:

```
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Der Nachteil dieses Ansatzes besteht darin, dass der Endbenutzer flackernde oder verzögerte Antworten auf die Benutzeroberfläche erfährt, wenn das Element zum ersten Mal verwendet wird. Diese Aktion tritt auf, da die Bildgrafik für den neuen Elementstatus noch nicht heruntergeladen wurde. Dieser Ansatz kann sich aufgrund der gestiegenen Anzahl an HTTP-Aufrufen an den Server auch geringfügig negativ auf die Leistung auswirken.

CSS-Sprites ist ein anderer Ansatz, bei dem Bildgrafiken für alle Elementzustände in einer PNG-Datei namens &quot;Sprite&quot;kombiniert werden. Ein solches &quot;Sprite&quot;hat alle visuellen Status für das jeweilige Element, das nacheinander positioniert wird. Beim Formatieren eines Benutzeroberflächenelements mit Sprites wird für alle verschiedenen Status in CSS auf dasselbe Sprite-Bild verwiesen. Außerdem wird mit der Eigenschaft &quot;`background-position`&quot;für jeden Status angegeben, welcher Teil des &quot;Sprite&quot;-Bildes verwendet wird. Sie können ein &quot;Sprite&quot;-Bild auf jede geeignete Weise strukturieren. Normalerweise wird sie von Viewern vertikal gestapelt. Nachfolgend finden Sie ein &quot;sprite&quot;-basiertes Beispiel für die Formatierung der gleichen Zoom-in-Schaltfläche von oben:

```
.s7zoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Allgemeine Hinweise und Hinweise zu Stilen {#section-95855dccbbc444e79970f1aaa3260b7b}

* Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung der `!IMPORTANT` -Regel nicht unterstützt, um Viewer-Elemente zu formatieren. Insbesondere sollte die Regel `!IMPORTANT` nicht verwendet werden, um Standard- oder Laufzeitstile zu überschreiben, die vom Viewer- oder Viewer-SDK bereitgestellt werden. Der Grund dafür ist, dass dies das Verhalten von richtigen Komponenten beeinflussen kann. Stattdessen sollten Sie CSS-Selektoren mit der richtigen Spezifität verwenden, um CSS-Eigenschaften festzulegen, die in diesem Referenzhandbuch dokumentiert sind.
* Alle Pfade zu externen Assets innerhalb von CSS werden mit dem CSS-Speicherort aufgelöst, nicht mit dem Viewer-HTML-Seitenspeicherort. Beachten Sie diese Regel, wenn Sie die Standard-CSS an einen anderen Speicherort kopieren. Kopieren Sie entweder die standardmäßigen Assets sowie oder aktualisieren Sie Pfade innerhalb des benutzerdefinierten CSS.
* Das bevorzugte Format für Bitmap-Grafiken ist PNG.
* Bitmap-Grafiken werden Elementen der Benutzeroberfläche mithilfe der Eigenschaft `background-image` zugewiesen.
* Die Eigenschaften `width` und `height` eines Benutzeroberflächenelements definieren seine logische Größe. Die Größe der an `background-image` übergebenen Bitmap wirkt sich nicht auf die logische Größe aus.
* Um die hohe Pixeldichte von hochauflösenden Bildschirmen wie Retina zu verwenden, geben Sie Bitmap-Grafiken doppelt so groß an wie die Elementgröße der logischen Benutzeroberfläche. Wenden Sie dann die Eigenschaft `-webkit-background-size:contain` an, um den Hintergrund auf die Elementgröße der logischen Benutzeroberfläche herunterzuskalieren.
* Um eine Schaltfläche aus der Benutzeroberfläche zu entfernen, fügen Sie `display:none` zur CSS-Klasse hinzu.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Sie Transparenz benötigen, verwenden Sie das Format `rgba(R,G,B,A)`. Andernfalls können Sie das Format `#RRGGBB` verwenden.

## Allgemeine Benutzeroberflächen-Elemente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Im Folgenden finden Sie die Referenzdokumentation zu Elementen der Benutzeroberfläche, die für den Video-Viewer gilt:
