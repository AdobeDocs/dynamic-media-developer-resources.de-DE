---
title: Scene7 Version Herbst 2016
description: '"Die neuesten Versionshinweise für Adobe Scene7 Herbst 2016, Teil der Adobe Experience Manager-Lösung in der Adobe Experience Cloud."'
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '2209'
ht-degree: 0%

---

# Scene7 Version Herbst 2016{#scene-fall-release}

Die neuesten Versionshinweise zur Adobe Scene7-Herbstversion 2016, Teil der Adobe Experience Manager-Lösung in der Adobe Experience Cloud.

## Scene7 Version Herbst 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Die aktuellen Versionshinweise für [!DNL Adobe Scene7] Version Herbst 2016 [!DNL Adobe Experience Manager] in der [!DNL Adobe Experience Cloud].

* [Allgemein](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Viewer (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Viewer (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Viewer (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 Viewer-SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 und Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Allgemein {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe freut sich, die Bereitstellung von Inhalten über HTTP/2 mit dem allgemeinen Vorteil einer verbesserten Leistung bekannt zu geben.

Siehe [Häufig gestellte Fragen zur Bereitstellung von Inhalt über HTTP/2](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Die vollständige Dokumentation finden Sie unter [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Neue Funktionen, Verbesserungen und Fehlerbehebungen**

* Funktion zur Videoneuausgabe aus entfernt [!DNL Adobe Scene7 Publishing System] -Benutzeroberfläche.
* Authentifizierung für alle Scene7-Servlets hinzugefügt, wo dies erforderlich und möglich ist
* Fehlerbehebung bei der Listenansicht im Papierkorb.
* Entfernt **Dynamic Media Classic (Scene7)-Administrator erstellen** Benutzerfunktion aus User Management aus Sicherheitsgründen.
* FTP WebAdmin unterstützt jetzt die OKTA-Authentifizierung.
* Die Funktion des Standardkennworts, das für neue Media Portal-Benutzer erstellt wurde, wurde entfernt.
* Fehlerbehebung für das temporäre Kennwort, das beim Hinzufügen eines neuen Benutzers generiert wurde. Das Kennwort entsprach nicht den erforderlichen Kennwortanforderungen.
* Behobene Probleme mit WebAdmin root disk full.
* Fehlerkorrektur - die Deaktivierung eines Benutzers wird nicht sofort in der Benutzeroberfläche angezeigt.
* Fehlerbehebung beim Löschen eines Benutzers, der es nicht ermöglichte, den Benutzer später erneut zu erstellen.
* Fehlerkorrektur - die Begrüßungs-E-Mail wird an neue Scene7-Benutzer gesendet, die keine Authentifizierung zur Steuerung bestimmter Einstellungen enthalten.
* Fehlerkorrektur - Es wurde eine FTP-Ordnerliste nicht mehr abgerufen, wenn ein Ordner Sonderzeichen im Namen hatte.
* Konfigurieren Sie die OKTA-Dienstanbieter für Scene7-Umgebungen.
* Unterstützung für Experience Cloud-Organisations-ID für Viewer Analytics hinzugefügt.
* Scene7 SAML-Consumer implementiert.

## Viewer (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Die vollständige Dokumentation finden Sie unter [Viewer-Referenzhandbuch](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Fehlerkorrekturen für Image Serving 5.5.3**

* Kompatibilität mit RequireJS- und DOJO-Bibliotheken.

   Konsolidiertes SDK-JS-Caching während der Viewer-Implementierung.

## Viewer (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Die vollständige Dokumentation finden Sie unter [Viewer-Referenzhandbuch](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Fehlerkorrekturen für Image Serving 5.5.2**

* Video konnte in Internet Explorer 11 unter Windows 7 nicht wiedergegeben werden.
* `initialframe` hatte keine Auswirkungen auf den Hochformat-Modus auf Mobilgeräten für HTML5 eCatalog.

## Viewer (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Die vollständige Dokumentation finden Sie unter [Viewer-Referenzhandbuch](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Neue Funktionen, Verbesserungen und Fehlerbehebungen für Image Serving 5.5.1**

* HTML5 eCatalog-Viewer mit Suchfunktion.
* Die HLS-Streaming-Videowiedergabe wurde als standardmäßige Videobereitstellungsmethode für die meisten Desktop-Systeme hinzugefügt. Flash-basiertes HDS-Video-Streaming ist weiterhin als alternative Wiedergabeoption verfügbar.
* Unterstützung für Geräte mit Maus- und Touch-Eingabe hinzugefügt, die im Chrome-Browser ausgeführt werden.
* Die Analytics-Integration wird nun mit der Experience Cloud-Organisations-ID unterstützt.
* Aktualisierung der AppMeasurement JavaScript-Bibliothek auf Version 1.6.1.
* Unterstützung für die Ausrichtung von rechts nach links im E-Katalog-Viewer hinzugefügt.
* Problem behoben, bei dem `tip=0,-1,0` einen Fehler außerhalb des Bereichs verursacht hat.

**Kompatibilitätshinweise**

* BlackBerry®

   * Inkompatibilität mit älteren AVS-Sets. Clients müssen AVS-Sets erneut hochladen, um die Wiedergabe zu ermöglichen.

* Allgemein

   * Die Browser-seitige Skalierung kann dazu führen, dass die Benutzeroberfläche und Bilder beim Vergrößern der Seite durch den Benutzer verschwommen werden. Die Formatierung der Benutzeroberfläche wird je nach Zoom möglicherweise auch falsch angezeigt. Dieser Effekt wird auf den Vollbildmodus übertragen.
   * Aufgrund der Größenbeschränkung auf Mobilgeräten verwendet der Viewer für gemischte Medien eine Foliengeste, um Frames in eingebetteten Bildsets zu tauschen, anstatt auf die eingebettete Farbfeldkomponente zu tippen. Die Komponente ist als visueller Indikator vorhanden.
   * In Internet Explorer-Browsern und einigen Touch-Geräten belegt der Vollbildmodus nicht den gesamten Gerätebildschirm. Stattdessen wird die Größe der Anwendung an die Größe des Browser-Fensters angepasst.
   * Die Schaltfläche &quot;Schließen&quot;funktioniert nicht in iOS 8.0 und 8.1, tritt jedoch nicht mehr in iOS 8.2 auf

* Galaxy SIII

   * Speicherleck bei Zoom- und eCatalog HTML5-Viewern. Eine wiederholte Navigation durch Frames kann zum Absturz des Browsers führen.
   * Doppeltippen auf den Viewer kann dazu führen, dass die ganze Seite vergrößert wird, anstatt dass nur der Viewer mit aktivierter Browser-seitiger Skalierung angezeigt wird.

* Galaxy S4

   * Gerät als Tablet im Hochformat erkannt, wobei Vollbild in den Browsereinstellungen aktiviert ist.

* Galaxy Nexus

   * Doppeltippen auf den Viewer kann dazu führen, dass die ganze Seite vergrößert wird, anstatt dass nur der Viewer mit aktivierter Browser-seitiger Skalierung angezeigt wird.

* Galaxy Nexus 10 und Galaxy Tablet

   * eCatalog mit falscher Seitenausrichtung im Hoch- und Querformat.

* HTC-Mobilgeräte

   * Die Ergebnisse der HTC-Adobe für Mobilgeräte zeigen, dass die Unmöglichkeit, natives Pinch-Zoom zu deaktivieren, eine &quot;Funktion&quot;des HTC UI-Wrapper (HTC Sense) ist. Dieses Problem kann dazu führen, dass die gesamte Seite beim Verwenden der Geste &quot;Pinch to Zoom&quot;im Viewer vergrößert wird. Verwenden Sie stattdessen Doppeltippen.
   * Imagemap-Symbole können sich überschneiden, wenn Imagemaps klein sind und nahe beieinander liegen.

* HTML5-Video

   * Internet Explorer 9: benutzerdefinierte Posterbilder werden nicht angezeigt.
   * `IntialBitRate` -Modifikator wird nur bei Software-HLS- und Flash-HDS-Wiedergabe unterstützt. Es funktioniert nicht, wenn die Wiedergabe den nativen Player verwendet.
   * Die progressive OGG- und WebM-Wiedergabe wird derzeit nicht unterstützt.
   * Die Browserskalierung kann dazu führen, dass der Videoplayer eine falsche Größe anzeigt (einschließlich Anzeigeeinstellungen für das Windows OS-Control Panel).
   * Die Videosuche mit HLS-Streaming in Safari kann inkonsistent sein.

* Internet Explorer

   * Der Quirks-Modus wird derzeit nicht unterstützt.
   * Der Kompatibilitätsmodus wird derzeit nicht unterstützt.
   * Internet Explorer auf Mobilgeräten wird derzeit nicht unterstützt.

* iOS

   * Große E-Kataloge können zu einem Browserabsturz auf iPad 2 führen.
   * iPhone 6+ Telefone werden von den Viewern als Tablets erkannt.

* Safari

   * Safari 6.1 oder höher: Einstellungen für Internet-Plug-ins können die Videowiedergabe von Flashs verhindern.
   * Das &quot;Suchen&quot;von Videos mit HLS-Streaming in Safari kann inkonsistent sein.
   * Das Ende des Videos in Safari 6 kann nicht mithilfe von HLS-Streaming gesucht werden.

**Bekannte Probleme und Einschränkungen**

* Die Image Serving-Modifikatoren von `iscommands` werden nicht zum `req=set` Anforderung nach Entwurf. Modifikatoren, die sich nur auf die Bildanzeige auswirken, funktionieren einwandfrei. Modifikatoren, die sich auf die Größe auswirken, müssen in einem komplexen Asset verwendet werden. Beispiel:

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [Flyout] IE9 bleibt manchmal auf dem Bildschirm, wenn die Maus ausgeschaltet ist.
* Die Browserskalierung führt zu einer falschen Größenanpassung.
* iPad 2: Große eCatalog-Assets stürzen Safari auf iOS ab.
* Alle Viewer

   * Wasserzeichen, Verschleierung und Sperren werden nicht unterstützt.
   * Bildvorgaben werden nicht unterstützt.
   * Hinzufügen oder Entfernen des Viewers aus dem DOM mithilfe von `display:none` CSS oder durch dynamisches Trennen vom übergeordneten Knoten wird derzeit nicht unterstützt.

* HTML 5 Alle Viewer

   * Das Einbetten des Viewers in eine Tabelle kann zu einer falschen Größe oder Platzierung des Viewers im nicht nativen Vollbildmodus führen. Verwenden Sie stattdessen DIVs.
   * Parameter mit expliziten Instanznamen im Code erfordern, dass auch Instanznamen in der URL überschrieben werden (z. B. `zoomView.iconfeffect=0`).
   * Image Serving-Befehlszuschnitt wird derzeit nicht unterstützt.
   * Die Schaltfläche Schließen funktioniert nur, wenn der Viewer im untergeordneten Fenster geöffnet ist.
   * Die `iscommands` -Modifikator unterstützt keine Image Serving-Modifikatoren, die sich auf die Bildgröße auswirken.

* HTML5 eCatalog

   * Wenn Sie zu einer anderen HTML-Seite navigieren und sie zurückgeben, führt dies gelegentlich dazu, dass der Viewer auf die erste Seite zurückgesetzt wird.
   * Gelegentlich wird das Seitenlayout nach dem Drehen des iOS-Geräts falsch angezeigt. Durch das Vergrößern der Seite wird das Layout korrigiert.
   * Interne Links führen nur zu der am weitesten links gelegenen Seite in mehrseitigen Tabellen. Betrifft Mobilgeräte im Hochformat.
   * InitialFrame verknüpft nur mit der ganz links gelegenen Seite in mehrseitigen Tabellen. Betrifft Mobilgeräte im Hochformat.
   * Aufgrund von Browserbeschränkungen ist die Druckfunktion in IE9 nicht verfügbar.

* HTML5 MixedMedia

   * Soundtrack-Wiedergabe wird nicht unterstützt.

* HTML5 Social

   * Um Miniaturansichten in ausgehenden E-Mails korrekt zu rendern, muss die `serverurl` -Modifikator muss über eine absolute URL verfügen.

* HTML5-Video

   * Beim Posterbild kann der Fehler &quot;max size&quot;auftreten. Das Unternehmen muss die Einstellung für die Beschränkung für die Veröffentlichung auf Image Serving erhöhen.
   * Für Videountertitel ist ein Regelsatz erforderlich, wenn das Hosting der HTML-Seite von einem externen Server (nicht von einem Scene7-Server) aus erfolgt. Wenden Sie sich für Unterstützung an den Support der Adobe.
   * Das Analytics-Tracking meldet aufgrund der Pufferung möglicherweise einen falschen Wiedergabeprozentsatz
   * Auf iPad- oder Android™-Geräten wird möglicherweise ein schwarzer Frame anstelle eines Standbilds angezeigt.
   * Beim Laden des Viewers auf iPad- oder Android™-Geräten blinkt möglicherweise ein schwarzer Frame auf dem Bildschirm.
   * Auf iPad-Geräten werden schwarze Rahmen neben der VideoPlayer-Komponente angezeigt, wenn der Hintergrund auf Weiß/Transparent eingestellt ist.
   * Der letzte Videobild kann in iPad mit iOS 7 verzerrt sein.
   * Gelegentlich kann es bei der Videosuche im HLS-Streaming-Modus in Chrome-, Firefox- und Internet Explorer-Browsern zu Makroblockierungen kommen.
      * Das Posterbild wird im Microsoft® Edge-Browser möglicherweise nicht zum ersten Mal angezeigt.
      * Das Standbild kann sich nach dem Laden des Videos in Internet Explorer 9 verbergen, wenn die progressive Wiedergabe verwendet wird.

## Scene7 HTML5 Viewer-SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

Das Benutzerhandbuch befindet sich im Ordner Adobe HTML5 Viewer SDK der Client-Installation. Die Dokumentation zur Komponenten-API finden Sie im Unterordner docs der Client-Installation.

**Fehlerbehebungen für 3.0.2**

* VideoPlayer - Video konnte in Internet Explorer 11 unter Windows 7 nicht wiedergegeben werden.
* TableOfContents -  `initialframe` hatte keine Auswirkungen auf den Hochformat-Modus auf Mobilgeräten für HTML5 eCatalog-Viewer.

**Neue Funktionen, Verbesserungen und Fehlerbehebungen für 3.0.1**

* Allgemein

   * Die HLS-Streaming-Videowiedergabe wurde als standardmäßige Videobereitstellungsmethode für die meisten Desktop-Systeme hinzugefügt. Flash-basiertes HDS-Video-Streaming ist weiterhin als alternative Wiedergabeoption verfügbar.
   * Die Komponenten SearchManager, SearchPanel, SearchEffect und SearchButton wurden hinzugefügt, um die neue Suchfunktion in eCatalog-Viewern zu unterstützen.
   * Unterstützung für Geräte mit Maus- und Touch-Eingabe im Chrome-Browser hinzugefügt.
   * Die Android™-Versionserkennung wurde überarbeitet, um zukünftige Versionen des Betriebssystems zu unterstützen.
   * Unterstützung für die Ausrichtung von rechts nach links in eCatalog-spezifischen SDK-Komponenten.

* ControlBar

   * Es wurde ein optionaler Bildlauf für ControlBar-Inhalt hinzugefügt, falls dieser nicht in die verfügbare Breite passt.

* FlyoutzoomView

   * Fester Fall, wenn `tip=0,-1,0` einen Fehler außerhalb des Bereichs verursacht hat.

**Kompatibilitätshinweise**

* Android™ 4.x

   * Um die Standardeinstellung zu deaktivieren, muss die folgende CSS-Regel für die Komponente blau markiert werden:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * Die Videowiedergabe kann beim Ändern von Bitratenströmen in AVS-Sets beendet werden.

* Chrome

   * Alle API-Aufrufe, die die Neuerstellung von Komponenten erzwingen, können aufgrund der internen Zwischenspeicherung von Chrome ignoriert werden.

* Galaxy SIII

   * Der Viewer kann manchmal nicht in den Vollbildmodus geladen werden.
   * Die Seitenansicht leidet derzeit an einem Speicherleck auf dem Gerät.
   * Durch Doppeltippen-Geste werden der Viewer und die Seite vergrößert, wenn die Browser-seitige Skalierung aktiv ist.

* Galaxy Nexus

   * Artefakte, die über einigen Ansichtskomponenten angezeigt werden.
   * Durch Doppeltippen-Geste werden der Viewer und die Seite vergrößert, wenn die Browser-seitige Skalierung aktiv ist.

* iPad 3

   * Die iPad 3 verfügt über eine native Auflösung von 2048 x 1536. Diese Lösung kann Anzeigeprobleme verursachen, wenn die IS-Veröffentlichung des Unternehmens, die Bildgrößenbeschränkung, niedriger ist.

* iPhone4

   * Symbol &quot;Wiederholung der Symbolwiedergabe&quot;wurde nach dem Scrollen der Seite durch das Wiedergabesymbol ersetzt.

* Internet Explorer

   * Im IE 10 und älteren Vollbildmodus wird nicht der gesamte Bildschirm angezeigt, sondern nur die Größe der Anwendung auf die Größe des Browserfensters geändert.
   * Der Rendermodus &quot;Quirks&quot;wird nicht unterstützt.
   * Internet Explorer auf Mobilgeräten wird derzeit nicht unterstützt.
   * Wenn Util.js asynchron eingeschlossen ist, kann es sein, dass das Laden von Util.js fehlschlägt.
   * Symbol &quot;IconEffect&quot;blockiert Klickereignisse in den Komponenten SpinView und ZoomView .

* Native Geräte-Videoplayer

   * Die Ebenen-UI-Komponenten über VideoPlayer werden nicht unterstützt, wenn VideoPlayer zum Aufrufen des nativen Players des Geräts verwendet wird.
   * Die Videowiedergabe im nativen Modus ist in Safari 6 inkonsistent.
   * Die native Wiedergabe ersetzt das Wiederholungssymbol durch das Wiedergabesymbol nach dem Scrollen der Seite.

* Touch-Geräte

   * Der Vollbildmodus belegt nicht den gesamten Gerätebildschirm, sondern ändert lediglich die Größe der Anwendung auf die Größe des Browser-Fensters.
   * Benutzerdefinierte Cursor funktionieren nicht auf Touch-Geräten.
   * Die Seitenskalierung auf Touch-Geräten wird derzeit nicht unterstützt. Für das Einbetten von HTML5-Viewern ist ein Viewport-Meta-Tag mit entsprechenden Einstellungen erforderlich.

* Xoom

   * Durch Doppeltippen-Geste werden der Viewer und die Seite vergrößert, wenn die Browser-seitige Skalierung aktiv ist.

**Bekannte Probleme und Einschränkungen**

* Alle Komponenten

   * In den Versionen 2.7.2 und früher wurden einige Komponenten zum DOM hinzugefügt, indem `insertBefore()` API. Daher würden sich solche Komponenten in der Stapelreihenfolge am unteren Rand befinden, unabhängig davon, ob die Komponenteninstanz relativ zu anderen Komponenten erstellt wird. Ab Version 2.8.1 verwenden alle Komponenten `appendChild()` API jetzt, was bedeutet, dass die Komponentenstapelreihenfolge mit der Reihenfolge der Instanzerstellung übereinstimmt.

   * Verwenden `iscommand` -Modifikator zum Festlegen des Alphakanalformats nicht unterstützt. Komponente verwenden `FMT` -Parameter.
   * CSS-Transformationseigenschaft wird derzeit nicht unterstützt.

* Touch-Geräte

   * Pinch-Gesten auf Touch-Geräten generiert kein Zoom-Ereignis

* Behälter

   * Rahmen, Abstände und Ränder im Container werden nicht unterstützt. Adobe empfiehlt das Hinzufügen von Stilelementen zum übergeordneten DIV.
   * Muss explizit die Behältergröße festlegen, sonst kann die Größe der Komponenten korrekt sein.

* Druckkomponente

   * Aufgrund von Browserbeschränkungen skaliert die Druckkomponente in Internet Explorer 9 den Inhalt möglicherweise nicht ordnungsgemäß auf dem Papier.

* IconEffect-Komponente

   * IconEffect erzeugt in Internet Explorer einen Skriptfehler, wenn `autohide` ist deaktiviert (festgelegt auf `0`).

* ImageMapEffect-Komponente

   * Verzögerung mit Neupositionierungssymbol beim Schwenken des Bildes auf der Ansichtskomponente

* MediaSet-Komponente

   * Inline-Assets erfordern dieselbe Kodierung wie auf der URL.

* NavigationView-Komponente

   * Derzeit unterstützt die Komponente keine Größenanpassung.

* PageScrubber-Komponente

   * Wenn in iPhone 5 die &quot;PageScrubber&quot;-Blase auf &quot;text&quot;gesetzt ist, werden beim Verschieben der Schaltfläche entlang der Spur Artefakte angezeigt. Verwenden `-webkit-background-clip: content;` im Stil funktioniert um das Problem zu umgehen.

* SpinView-Komponente

   * SpinView scheint manchmal nach dem Wischen einzufrieren und das Gerät zu drehen, während das Bild gedreht wird.

* Farbfeldkomponente

   * Bei der Auswahl eines Out-of-Bounds-Musters werden zwei Highlights angezeigt.
   * Automatisches Scrollen mit `selectSwatch()` -Methode nicht korrekt funktioniert.

* VideoPlayer

   * Der Videoframe wird nicht aktualisiert, wenn die Suche auf 100 % festgelegt ist und der Fallback auf &quot;auto&quot;eingestellt ist.
   * Gelegentlich kann es während der Videosuche im HLS-Streaming-Modus in Chrome-, Firefox- und Internet Explorer-Browsern zu Makroblockierungen kommen.
   * Das Posterbild wird im Microsoft® Edge-Browser möglicherweise nicht zum ersten Mal angezeigt.
   * Das Standbild kann sich nach dem Laden des Videos in Internet Explorer 9 verbergen, wenn die progressive Wiedergabe verwendet wird.

## Dynamic Media Image Serving 6.3.2 und Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC-Dienstprogramm - `downsample2x2` -Markierung wird nicht mehr unterstützt. Diese Markierung war ein schlechter Downsampler von 2x2-Qualität, der nicht mehr von IPS verwendet wird.
* CORS-Kopfzeile - Derzeit ist der CORS-Header für `/is/content/` -Anfragen.
