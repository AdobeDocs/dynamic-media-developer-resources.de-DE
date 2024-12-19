---
title: Anpassen des interaktiven Video-Viewers
description: Die gesamte visuelle Anpassung und die meisten Verhaltensanpassungen für den interaktiven Video-Viewer werden durch die Erstellung eines benutzerdefinierten CSS vorgenommen.
keywords: Responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c428c3e6-81be-4708-b064-f9d794183209
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 0%

---

# Anpassen des interaktiven Video-Viewers{#customizing-interactive-video-viewer}

Die gesamte visuelle Anpassung und die meisten Verhaltensanpassungen für den interaktiven Video-Viewer werden durch die Erstellung eines benutzerdefinierten CSS vorgenommen.

Der vorgeschlagene Workflow besteht darin, die standardmäßige CSS-Datei für den entsprechenden Viewer zu verwenden, sie an einen anderen Speicherort zu kopieren, anzupassen und den Speicherort der angepassten Datei im `style=`-Befehl anzugeben.

Standard-CSS-Dateien befinden sich unter folgendem Speicherort:

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

Der Viewer wird mit zwei vorkonfigurierten CSS-Dateien für „helle“ und „dunkle“ Farbschemata geliefert. Standardmäßig wird die „dunkle“ Version verwendet, aber es ist einfach, mithilfe des folgenden Standard-CSS zur „hellen“ Version zu wechseln:

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

Benutzerdefinierte CSS-Datei muss dieselben Klassendeklarationen enthalten wie die Standarddeklaration. Wenn eine Klassendeklaration ausgelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für Elemente der Benutzeroberfläche bereitstellt.

Eine alternative Möglichkeit, benutzerdefinierte CSS-Regeln bereitzustellen, besteht darin, eingebettete Stile direkt auf der Web-Seite oder in einer der verknüpften externen CSS-Regeln zu verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer `.s7interactivevideoviewer` Klasse seinem Container-DOM-Element zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit `style=` Befehl übergeben wird, verwenden Sie `.s7interactivevideoviewer` Klasse als übergeordnete Klasse in einem untergeordneten Selektor für Ihre CSS-Regeln. Wenn Sie eingebettete Stile auf der Web-Seite verwenden, qualifizieren Sie diesen Selektor mit einer ID des Container-DOM-Elements wie folgt:

`#<containerId>.s7interactivevideoviewer`

## Erstellen von responsivem CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

Es ist möglich, verschiedene Geräte anzusprechen und Größen in CSS einzubetten, damit Ihre Inhalte je nach Gerät eines Benutzers oder einem bestimmten Web-Seiten-Layout unterschiedlich angezeigt werden. Diese Methode umfasst u. a. verschiedene Layouts, Elementgrößen der Benutzeroberfläche und Bildauflösung.

Der Viewer unterstützt zwei Mechanismen zum Erstellen von responsivem entworfenem CSS: CSS-Markierungen und standardmäßige CSS-Medienabfragen. Sie können diese Mechanismen unabhängig oder zusammen verwenden.

**CSS-Markierungen**

Um das Erstellen von responsivem entworfenem CSS zu erleichtern, unterstützt der Viewer CSS-Markierungen. Diese Markierungen sind spezielle CSS-Klassen. Sie werden basierend auf der Laufzeit-Viewer-Größe und dem auf dem aktuellen Gerät verwendeten Eingabetyp dynamisch dem Viewer-Container-Element der obersten Ebene zugewiesen.

Die erste Gruppe von CSS-Markern umfasst `.s7size_large`-, `.s7size_medium`- und `.s7size_small`. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Wenn der Viewer-Bereich gleich oder größer ist als die Größe eines herkömmlichen Desktop-Monitors, wird `.s7size_large` verwendet. Wenn der Bereich in der Nähe eines allgemeinen Tablet-Geräts liegt, wird `.s7size_medium` zugewiesen. Für Bereiche, die Mobiltelefonbildschirmen ähnlich sind, ist `.s7size_small` festgelegt. Der primäre Zweck dieser CSS-Markierungen besteht darin, verschiedene Benutzeroberflächen-Layouts für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markern enthält `.s7mouseinput` und `.s7touchinput`. Die Markierung `.s7touchinput` wird gesetzt, wenn das aktuelle Gerät über Touch-Eingabefunktionen verfügt; andernfalls wird `.s7mouseinput` verwendet. Diese Markierungen sind hauptsächlich dazu gedacht, Benutzeroberflächen-Eingabeelemente mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen zu erstellen, da normalerweise für Touch-Eingaben größere Elemente erforderlich sind.

Die dritte Gruppe von CSS-Markern enthält `.s7device_landscape` und `.s7device_portrait`. Die `.s7device_landscape` wird festgelegt, wenn sich das Touch-Gerät im Querformat befindet. `.s7device_portrait` wird verwendet, wenn das Touch-Gerät im Hochformat gedreht wird. Diese CSS-Markierungen sind nur für die Verwendung auf Desktop-Systemen vorgesehen.

Im folgenden Beispiel-CSS wird die Größe der Wiedergabe-/Pause-Schaltfläche auf Systemen mit Mauseingang auf 28x28 Pixel und auf Touch-Geräten auf 56x56 Pixel eingestellt. Darüber hinaus wird die Schaltfläche vollständig ausgeblendet, wenn die Viewer-Größe erheblich reduziert wird:

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7interactivevideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7interactivevideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

In diesem Beispiel befindet sich die Video-Steuerleiste 138 Pixel über dem unteren Rand des Viewers, wenn sich das Touch-Gerät im Hochformat befindet. In allen anderen Fällen wird sie an das Ende des Viewers verschoben:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
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

Viele Elemente der Viewer-Benutzeroberfläche werden mit Bitmap-Grafiken formatiert und weisen mehr als einen eindeutigen visuellen Status auf. Ein gutes Beispiel ist eine Schaltfläche, die normalerweise mindestens drei verschiedene Status hat: „oben“, „vorbei“ und „unten“. Jedem Status muss ein eigenes Bitmap-Bildmaterial zugewiesen werden.

Bei einem klassischen Stilansatz hätte das CSS für jeden Status des Benutzeroberflächenelements einen separaten Verweis auf eine einzelne Bilddatei auf dem Server. Im Folgenden finden Sie ein Beispiel für die CSS-Formatierung einer Vollbildschaltfläche:

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

Der Nachteil dieses Ansatzes besteht darin, dass die Endbenutzerin bzw. der Endbenutzer flackert oder eine verzögerte Antwort der Benutzeroberfläche erfährt, wenn das Element zum ersten Mal interagiert wird. Diese Aktion tritt auf, weil das Bildmaterial für den neuen Elementstatus noch nicht heruntergeladen wurde. Außerdem kann dieser Ansatz leichte negative Auswirkungen auf die Leistung haben, da die Anzahl der HTTP-Aufrufe an den Server zunimmt.

CSS-Sprites sind ein anderer Ansatz, bei dem Bildgrafiken für alle Elementstatus in einer einzigen PNG-Datei namens „Sprite“ zusammengefasst werden. Ein solches „Sprite“ weist alle visuellen Zustände für das angegebene Element nacheinander auf. Beim Formatieren eines Elements der Benutzeroberfläche mit Sprites wird für alle verschiedenen Status in CSS auf dasselbe Sprite-Bild verwiesen. Außerdem wird die `background-position`-Eigenschaft für jeden Status verwendet, um anzugeben, welcher Teil des „Sprite“-Bildes verwendet wird. Sie können ein „Sprite“-Bild auf jede geeignete Weise strukturieren. Betrachter haben sie normalerweise vertikal gestapelt. Im Folgenden finden Sie ein „Sprite“-basiertes Beispiel für die Formatierung derselben Vollbildschaltfläche zuvor:

```
.s7interactivevideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Allgemeine Hinweise und Hinweise zu Stilen {#section-95855dccbbc444e79970f1aaa3260b7b}

* Beim Anpassen der Viewer-Benutzeroberfläche mit CSS wird die Verwendung der `!IMPORTANT`-Regel nicht unterstützt, um Viewer-Elemente zu gestalten. Insbesondere sollte `!IMPORTANT` Regel nicht verwendet werden, um Standard- oder Laufzeitstile zu überschreiben, die vom Viewer oder Viewer-SDK bereitgestellt werden. Der Grund dafür ist, dass dies das Verhalten der richtigen Komponenten beeinträchtigen kann. Stattdessen sollten Sie CSS-Selektoren mit der richtigen Spezifität verwenden, um CSS-Eigenschaften festzulegen, die in diesem Referenzhandbuch dokumentiert sind.

* Alle Pfade zu externen Assets innerhalb von CSS werden anhand des CSS-Speicherorts aufgelöst, nicht anhand des Speicherorts der Viewer-HTML-Seite. Beachten Sie diese Regel, wenn Sie das Standard-CSS an einen anderen Speicherort kopieren. Kopieren Sie entweder die Standard-Assets oder aktualisieren Sie die Pfade innerhalb des benutzerdefinierten CSS.
* Das bevorzugte Format für Bitmap-Grafiken ist PNG.
* Bitmap-Grafiken werden Benutzeroberflächenelementen mithilfe der `background-image`-Eigenschaft zugewiesen.
* Die `width`- und `height` eines Benutzeroberflächenelements definieren dessen logische Größe. Die Größe der an `background-image` übergebenen Bitmap hat keine Auswirkungen auf die logische Größe.

* Um die hohe Pixeldichte hochauflösender Bildschirme wie Retina zu verwenden, geben Sie Bitmap-Grafiken doppelt so groß wie die Elementgröße der logischen Benutzeroberfläche an. Wenden Sie dann die Eigenschaft `-webkit-background-size:contain` an, um den Hintergrund auf die Elementgröße der logischen Benutzeroberfläche herunterzuskalieren.
* Um eine Schaltfläche aus der Benutzeroberfläche zu entfernen, fügen Sie `display:none` zu ihrer CSS-Klasse hinzu.
* Sie können verschiedene Formate für Farbwerte verwenden, die von CSS unterstützt werden. Wenn Sie Transparenz benötigen, verwenden Sie das Format `rgba(R,G,B,A)`. Andernfalls können Sie das Format `#RRGGBB` verwenden.

## Allgemeine Elemente der Benutzeroberfläche {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Im Folgenden finden Sie die Referenzdokumentation zu Benutzeroberflächenelementen, die für den interaktiven Video-Viewer gilt:
