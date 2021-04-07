---
description: Alle visuellen Anpassungen und die meisten Verhaltensanpassungen für den Video360-Viewer erfolgen durch Erstellen einer benutzerdefinierten CSS.
keywords: responsive
solution: Experience Manager
title: Anpassen des Video360-Viewers
feature: Dynamic Media Classic,Viewer,SDK/API,360 VR Video
role: Entwickler, Geschäftspraktiker
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1304'
ht-degree: 0%

---

# Anpassen des Video360-Viewers{#customizing-video-viewer}

Alle visuellen Anpassungen und die meisten Verhaltensanpassungen für den Video360-Viewer erfolgen durch Erstellen einer benutzerdefinierten CSS.

Der empfohlene Arbeitsablauf besteht darin, die Standard-CSS-Datei für den entsprechenden Viewer zu übernehmen, sie an einen anderen Speicherort zu kopieren, sie anzupassen und den Speicherort der angepassten Datei im Befehl `style=` anzugeben.

Standard-CSS-Dateien finden Sie im folgenden Verzeichnis:

`<s7_viewers_root>/html5/Video360Viewer_dark.css`

Die benutzerdefinierte CSS-Datei muss dieselben Klassendeklarationen wie die Standarddeklaration enthalten. Wenn eine Klassendeklaration weggelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitgestellt werden.

Eine andere Möglichkeit, benutzerdefinierte CSS-Regeln bereitzustellen, besteht darin, eingebettete Stile direkt auf der Webseite oder in einer verknüpften externen CSS-Regel zu verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer dem Container-DOM-Element die Klasse `.s7video360viewer` zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit dem Befehl `style=` übergeben wird, verwenden Sie die Klasse `.s7video360viewer` als übergeordnete Klasse in der untergeordneten Auswahl für Ihre CSS-Regeln. Wenn Sie eingebettete Stile auf der Webseite verwenden, sollten Sie diesen Selektor zusätzlich mit einer ID des Container-DOM-Elements wie folgt qualifizieren:

`#<containerId>.s7video360viewer`

## Erstellen von reaktionsfähigem CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

Es ist möglich, verschiedene Geräte und Einbettungsgrößen in CSS Zielgruppe, damit Ihre Inhalte je nach Benutzergerät oder Webseitenlayout unterschiedlich angezeigt werden. Dazu gehören u. a. verschiedene Layouts, die Elementgröße der Benutzeroberfläche und die Auflösung von Grafiken.

Der Viewer unterstützt zwei Mechanismen zum Erstellen von Responsive-Design-CSS: CSS-Marker und Standard-CSS-Media-Abfragen. Sie können diese unabhängig oder zusammen verwenden.

**CSS-Marker**

Zur Unterstützung bei der Erstellung reaktionsfähiger CSS unterstützt der Viewer CSS-Markierungen. Hierbei handelt es sich um spezielle CSS-Klassen, die dynamisch dem Viewer-Container der obersten Ebene zugewiesen werden, basierend auf der Laufzeit-Viewer-Größe und dem Eingabetyp, der auf dem aktuellen Gerät verwendet wird.

Die erste Gruppe von CSS-Markern umfasst die Klassen `.s7size_large`, `.s7size_medium` und `.s7size_small`. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Wenn der Viewer-Bereich größer oder gleich der Größe eines gemeinsamen Desktop-Monitors ist, wird `.s7size_large` verwendet; Wenn der Bereich nahe an einem gemeinsamen Tablet-Gerät liegt, wird `.s7size_medium` zugewiesen. Für Bereiche, die mit Mobiltelefonbildschirmen vergleichbar sind, ist `.s7size_small` eingestellt. Diese CSS-Marker dienen vor allem dazu, unterschiedliche Layouts der Benutzeroberfläche für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markern enthält `.s7mouseinput` und `.s7touchinput`. `.s7touchinput` eingestellt ist, wenn das aktuelle Gerät über Touch-Eingabefunktionen verfügt; andernfalls  `.s7mouseinput` verwendet. Diese Markierungen sind hauptsächlich dazu bestimmt, Benutzeroberflächeneingabeelemente mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen zu erstellen, da für gewöhnlich Touch-Eingaben größere Elemente erforderlich sind. Beachten Sie, dass für den Fall, dass das Gerät sowohl über Maus- als auch Touch-Funktionen verfügt, `.s7touchinput` eingestellt ist und der Viewer eine touchfreundliche Benutzeroberfläche wiedergibt.

Im folgenden CSS-Beispiel wird die Schaltflächengröße für Wiedergabe/Pause auf 28 x 28 Pixel bei Systemen mit Mauseingabe und auf Touch-Geräten auf 56 x 56 Pixel eingestellt. Außerdem wird die Schaltfläche vollständig ausgeblendet, wenn die Viewer-Größe erheblich reduziert wird:

```
.s7video360viewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7video360viewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7video360viewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Zur Zielgruppe von Geräten mit unterschiedlicher Pixeldichte müssen Sie CSS-Media-Abfragen verwenden. Der folgende Medienblock enthält CSS-spezifische Abfragen für hochdichte Bildschirme:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Die Verwendung von CSS-Markierungen ist die flexibelste Methode zum Erstellen von Responsive-Design-CSS, da Sie damit nicht nur die Bildschirmgröße des Geräts, sondern auch die tatsächliche Viewer-Größe Zielgruppe haben können. Dies ist bei reaktionsfähigen Designlayouts nützlich.

Sie können die Standard-CSS-Datei des Viewers als Beispiel für einen CSS-Marker-Ansatz verwenden.

**CSS-Medien-Abfragen**

Sie können die Geräteerkennung auch mit reinen CSS-Media-Abfragen durchführen. Alles, was in einem Medienblock eingeschlossen ist, wird nur angewendet, wenn er auf einem entsprechenden Abfrage ausgeführt wird.

Bei der Anwendung auf HTML5-Mobil-Viewer werden vier CSS-Media-Abfragen verwendet, die in Ihrer CSS definiert sind, und zwar in der folgenden Reihenfolge:

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

Bei einem klassischen Stilverfahren würde das CSS für jeden Status des Elements der Benutzeroberfläche einen separaten Verweis auf die einzelne Bilddatei auf dem Server haben. Im Folgenden finden Sie ein Beispiel für CSS zum Formatieren einer Schaltfläche im Vollbildmodus:

```
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

Der Nachteil dieses Ansatzes besteht darin, dass der Endbenutzer flackernde oder verzögerte Antworten auf die Benutzeroberfläche erfährt, wenn das Element zum ersten Mal interagiert wird. Diese Aktion tritt auf, weil die Bildgrafik für den Status des neuen Elements noch nicht heruntergeladen wurde. Dieser Ansatz kann sich außerdem geringfügig negativ auf die Leistung auswirken, da die Anzahl der HTTP-Aufrufe an den Server zunimmt.

CSS-Sprites sind andere Methoden, bei denen Bildgrafiken für alle Elementzustände in einer einzigen PNG-Datei namens &quot;Sprite&quot;kombiniert werden. Ein solches &quot;Sprite&quot;hat alle visuellen Zustände für das jeweilige Element nacheinander positioniert. Beim Formatieren eines Benutzeroberflächenelements mit Sprites wird für alle verschiedenen Status im CSS auf dasselbe Sprite-Bild verwiesen. Die `background-position`-Eigenschaft wird für jeden Status verwendet, um anzugeben, welcher Teil des &quot;sprite&quot;-Bildes verwendet wird. Sie können ein &quot;Sprite&quot;-Bild auf jede geeignete Weise strukturieren. Normalerweise wird das Bild vertikal gestapelt. Nachstehend finden Sie ein &quot;sprite&quot;-basiertes Beispiel für die Formatierung derselben Schaltfläche im Vollbildmodus:

```
.s7video360viewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Allgemeine Hinweise und Hinweise zum Stil {#section-95855dccbbc444e79970f1aaa3260b7b}

* Alle Pfade zu externen Assets innerhalb von CSS werden mit dem CSS-Speicherort und nicht mit dem HTML-Seitenspeicherort des Viewers aufgelöst. Achten Sie auf diese Regel, wenn Sie die Standard-CSS an einen anderen Speicherort kopieren. Kopieren Sie entweder die Standardelemente oder aktualisieren Sie Pfade in der benutzerdefinierten CSS.
* Das bevorzugte Format für Bitmapgrafiken ist PNG.
* Bitmapgrafiken werden Benutzeroberflächenelementen mithilfe der Eigenschaft `background-image` zugewiesen.
* Die Eigenschaften `width` und `height` eines Elements der Benutzeroberfläche definieren seine logische Größe. Die Größe der an `background-image` übergebenen Bitmap hat keine Auswirkungen auf die logische Größe.

* Um die hohe Pixeldichte hochauflösender Bildschirme wie Retina zu verwenden, geben Sie Bitmapgrafiken doppelt so groß wie die Elementgröße der logischen Benutzeroberfläche an. Wenden Sie dann die `-webkit-background-size:contain`-Eigenschaft an, um den Hintergrund auf die Elementgröße der logischen Benutzeroberfläche herunterzuskalieren.
* Um eine Schaltfläche aus der Benutzeroberfläche zu entfernen, fügen Sie der CSS-Klasse `display:none` hinzu.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Sie Transparenz benötigen, verwenden Sie das Format `rgba(R,G,B,A)`. Andernfalls können Sie das Format `#RRGGBB` verwenden.

* Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung der `!IMPORTANT`-Regel nicht unterstützt, um Viewer-Elemente zu formatieren. Insbesondere sollte die `!IMPORTANT`-Regel nicht verwendet werden, um Standard- oder Laufzeitformatierungen zu überschreiben, die vom Viewer- oder Viewer-SDK bereitgestellt werden. Der Grund dafür ist, dass dies das Verhalten von richtigen Komponenten beeinträchtigen kann. Stattdessen sollten Sie CSS-Selektoren mit der richtigen Spezifität verwenden, um CSS-Eigenschaften festzulegen, die in diesem Referenzhandbuch dokumentiert sind.

## Allgemeine Benutzeroberflächenelemente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Nachstehend finden Sie eine Referenzdokumentation zu Elementen der Benutzeroberfläche, die für Video360 Viewer gilt:
