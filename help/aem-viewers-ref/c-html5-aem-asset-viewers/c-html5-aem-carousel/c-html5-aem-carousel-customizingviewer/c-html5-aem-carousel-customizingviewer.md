---
title: Anpassen des Karussellanzeige
description: Die visuelle Anpassung und die meisten Verhaltensanpassungen für den Karussell-Viewer erfolgen durch Erstellen eines benutzerdefinierten CSS.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f392d830-5c75-45dd-bab8-29a38218790d
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 0%

---

# Anpassen des Karussellanzeige{#customizing-carousel-viewer}

Die visuelle Anpassung und die meisten Verhaltensanpassungen für den Karussell-Viewer erfolgen durch Erstellen eines benutzerdefinierten CSS.

Der vorgeschlagene Workflow besteht darin, die Standard-CSS-Datei für den entsprechenden Viewer zu übernehmen, sie an einen anderen Speicherort zu kopieren, sie anzupassen und den Speicherort der angepassten Datei im Befehl `style=` anzugeben.

Standard-CSS-Dateien finden Sie unter folgendem Speicherort:

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

Der Viewer wird mit vier nativen CSS-Dateien für numerische und gepunktete Set-Indikatoren geliefert, die jeweils ein helles und dunkles Farbschema aufweisen. Die Version &quot;Gepunktetes Licht&quot;wird standardmäßig verwendet, aber es ist einfach, zu einer anderen Version zu wechseln, indem Sie unterschiedliche Standard-CSS verwenden und den Parameter `SetIndicator.mode` festlegen. Andere standardmäßige CSS-Dateien finden Sie an folgendem Speicherort:

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

Benutzerdefinierte CSS-Dateien müssen dieselben Klassendeklarationen wie die Standarddeklaration enthalten. Wenn eine Klassendeklaration weggelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitstellt.

Eine alternative Möglichkeit zur Bereitstellung benutzerdefinierter CSS-Regeln besteht darin, eingebettete Stile direkt auf der Webseite oder in einer verknüpften externen CSS-Regel zu verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer dem Container-DOM-Element die Klasse `.s7carouselviewer` zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit dem Befehl `style=` übergeben wird, verwenden Sie für Ihre CSS-Regeln die Klasse `.s7carouselviewer` als übergeordnete Klasse im untergeordneten Selektor. Wenn Sie eingebettete Stile auf der Web-Seite hinzufügen, qualifizieren Sie diesen Selektor wie folgt mit einer ID des Container-DOM-Elements:

`#<containerId>.s7carouselviewer`

## Erstellen von responsiv gestaltetem CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

Es ist möglich, verschiedene Geräte anzusprechen und Größen in CSS einzubetten, damit Ihre Inhalte je nach Gerät eines Benutzers oder Layout einer bestimmten Webseite unterschiedlich angezeigt werden. Diese Technik umfasst, aber nicht beschränkt auf, verschiedene Layouts, Elementgrößen der Benutzeroberfläche und Bildauflösung.

Der Viewer unterstützt zwei Möglichkeiten zum Erstellen von responsiv gestaltetem CSS: CSS-Markierungen und Standard-CSS-Medienabfragen. Sie können diese beiden Mechanismen unabhängig oder gemeinsam verwenden.

**CSS-Markierungen**

Um das Erstellen von responsiv entworfenen CSS zu unterstützen, unterstützt der Viewer CSS-Markierungen. Diese Markierungen sind spezielle CSS-Klassen, die dynamisch dem Viewer-Container-Element der obersten Ebene zugewiesen werden. Sie basieren auf der Laufzeit-Viewer-Größe und dem Eingabetyp, der auf dem aktuellen Gerät verwendet wird.

Die erste Gruppe von CSS-Markern enthält die Klassen `.s7size_large`, `.s7size_medium` und `.s7size_small`. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Wenn der Viewer-Bereich beispielsweise gleich oder größer als die Größe eines allgemeinen Desktop-Monitors ist, verwenden Sie &quot;`.s7size_large`&quot;. Wenn der Bereich in der Nähe eines gemeinsamen Tablet-Geräts liegt, weisen Sie &quot;`.s7size_medium`&quot;zu. Verwenden Sie für Bereiche, die Mobiltelefonbildschirmen ähnlich sind, `.s7size_small`. Der Hauptzweck dieser CSS-Markierungen besteht darin, verschiedene Benutzeroberflächen-Layouts für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markern enthält `.s7mouseinput` und `.s7touchinput`. Die CSS-Markierung `.s7touchinput` wird gesetzt, wenn das aktuelle Gerät eine Touch-Eingabe ist. Andernfalls wird `.s7mouseinput` verwendet. Diese Markierungen dienen hauptsächlich dazu, Benutzeroberflächen-Eingabeelemente mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen zu erstellen, da Touch-Eingaben normalerweise größere Elemente erfordern.

Im folgenden Beispiel-CSS wird die Größe der Zoom-Schaltfläche auf 28 x 28 Pixel bei Systemen mit Mauseingabe und auf Touch-Eingabegeräten auf 56 x 56 Pixel eingestellt. Wenn die Größe des Viewers noch kleiner ist, wird er auf 20 x 20 Pixel eingestellt.

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
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

Viele Elemente der Viewer-Benutzeroberfläche werden mit Bitmap-Grafiken formatiert und weisen mehr als einen bestimmten visuellen Status auf. Ein gutes Beispiel ist eine Schaltfläche mit normalerweise mindestens drei verschiedenen Status: `up`, `over` und `down`. Jeder Status erfordert eine eigene Bitmap-Grafik, die zugewiesen wird.

Bei einem klassischen Stil würde CSS für jeden Status des Benutzeroberflächenelements einen separaten Verweis auf die einzelne Bilddatei auf dem Server haben. Im Folgenden finden Sie ein Beispiel-CSS zum Formatieren einer Zoom-in-Schaltfläche:

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

Der Nachteil dieses Ansatzes besteht darin, dass der Endbenutzer flackernde oder verzögerte Antworten auf die Benutzeroberfläche erfährt, wenn das Element zum ersten Mal verwendet wird. Diese Aktion tritt auf, da die Bildgrafik für den neuen Elementstatus noch nicht heruntergeladen wurde. Dieser Ansatz kann sich aufgrund der gestiegenen Anzahl an HTTP-Aufrufen an den Server auch geringfügig negativ auf die Leistung auswirken.

CSS-Sprites ist ein anderer Ansatz, bei dem Bildgrafiken für alle Elementzustände in einer PNG-Datei namens &quot;Sprite&quot;kombiniert werden. Ein solches &quot;Sprite&quot;hat alle visuellen Status für das jeweilige Element, das nacheinander positioniert wird. Beim Formatieren eines Benutzeroberflächenelements mit Sprites wird für alle verschiedenen Status in CSS auf dasselbe Sprite-Bild verwiesen. Außerdem wird mit der Eigenschaft &quot;`background-position`&quot;für jeden Status angegeben, welcher Teil des &quot;Sprite&quot;-Bildes verwendet wird. Sie können ein &quot;Sprite&quot;-Bild auf jede geeignete Weise strukturieren. Normalerweise wird sie von Viewern vertikal gestapelt.

Im Folgenden finden Sie ein &quot;sprite&quot;-basiertes Beispiel für die Formatierung desselben Hotspot-Symbols:

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Allgemeine Hinweise und Hinweise zu Stilen {#section-95855dccbbc444e79970f1aaa3260b7b}

* Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung der `!IMPORTANT` -Regel nicht unterstützt, um Viewer-Elemente zu formatieren. Insbesondere sollte die Regel `!IMPORTANT` nicht verwendet werden, um Standard- oder Laufzeitstile zu überschreiben, die vom Viewer- oder Viewer-SDK bereitgestellt werden. Der Grund dafür ist, dass dies das Verhalten von richtigen Komponenten beeinflussen kann. Stattdessen sollten Sie CSS-Selektoren mit der richtigen Spezifität verwenden, um CSS-Eigenschaften festzulegen, die in diesem Viewer-Referenzhandbuch dokumentiert sind.
* Alle Pfade zu externen Assets innerhalb von CSS werden mit dem CSS-Speicherort aufgelöst, nicht mit dem Viewer-HTML-Seitenspeicherort. Beachten Sie diese Regel, wenn Sie die Standard-CSS an einen anderen Speicherort kopieren. Kopieren Sie entweder auch die Standard-Assets oder aktualisieren Sie alle Pfade innerhalb des benutzerdefinierten CSS.
* Das bevorzugte Format für Bitmap-Grafiken ist PNG.
* Bitmap-Grafiken werden Elementen der Benutzeroberfläche mithilfe der Eigenschaft `background-image` zugewiesen.
* Die Eigenschaften `width` und `height` eines Benutzeroberflächenelements definieren seine logische Größe. Die Größe der an `background-image` übergebenen Bitmap wirkt sich nicht auf ihre logische Größe aus.
* Um die hohe Pixeldichte von hochauflösenden Bildschirmen wie Retina zu verwenden, geben Sie Bitmap-Grafiken doppelt so groß an wie die Elementgröße der logischen Benutzeroberfläche. Wenden Sie dann die Eigenschaft `-webkit-background-size:contain` an, um den Hintergrund auf die Elementgröße der logischen Benutzeroberfläche herunterzuskalieren.
* Um eine Schaltfläche aus der Benutzeroberfläche zu entfernen, fügen Sie `display:none` zur CSS-Klasse hinzu.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Sie Transparenz benötigen, verwenden Sie das Format `rgba(R,G,B,A)`. Andernfalls können Sie das Format `#RRGGBB` verwenden.

## Allgemeine Elemente der Benutzeroberfläche {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Im Folgenden finden Sie die Referenzdokumentation zu Elementen der Benutzeroberfläche, die für den Video Image Viewer gilt:
