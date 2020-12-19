---
description: Alle visuellen Anpassungen und die meisten Verhaltensanpassungen für den einfachen Zoom-Viewer erfolgen durch Erstellung eines benutzerdefinierten CSS.
keywords: responsive
seo-description: Alle visuellen Anpassungen und die meisten Verhaltensanpassungen für den einfachen Zoom-Viewer erfolgen durch Erstellung eines benutzerdefinierten CSS.
seo-title: Anpassen des einfachen Zoom-Viewers
solution: Experience Manager
title: Anpassen des einfachen Zoom-Viewers
topic: Dynamic media
uuid: 9f3c203e-ff6f-4bf1-a1dc-26495412af45
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 0%

---


# Anpassen des grundlegenden Zoom-Viewers{#customizing-basic-zoom-viewer}

Alle visuellen Anpassungen und die meisten Verhaltensanpassungen für den einfachen Zoom-Viewer erfolgen durch Erstellung eines benutzerdefinierten CSS.

Der empfohlene Arbeitsablauf besteht darin, die Standard-CSS-Datei für den entsprechenden Viewer zu übernehmen, sie an einen anderen Speicherort zu kopieren, sie anzupassen und den Speicherort der angepassten Datei im Befehl `style=` anzugeben.

Standard-CSS-Dateien finden Sie im folgenden Verzeichnis:

`<s7_viewers_root>/html5/BasicZoomViewer_light.css`

Der Viewer wird mit zwei sofort einsetzbaren CSS-Dateien für &quot;helle&quot;und &quot;dunkle&quot;Farbschemata geliefert. Die &quot;helle&quot;Version wird standardmäßig verwendet. Sie können jedoch mithilfe der folgenden Standard-CSS zur &quot;dunklen&quot;Version wechseln:

`<s7_viewers_root>/html5/BasicZoomViewer_dark.css`

Die benutzerdefinierte CSS-Datei muss dieselben Klassendeklarationen wie die Standarddeklaration enthalten. Wenn eine Klassendeklaration weggelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitgestellt werden.

Alternativ können Sie benutzerdefinierte CSS-Regeln bereitstellen, indem Sie eingebettete Stile direkt auf der Webseite oder in einer verknüpften externen CSS-Regel verwenden.

Beachten Sie beim Erstellen benutzerdefinierter CSS, dass der Viewer dem Container-DOM-Element die Klasse `.s7basiczoomviewer` zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit dem Befehl `style=` übergeben wird, verwenden Sie die Klasse `.s7basiczoomviewer` als übergeordnete Klasse in der untergeordneten Auswahl für Ihre CSS-Regeln. Wenn Sie eingebettete Stile auf der Webseite verwenden, sollten Sie diesen Selektor zusätzlich mit einer ID des Container-DOM-Elements wie folgt qualifizieren:

`#<containerId>.s7basiczoomviewer`

## Erstellen von Responsive Design CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

Es ist möglich, verschiedene Geräte und Einbettungsgrößen in CSS Zielgruppe, damit Ihre Inhalte je nach Benutzergerät oder Webseitenlayout unterschiedlich angezeigt werden. Dazu gehören u. a. verschiedene Layouts, die Elementgröße der Benutzeroberfläche und die Auflösung von Grafiken.

Der Viewer unterstützt zwei Mechanismen zum Erstellen von Responsive-Design-CSS: CSS-Marker und Standard-CSS-Media-Abfragen. Sie können diese unabhängig oder zusammen verwenden.

**CSS-Marker**

Zur Unterstützung bei der Erstellung reaktionsfähiger CSS unterstützt der Viewer CSS-Marker. Hierbei handelt es sich um spezielle CSS-Klassen, die dynamisch dem Viewer-Container der obersten Ebene zugewiesen werden, basierend auf der Laufzeit-Viewer-Größe und dem Eingabetyp, der auf dem aktuellen Gerät verwendet wird.

Die erste Gruppe von CSS-Markern umfasst die Klassen `.s7size_large`, `.s7size_medium` und `.s7size_small`. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Wenn der Viewer-Bereich größer oder gleich der Größe eines gemeinsamen Desktop-Monitors ist, wird `.s7size_large` verwendet; Wenn der Bereich nahe an einem gemeinsamen Tablet-Gerät liegt, wird `.s7size_medium` zugewiesen. Für Bereiche, die mit Mobiltelefonbildschirmen vergleichbar sind, ist `.s7size_small` eingestellt. Diese CSS-Marker dienen vor allem dazu, unterschiedliche Layouts der Benutzeroberfläche für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markern enthält `.s7mouseinput` und `.s7touchinput`. `.s7touchinput` eingestellt ist, wenn das aktuelle Gerät über Touch-Eingabefunktionen verfügt; andernfalls  `.s7mouseinput` verwendet. Diese Markierungen sind hauptsächlich dazu bestimmt, Benutzeroberflächeneingabeelemente mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen zu erstellen, da die Touch-Eingabe normalerweise größere Elemente erfordert. In Fällen, in denen das Gerät sowohl Mauseingabe- als auch Berührungsfunktionen hat, wird `.s7touchinput` eingestellt und der Viewer rendert eine touchfreundliche Benutzeroberfläche.

Im folgenden CSS-Beispiel wird die Größe der Zoomschaltfläche auf Systemen mit Mauseingabe auf 28 x 28 Pixel und auf Touch-Geräten auf 56 x 56 Pixel eingestellt. Außerdem wird die Schaltfläche vollständig ausgeblendet, wenn die Viewer-Größe sehr klein ist:

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7basiczoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7basiczoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Zur Zielgruppe von Geräten mit unterschiedlicher Pixeldichte müssen Sie CSS-Media-Abfragen verwenden. Der folgende Medienblock enthält CSS-spezifische Abfragen für hochdichte Bildschirme:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Die Verwendung von CSS-Markierungen ist die flexibelste Methode zum Erstellen von CSS für reaktionsfähiges Design, da Sie damit nicht nur die Bildschirmgröße des Geräts, sondern auch die tatsächliche Viewer-Größe Zielgruppe haben, was für reaktionsfähige Layouts nützlich ist.

Sie können die Standard-CSS-Datei des Viewers als Beispiel für einen CSS-Marker-Ansatz verwenden.

**CSS-Medien-Abfragen**

Sie können die Geräteerkennung auch mit reinen CSS-Media-Abfragen durchführen. Alles, was in einem Medienblock eingeschlossen ist, wird nur angewendet, wenn er auf einem entsprechenden Abfrage ausgeführt wird.

Bei Anwendung auf mobile Viewer werden vier CSS-Media-Abfragen verwendet, die in Ihrer CSS definiert sind, und zwar in der unten aufgeführten Reihenfolge:

1. Enthält nur Regeln, die für alle Touch-Geräte spezifisch sind.

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

1. Enthält nur Regeln, die für alle Mobiltelefone spezifisch sind.

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

Mithilfe eines Medienansatzes sollten Sie CSS mit Geräteerkennung wie folgt organisieren:

* Zunächst definiert der Abschnitt &quot;Desktop-spezifisch&quot;alle Eigenschaften, die entweder für den Desktop spezifisch oder für alle Bildschirme gleich sind.
* Zweitens gehen die vier Medien in der oben definierten Reihenfolge vor und stellen CSS-Abfragen bereit, die für den jeweiligen Gerätetyp spezifisch sind.

Es ist nicht erforderlich, die gesamte CSS des Viewers in jeder Mediendatei-Abfrage Duplikat. Nur Eigenschaften, die spezifisch für bestimmte Geräte sind, werden innerhalb einer Mediendatei neu definiert.

## CSS-Sprites {#section-9b6d8d601cb441d08214dada7bb4eddc}

Viele Elemente der Benutzeroberfläche des Viewers werden mit Bitmapgrafiken formatiert und haben mehr als einen bestimmten visuellen Status. Ein gutes Beispiel ist eine Schaltfläche mit normalerweise mindestens 3 verschiedenen Status: &quot;up&quot;, &quot;over&quot; und &quot;down&quot;. Jeder Status erfordert eine eigene Bitmap-Grafik, die zugewiesen wird.

Bei einem klassischen Stilverfahren würde das CSS für jeden Status des Elements der Benutzeroberfläche einen separaten Verweis auf die einzelne Bilddatei auf dem Server haben. Im Folgenden finden Sie ein Beispiel-CSS zum Formatieren der Schaltfläche zum Einzoomen:

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Der Nachteil dieses Ansatzes besteht darin, dass der Endbenutzer flackernde oder verzögerte Antworten auf die Benutzeroberfläche erfährt, wenn das Element zum ersten Mal interagiert wird. Diese Aktion tritt auf, weil die Bildgrafik für den Status des neuen Elements noch nicht heruntergeladen wurde. Dieser Ansatz kann sich außerdem geringfügig negativ auf die Leistung auswirken, da die Anzahl der HTTP-Aufrufe an den Server zunimmt.

CSS-Sprites sind andere Methoden, bei denen Bildgrafiken für alle Elementzustände in einer einzigen PNG-Datei namens &quot;Sprite&quot;kombiniert werden. Ein solches &quot;Sprite&quot;hat alle visuellen Zustände für das jeweilige Element nacheinander positioniert. Beim Formatieren eines Benutzeroberflächenelements mit Sprites wird für alle verschiedenen Status im CSS auf dasselbe Sprite-Bild verwiesen. Die `background-position`-Eigenschaft wird für jeden Status verwendet, um anzugeben, welcher Teil des &quot;sprite&quot;-Bildes verwendet wird. Sie können ein &quot;Sprite&quot;-Bild auf jede geeignete Weise strukturieren. Normalerweise wird das Bild vertikal gestapelt. Nachstehend finden Sie ein &quot;sprite&quot;-basiertes Beispiel für die Formatierung derselben Zoom-in-Schaltfläche von oben:

```
.s7basiczoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Allgemeine Hinweise und Hinweise zum Stil {#section-95855dccbbc444e79970f1aaa3260b7b}

* Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung der `!IMPORTANT`-Regel nicht unterstützt, um Viewer-Elemente zu formatieren. Insbesondere sollte die `!IMPORTANT`-Regel nicht verwendet werden, um Standard- oder Laufzeitformatierungen zu überschreiben, die vom Viewer- oder Viewer-SDK bereitgestellt werden. Der Grund dafür ist, dass dies das Verhalten von richtigen Komponenten beeinträchtigen kann. Stattdessen sollten Sie CSS-Selektoren mit der richtigen Spezifität verwenden, um CSS-Eigenschaften festzulegen, die in diesem Referenzhandbuch dokumentiert sind.
* Alle Pfade zu externen Assets innerhalb von CSS werden mit dem CSS-Speicherort und nicht mit dem HTML-Seitenspeicherort des Viewers aufgelöst. Achten Sie auf diese Regel, wenn Sie die Standard-CSS an einen anderen Speicherort kopieren. Kopieren Sie entweder die Standardelemente oder aktualisieren Sie Pfade in der benutzerdefinierten CSS.
* Das bevorzugte Format für Bitmapgrafiken ist PNG.
* Bitmapgrafiken werden Benutzeroberflächenelementen mithilfe der Eigenschaft `background-image` zugewiesen.
* Die Eigenschaften `width` und `height` eines Elements der Benutzeroberfläche definieren seine logische Größe. Die Größe der an `background-image` übergebenen Bitmap hat keine Auswirkungen auf die logische Größe.
* Um die hohe Pixeldichte hochauflösender Bildschirme wie Retina zu verwenden, geben Sie Bitmapgrafiken doppelt so groß wie die Elementgröße der logischen Benutzeroberfläche an. Wenden Sie dann die `-webkit-background-size:contain`-Eigenschaft an, um den Hintergrund auf die Elementgröße der logischen Benutzeroberfläche herunterzuskalieren.
* Um eine Schaltfläche aus der Benutzeroberfläche zu entfernen, fügen Sie der CSS-Klasse `display:none` hinzu.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Sie Transparenz benötigen, verwenden Sie das Format `rgba(R,G,B,A)`. Andernfalls können Sie das Format `#RRGGBB` verwenden.

## Allgemeine Benutzeroberflächenelemente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Im Folgenden finden Sie eine Referenzdokumentation zu Elementen der Benutzeroberfläche, die für den einfachen Zoom-Viewer gilt:
