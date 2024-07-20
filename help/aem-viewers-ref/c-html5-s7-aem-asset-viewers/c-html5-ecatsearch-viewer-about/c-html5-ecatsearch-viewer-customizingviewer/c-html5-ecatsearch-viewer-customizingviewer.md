---
title: Anpassen des eCatalog Search-Viewers
description: Die visuelle Anpassung und die meisten Verhaltensanpassungen für den eCatalog Search Viewer erfolgen durch Erstellen eines benutzerdefinierten CSS.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# Anpassen des eCatalog Search-Viewers{#customizing-ecatalog-search-viewer}

Die visuelle Anpassung und die meisten Verhaltensanpassungen für den eCatalog Search Viewer erfolgen durch Erstellen eines benutzerdefinierten CSS.

Der vorgeschlagene Workflow besteht darin, die Standard-CSS-Datei für den entsprechenden Viewer zu übernehmen, sie an einen anderen Speicherort zu kopieren, sie anzupassen und den Speicherort der angepassten Datei im Befehl `style=` anzugeben.

Standard-CSS-Dateien finden Sie unter folgendem Speicherort:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

Die benutzerdefinierte CSS-Datei muss dieselben Klassendeklarationen wie die Standarddatei enthalten. Wenn eine Klassendeklaration weggelassen wird, funktioniert der Viewer nicht ordnungsgemäß, da er keine integrierten Standardstile für die Elemente der Benutzeroberfläche bereitstellt.

Eine alternative Möglichkeit zur Bereitstellung benutzerdefinierter CSS-Regeln besteht darin, eingebettete Stile direkt auf der Webseite oder in einer der verknüpften externen CSS-Regeln zu verwenden.

Beachten Sie beim Erstellen von benutzerdefiniertem CSS, dass der Viewer dem Container-DOM-Element die Klasse `.s7ecatalogsearchviewer` zuweist. Wenn Sie eine externe CSS-Datei verwenden, die mit dem Befehl `style=` übergeben wird, verwenden Sie für Ihre CSS-Regeln die Klasse `.s7ecatalogsearchviewer` als übergeordnete Klasse im untergeordneten Selektor. Wenn Sie eingebettete Stile auf der Web-Seite verwenden, sollten Sie diesen Selektor wie folgt mit einer ID des Container-DOM-Elements qualifizieren:

`#<containerId>.s7ecatalogsearchviewer`

## Erstellen von responsiv gestaltetem CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

Es ist möglich, verschiedene Geräte anzusprechen und Größen in CSS einzubetten, damit Ihre Inhalte je nach Gerät eines Benutzers oder Layout einer bestimmten Webseite unterschiedlich angezeigt werden. Dieses Targeting umfasst, aber nicht ausschließlich, verschiedene Webseitenlayouts, Elementgrößen der Benutzeroberfläche und die Auflösung von Grafiken.

Der Viewer unterstützt zwei Methoden zum Erstellen von responsiv gestaltetem CSS: CSS-Markierungen und Standard-CSS-Medienabfragen. Sie können diese Methoden unabhängig oder gemeinsam verwenden.

**CSS-Markierungen**

Um responsives CSS zu erstellen, unterstützt der Viewer CSS-Markierungen, die spezielle CSS-Klassen darstellen, die dynamisch dem Viewer-Container-Element der obersten Ebene basierend auf der Laufzeit-Viewer-Größe und dem Eingabetyp auf dem aktuellen Gerät zugewiesen werden.

Die erste Gruppe von CSS-Markern umfasst die Klassen `.s7size_large`, `.s7size_medium` und `.s7size_small`. Sie werden basierend auf dem Laufzeitbereich des Viewer-Containers angewendet. Das heißt, wenn der Viewer-Bereich gleich oder größer als die Größe eines gemeinsamen Desktop-Monitors `.s7size_large` ist. Wenn der Bereich nahe an einem gemeinsamen Tablet-Gerät liegt, wird `.s7size_medium` zugewiesen. Für Bereiche ähnlich wie Mobiltelefonbildschirme. Die Markierung `.s7size_small` wird gesetzt. Der Hauptzweck dieser CSS-Markierungen besteht darin, verschiedene Benutzeroberflächen-Layouts für verschiedene Bildschirme und Viewer-Größen zu erstellen.

Die zweite Gruppe von CSS-Markierungen umfasst `.s7mouseinput` und `.s7touchinput`. Die Markierung `.s7touchinput` wird gesetzt, wenn das aktuelle Gerät Touch-Eingabefunktionen aufweist. Andernfalls wird `.s7mouseinput` verwendet. Diese Markierungen dienen zur Erstellung von Eingabeelementen der Benutzeroberfläche mit unterschiedlichen Bildschirmgrößen für verschiedene Eingabetypen, da Touch-Eingaben normalerweise größere Elemente erfordern. Falls das Gerät sowohl über eine Maus- als auch Touch-Funktion verfügt, wird `.s7touchinput` eingestellt und der Viewer rendert eine Touch-optimierte Benutzeroberfläche.

Im folgenden Beispiel-CSS wird die Größe der Zoom-Schaltfläche auf 28 x 28 Pixel bei Systemen mit Mauseingabe und auf Touch-Geräten auf 56 x 56 Pixel eingestellt. Darüber hinaus wird die Schaltfläche vollständig ausgeblendet, wenn die Viewer-Größe zu klein wird:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7ecatalogsearchviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Verwenden Sie CSS-Medienabfragen, um Geräte mit einer anderen Pixeldichte als Ziel auszuwählen. Der folgende Medienabfrageblock enthält CSS, das speziell für High-Density-Bildschirme gilt:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Die Verwendung von CSS-Markern ist die flexibelste Möglichkeit, responsives CSS zu erstellen. Damit können Sie nicht nur die Bildschirmgröße des Geräts, sondern auch die tatsächliche Viewer-Größe bestimmen, was für responsive Seitenlayouts nützlich ist.

Verwenden Sie die standardmäßige Viewer-CSS-Datei als Beispiel für einen CSS-Marker-Ansatz.

**CSS-Medienabfragen**

Die Geräteerkennung kann auch mit reinen CSS-Medienabfragen durchgeführt werden. Alles, was in einem bestimmten Medienabfrageblock eingeschlossen ist, wird nur angewendet, wenn er auf einem entsprechenden Gerät ausgeführt wird.

Verwenden Sie bei Anwendung auf Mobile Viewer vier CSS-Medienabfragen, die in Ihrem CSS in der folgenden Reihenfolge definiert sind:

1. Enthält nur für alle Touch-Geräte spezifische Regeln.

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

## CSS-Sprites {#section-9d570f95eb2443aca74c1b02f6e89aff}

Viele Elemente der Viewer-Benutzeroberfläche werden mit Bitmap-Grafiken formatiert und weisen mehr als einen bestimmten visuellen Status auf. Ein gutes Beispiel ist eine Schaltfläche mit normalerweise mindestens drei verschiedenen Status: &quot;up&quot;, &quot;over&quot;und &quot;down&quot;. Jeder Status erfordert eine eigene Bitmap-Grafik, die zugewiesen wird.

Bei einem klassischen Stil würde CSS für jeden Status des Benutzeroberflächenelements einen separaten Verweis auf die einzelne Bilddatei auf dem Server haben. Im Folgenden finden Sie ein Beispiel-CSS zum Formatieren einer Zoom-in-Schaltfläche:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Der Nachteil dieses Ansatzes besteht darin, dass der Endbenutzer flackernde oder verzögerte Antworten auf die Benutzeroberfläche erfährt, wenn das Element zum ersten Mal verwendet wird. Diese Aktion tritt auf, da die Bildgrafik für den neuen Elementstatus noch nicht heruntergeladen wurde. Dieser Ansatz kann sich aufgrund der gestiegenen Anzahl an HTTP-Aufrufen an den Server auch geringfügig negativ auf die Leistung auswirken.

CSS-Sprites ist ein anderer Ansatz, bei dem Bildgrafiken für alle Elementzustände in einer PNG-Datei namens &quot;Sprite&quot;kombiniert werden. Ein solches &quot;Sprite&quot;hat alle visuellen Status für das jeweilige Element, das nacheinander positioniert wird. Beim Formatieren eines Benutzeroberflächenelements mit Sprites wird für alle verschiedenen Status in CSS auf dasselbe Sprite-Bild verwiesen. Außerdem wird mit der Eigenschaft &quot;`background-position`&quot;für jeden Status angegeben, welcher Teil des &quot;Sprite&quot;-Bildes verwendet wird. Sie können ein &quot;Sprite&quot;-Bild auf jede geeignete Weise strukturieren. Normalerweise wird sie von Viewern vertikal gestapelt. Nachfolgend finden Sie ein &quot;sprite&quot;-basiertes Beispiel für die Formatierung der gleichen Zoom-in-Schaltfläche von oben:

```
.s7ecatalogsearchviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
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

Im Folgenden finden Sie die Referenzdokumentation zu Elementen der Benutzeroberfläche, die für den eCatalog Search Viewer gilt:

* [Schaltfläche &quot;Favoriten hinzufügen&quot;](r-html5-ecatsearch-customize-addfavorite.md)
* [Schaltfläche schließen](r-html5-ecatsearch-customize-closebutton.md)
* [Download](r-html5-ecatsearch-customize-download.md)
* [Email Share](r-html5-ecatsearch-customize-emailshare.md)
* [Freigabe einbetten](r-html5-ecatsearch-customize-embedshare.md)
* [Facebook Share](r-html5-ecatsearch-customize-facebookshare.md)
* [Favoriteneffekt](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Favoriten, Menü](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Favoritenansicht](r-html5-ecatsearch-customize-favoritesview.md)
* [Schaltfläche &quot;Erste Seite&quot;](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Fokushervorhebung](r-html5-ecatsearch-customize-focushighlight.md)
* [Schaltfläche im Vollbildmodus](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Symboleffekt](r-html5-ecatsearch-customize-iconeffect.md)
* [Popup für Infobereich](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Bild-Map-Effekt](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Schaltfläche &quot;Weiter&quot;](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Schaltfläche &quot;Große vorherige Seite&quot;](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Schaltfläche &quot;Letzte Seite&quot;](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Linkfreigabe](r-html5-ecatsearch-customize-linkshare.md)
* [Hauptrollleiste](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Hauptanzeige-Bereich](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Schaltfläche &quot;Nächste Seite&quot;](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Seitenanzeige](r-html5-ecatsearch-customize-pageindicator.md)
* [Seitenansicht](r-html5-ecatsearch-customize-pageview.md)
* [Schaltfläche &quot;Vorherige Seite&quot;](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Drucken](r-html5-ecatsearch-customize-print.md)
* [Schaltfläche &quot;Favoriten entfernen&quot;](r-html5-ecatsearch-customize-removefavorite.md)
* [Suchschaltfläche](r-html5-ecatsearch-customize-searchbutton.md)
* [Sucheffekt](r-html5-ecatsearch-customize-searcheffect.md)
* [Suchergebnisbereich](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Sekundäre Steuerleiste](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Social Share](r-html5-ecatsearch-customize-socialshare.md)
* [Inhaltsverzeichnis](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniaturen](r-html5-ecatsearch-customize-thumbnails.md)
* [Schaltfläche &quot;Miniaturansichten&quot;](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Tooltips](r-html5-ecatsearch-customize-tooltips.md)
* [Twitter Share](r-html5-ecatsearch-customize-twittershare.md)
* [Schaltfläche &quot;Alle Favoriten anzeigen&quot;](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Schaltfläche &quot;Vergrößern&quot;](r-html5-ecatsearch-customize-zoominbutton.md)
* [Schaltfläche &quot;Auszoomen&quot;](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Schaltfläche &quot;Zoom zurücksetzen&quot;](r-html5-ecatsearch-customize-zoomresetbutton.md)
