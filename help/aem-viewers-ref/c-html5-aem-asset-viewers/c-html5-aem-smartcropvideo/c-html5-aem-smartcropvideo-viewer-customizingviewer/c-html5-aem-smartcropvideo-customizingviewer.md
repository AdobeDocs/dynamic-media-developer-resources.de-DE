---
description: Anpassen des Video-Viewers für smartes Zuschneiden
keywords: responsiv
solution: Experience Manager
title: Anpassen des Video-Viewers für smartes Zuschneiden
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 90dc93ee-fdd0-41c9-9eef-4c9952198356
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '1265'
ht-degree: 0%

---

# Anpassen des Video-Viewers für smartes Zuschneiden{#customizing-smartcrop-video-viewer}

Die visuelle Anpassung und die meisten Verhaltensanpassungen erfolgen durch die Erstellung eines benutzerdefinierten CSS.

Der vorgeschlagene Workflow besteht darin, die Standard-CSS-Datei für den entsprechenden Viewer zu übernehmen, sie an einen anderen Speicherort zu kopieren, sie anzupassen und den Speicherort der angepassten Datei im `style=` Befehl.

Standard-CSS-Dateien finden Sie unter folgendem Speicherort:

`<s7_viewers_root>/html5/SmartCropVideoViewer.css`

Benutzerdefinierte CSS-Dateien müssen dieselben Klassendeklarationen wie die Standarddeklaration enthalten. Wenn eine Klassendeklaration weggelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitstellt.

Eine alternative Möglichkeit zur Bereitstellung benutzerdefinierter CSS-Regeln besteht darin, eingebettete Stile direkt auf der Webseite oder in einer verknüpften externen CSS-Regel zu verwenden.

Denken Sie beim Erstellen von benutzerdefiniertem CSS daran, dass der Viewer `.s7smartcropvideoviewer` -Klasse zu ihrem Container-DOM-Element hinzu. Wenn Sie eine externe CSS-Datei verwenden, die mit dem `style=` Befehl, verwenden `.s7smartcropvideoviewer` -Klasse als übergeordnete Klasse im untergeordneten Selektor für Ihre CSS-Regeln. Wenn Sie Stile auf der Web-Seite einbetten, qualifizieren Sie diesen Selektor zusätzlich wie folgt mit einer ID des Container-DOM-Elements:

`#<containerId>.s7smartcropvideoviewer`

## Erstellen von responsiv gestaltetem CSS {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

Es ist möglich, verschiedene Geräte in CSS als Ziel festzulegen, damit Ihre Inhalte je nach Gerät des Benutzers unterschiedlich angezeigt werden. Dieses Targeting umfasst verschiedene Elementgrößen und die Auflösung von Grafiken in der Benutzeroberfläche, ist jedoch nicht darauf beschränkt.

Der Viewer unterstützt zwei Mechanismen zum Erstellen von responsivem CSS: CSS-Markierungen und Standard-CSS-Medienabfragen. Sie können diese unabhängig oder gemeinsam verwenden.

**CSS-Markierungen**

Um responsives CSS zu erstellen, unterstützt der Viewer CSS-Markierungen, die spezielle CSS-Klassen enthalten, die dynamisch dem Viewer-Container-Element der obersten Ebene zugewiesen werden, basierend auf der Laufzeit-Viewer-Größe und dem Eingabetyp, der auf dem aktuellen Gerät verwendet wird.

Die erste Gruppe von CSS-Markern umfasst `.s7size_large`, `.s7size_medium`und `.s7size_small` Klassen. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Das heißt, wenn der Viewer-Bereich gleich oder größer als die Größe eines gemeinsamen Desktop-Monitors ist `.s7size_large` verwendet wird; wenn der Bereich nahe an einem gemeinsamen Tablet-Gerät liegt `.s7size_medium` zugewiesen wurde. Für Bereiche ähnlich wie Mobiltelefonbildschirme `.s7size_small` festgelegt ist. Der Hauptzweck dieser CSS-Markierungen besteht darin, verschiedene Benutzeroberflächen-Layouts für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markern umfasst `.s7mouseinput` und `.s7touchinput`. `.s7touchinput` festgelegt ist, wenn das aktuelle Gerät über Touch-Eingabefunktionen verfügt; andernfalls `.s7mouseinput` verwendet. Diese Markierungen dienen zur Erstellung von Eingabeelementen der Benutzeroberfläche mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen, da Touch-Eingaben normalerweise größere Elemente erfordern. Falls das Gerät sowohl über eine Maus- als auch eine Touch-Funktion verfügt, `.s7touchinput` festgelegt ist und der Viewer eine Touch-optimierte Benutzeroberfläche rendert.

Im folgenden Beispiel-CSS wird die Größe der Wiedergabe-/Pause-Schaltfläche auf Systemen mit Mauseingabe auf 28 x 28 Pixel und auf Touch-Geräten auf 56 x 56 Pixel eingestellt. Darüber hinaus wird die Schaltfläche vollständig ausgeblendet, wenn die Viewer-Größe sehr klein wird:

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7smartcropvideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7smartcropvideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Verwenden Sie CSS-Medienabfragen, um Geräte mit einer anderen Pixeldichte als Ziel auszuwählen. Der folgende Medienabfrageblock enthält CSS, das speziell für High-Density-Bildschirme gilt:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Die Verwendung von CSS-Markierungen ist die flexibelste Methode zum Erstellen von responsiv gestaltetem CSS, da Sie damit nicht nur die Bildschirmgröße des Geräts, sondern auch die tatsächliche Viewer-Größe bestimmen können. Dies kann bei Layouts responsiver Designseiten nützlich sein.

Verwenden Sie die standardmäßige Viewer-CSS-Datei als Beispiel für einen CSS-Marker-Ansatz.

**CSS-Medienabfragen**

Die Geräteerkennung kann auch mit reinen CSS-Medienabfragen durchgeführt werden. Alles, was in einem bestimmten Medienabfrageblock eingeschlossen ist, wird nur angewendet, wenn er auf einem entsprechenden Gerät ausgeführt wird.

Verwenden Sie bei Anwendung auf Mobile Viewer vier CSS-Medienabfragen, die in Ihrer CSS-Datei in der unten aufgeführten Reihenfolge definiert sind:

1. Enthält nur Regeln, die für alle Touch-Geräte spezifisch sind.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. Enthält nur Regeln für Tablets mit Bildschirmen mit hoher Auflösung.

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

Mithilfe des CSS-Medienabfrageansatzes sollten Sie CSS mit der Geräteerkennung wie folgt organisieren:

* Zunächst werden im Desktop-spezifischen Abschnitt alle Eigenschaften definiert, die entweder Desktop-spezifisch oder für alle Bildschirme gemeinsam sind.
* Zweitens sollten die vier Medienabfragen in der oben definierten Reihenfolge ausgeführt werden und CSS-Regeln für den entsprechenden Gerätetyp bereitstellen.

Es ist nicht erforderlich, die gesamte Viewer-CSS in jeder Medienabfrage zu duplizieren. Innerhalb einer Medienabfrage werden nur Eigenschaften neu definiert, die für bestimmte Geräte spezifisch sind.

## CSS-Sprites {#section-9b6d8d601cb441d08214dada7bb4eddc}

Viele Elemente der Viewer-Benutzeroberfläche werden mit Bitmap-Grafiken formatiert und weisen mehr als einen bestimmten visuellen Status auf. Ein gutes Beispiel ist eine Schaltfläche mit normalerweise mindestens drei verschiedenen Status: &quot;up&quot;, &quot;over&quot;und &quot;down&quot;. Jeder Status erfordert eine eigene Bitmap-Grafik, die zugewiesen wird.

Bei einem klassischen Stil würde CSS für jeden Status des Benutzeroberflächenelements einen separaten Verweis auf die einzelne Bilddatei auf dem Server haben. Im Folgenden finden Sie ein Beispiel-CSS für die Formatierung einer Vollbildschaltfläche:

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

Der Nachteil dieses Ansatzes besteht darin, dass der Endbenutzer flackernde oder verzögerte Antworten auf die Benutzeroberfläche erfährt, wenn das Element zum ersten Mal mit interagiert wird. Diese Aktion tritt auf, da die Bildgrafik für den neuen Elementstatus noch nicht heruntergeladen wurde. Dieser Ansatz kann sich aufgrund der gestiegenen Anzahl an HTTP-Aufrufen an den Server auch geringfügig negativ auf die Leistung auswirken.

CSS-Sprites ist ein anderer Ansatz, bei dem Bildgrafiken für alle Elementzustände in einer PNG-Datei namens &quot;Sprite&quot;kombiniert werden. Ein solches &quot;Sprite&quot;hat alle visuellen Status für das jeweilige Element, das nacheinander positioniert wird. Beim Formatieren eines Benutzeroberflächenelements mit Sprites wird für alle verschiedenen Status in der CSS auf dasselbe Sprite-Bild verwiesen. Außerdem wird die `background-position` -Eigenschaft wird für jeden Status verwendet, um anzugeben, welcher Teil des &quot;Sprite&quot;-Bildes verwendet wird. Sie können ein &quot;Sprite&quot;-Bild auf jede geeignete Weise strukturieren. Normalerweise wird sie von Viewern vertikal gestapelt. Nachfolgend finden Sie ein &quot;sprite&quot;-basiertes Beispiel für die Formatierung derselben Vollbildschaltfläche von oben:

```
.s7smartcropvideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Allgemeine Hinweise und Hinweise zu Stilen {#section-097418bd618740bba36352629e4d88e1}

* Alle Pfade zu externen Assets in CSS werden mit dem CSS-Speicherort aufgelöst, nicht mit dem Speicherort der Viewer-HTML-Seite. Denken Sie daran, diese Regel zu berücksichtigen, wenn Sie die Standard-CSS an einen anderen Speicherort kopieren. Kopieren Sie die Standard-Assets oder aktualisieren Sie Pfade innerhalb des benutzerdefinierten CSS.
* Das bevorzugte Format für Bitmap-Grafiken ist PNG.
* Bitmap-Grafiken werden den Elementen der Benutzeroberfläche mithilfe der `background-image` -Eigenschaft.
* Die `width` und `height` -Eigenschaften eines Benutzeroberflächenelements definieren die logische Größe. Die Größe der Bitmap, die an `background-image` hat keine Auswirkungen auf die logische Größe.

* Um die hohe Pixeldichte von hochauflösenden Bildschirmen wie Retina zu verwenden, geben Sie Bitmap-Grafiken doppelt so groß an wie die Elementgröße der logischen Benutzeroberfläche. Wenden Sie dann die `-webkit-background-size:contain` -Eigenschaft, um den Hintergrund auf die Elementgröße der logischen Benutzeroberfläche herunterzuskalieren.
* Um eine Schaltfläche aus der Benutzeroberfläche zu entfernen, fügen Sie `display:none` zu seiner CSS-Klasse hinzu.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Sie Transparenz benötigen, verwenden Sie das Format `rgba(R,G,B,A)`. Andernfalls können Sie das Format `#RRGGBB`.

* Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung der `!IMPORTANT` -Regel wird nicht unterstützt, um Viewer-Elemente zu formatieren. Insbesondere `!IMPORTANT` -Regel sollte nicht verwendet werden, um Standard- oder Laufzeitstile zu überschreiben, die vom Viewer- oder Viewer-SDK bereitgestellt werden. Der Grund dafür ist, dass dies das Verhalten von richtigen Komponenten beeinflussen kann. Stattdessen sollten Sie CSS-Selektoren mit der richtigen Spezifität verwenden, um CSS-Eigenschaften festzulegen, die in diesem Referenzhandbuch dokumentiert sind.

## Allgemeine Benutzeroberflächen-Elemente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Im Folgenden finden Sie die Referenzdokumentation zu Elementen der Benutzeroberfläche, die für den Smart Crop Video Viewer gilt:
