---
description: Die neuesten Versionshinweise für Adobe Scene7 Herbst 2016, Teil der Adobe Experience Manager-Lösung in der Adobe Marketing Cloud.
seo-description: Die neuesten Versionshinweise für Adobe Scene7 Herbst 2016, Teil der Adobe Experience Manager-Lösung in der Adobe Marketing Cloud.
seo-title: Scene7 Version Herbst 2016
solution: Experience Manager
title: Scene7 Version Herbst 2016
topic: Dynamic media
uuid: 3fddda65-0c6e-48ec-bd60-7e0ca59421a8
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2263'
ht-degree: 0%

---


# Scene7 Version Herbst 2016{#scene-fall-release}

Die neuesten Versionshinweise für Adobe Scene7 Herbst 2016, Teil der Adobe Experience Manager-Lösung in der Adobe Marketing Cloud.

## Scene7 Version Herbst 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Die neuesten Versionshinweise für [!DNL Adobe Scene7] Herbstversion 2016 der [!DNL Adobe Experience Manager]-Lösung in [!DNL Adobe Marketing Cloud].

* [Allgemein](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7 Publishing System](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Viewer (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Viewer (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Viewer (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Scene7 HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Scene7 Image Serving 6.3.2 und Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Allgemein {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe freut sich, die Verfügbarkeit von HTTP/2-Versänden mit dem allgemeinen Vorteil einer verbesserten Performance bekannt zu geben.

Siehe [HTTP2-Versand der Content FAQ](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7/http2faq.html).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Die vollständige Dokumentation finden Sie unter [https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html)

**Neue Funktionen, Verbesserungen und Fehlerbehebungen**

* Die Videoneuschnitt-Funktion wurde aus der [!DNL Adobe Scene7 Publishing System]-Benutzeroberfläche entfernt.
* Es wurde nach Bedarf und nach Möglichkeit eine Authentifizierung für alle Scene7-Servlets hinzugefügt.
* Fehlerkorrektur mit der Ansicht der Liste im Papierkorb.
* Die Benutzerfunktion **SPSAdmin** aus User Management wurde aus Sicherheitsgründen entfernt.
* FTP WebAdmin unterstützt jetzt die OKTA-Authentifizierung.
* Die Funktion des Standardkennworts für neue Media Portal-Benutzer wurde entfernt.
* Fehlerkorrektur mit dem temporären Kennwort, das beim Hinzufügen eines neuen Benutzers generiert wurde. Das Kennwort entsprach nicht den erforderlichen Kennwortanforderungen.
* Es wurden Probleme mit WebAdmin-Root-Disk vollständig behoben.
* Fehlerkorrektur, bei der ein Benutzer deaktiviert wird, der nicht sofort in der Benutzeroberfläche angezeigt wird.
* Fehlerkorrektur, bei der ein Benutzer gelöscht wurde, ohne dass Sie ihn später erneut erstellen konnten.
* Fehlerbehebung, bei der die Begrüßungs-E-Mail an neue Scene7-Benutzer gesendet wurde, die keine Authentifizierung zur Steuerung bestimmter Einstellungen enthielten.
* Fehlerkorrektur, bei der eine Liste des FTP-Ordners nicht abgerufen werden konnte, wenn ein beliebiger Ordner Sonderzeichen enthielt.
* Konfigurieren Sie OKTA-Dienstleister für Scene7-Umgebung.
* Unterstützung für Marketing Cloud-Organisations-ID für Viewer-Analytics hinzugefügt.
* Scene7 SAML-Consumer implementiert.

## Viewer (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Eine vollständige Dokumentation finden Sie unter [Viewer-Referenzhandbuch](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Fehlerbehebungen für Image Serving 5.5.3**

* Kompatibilität mit RequireJS- und DOJO-Bibliotheken.

   Konsolidierte SDK-JS-Zwischenspeicherung während der Viewer-Bereitstellung.

## Viewer (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Eine vollständige Dokumentation finden Sie unter [Viewer-Referenzhandbuch](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Fehlerbehebungen für Image Serving 5.5.2**

* Video konnte in Internet Explorer 11 unter Windows 7 nicht wiedergegeben werden.
* `initialframe` hatte keine Auswirkungen auf den Hochformat-Modus auf Mobilgeräten für den HTML5-E-Katalog.

## Viewer (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Eine vollständige Dokumentation finden Sie unter [Viewer-Referenzhandbuch](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Neue Funktionen, Verbesserungen und Fehlerkorrekturen für Image Serving 5.5.1**

* HTML5-E-Katalog-Viewer mit Suchfunktion.
* HLS-Streaming-Video-Wiedergabe als Standard-Video-Versand für die meisten Desktop-Systeme hinzugefügt. Flash-basiertes HDS-Video-Streaming ist weiterhin als alternative Wiedergabemöglichkeit verfügbar.
* Unterstützung für Geräte mit Maus- und Berührungseingabe unter Chrome Browser hinzugefügt.
* Marketing Cloud-Organisations-ID-Unterstützung zur Analytics-Integration hinzugefügt.
* Aktualisieren Sie die AppMeasurement JavaScript-Bibliothek auf Version 1.6.1.
* Unterstützung für die Ausrichtung von rechts nach links im E-Katalog-Viewer hinzugefügt.
* Behebung eines Problems, bei dem `tip=0,-1,0` einen Fehler in Bezug auf die Entfernung verursachte.

**Anmerkungen zur Kompatibilität**

* Blackberry

   * Inkompatibilität mit älteren AVS-Sets. Kunden müssen möglicherweise AVS-Sets erneut hochladen, um die Wiedergabe zu ermöglichen.

* Allgemein

   * Die seitliche Skalierung des Browsers kann dazu führen, dass die Benutzeroberfläche und die Bilder verschwommen werden, wenn der Benutzer die Seite vergrößert. Die Formatierung der Benutzeroberfläche wird ggf. je nach Zoom falsch angezeigt. Dies wird in den Vollbildmodus übertragen.
   * Aufgrund der Größenbeschränkung auf Mobilgeräten verwendet der Viewer für gemischte Medien eine Foliengeste, um Frames in eingebetteten Bildsätzen auszutauschen, anstatt auf die Komponente für eingebettete Farbfelder zu tippen. Die Komponente ist als visueller Indikator vorhanden.
   * In Internet Explorer-Browsern und einigen Touch-Geräten belegt der Vollbildmodus nicht den gesamten Gerätebildschirm. Stattdessen wird die Größe der Anwendung an die Größe des Browser-Fensters angepasst.
   * Die Schaltfläche &quot;Schließen&quot;funktioniert nicht unter iOS 8.0 und 8.1, tritt aber nicht mehr unter iOS 8.2 auf

* Galaxy SIII

   * Speicherleck bei HTML5-Viewern im Zoom- und E-Katalog. Wiederholte Navigation durch Frames kann zu einem Absturz des Browsers führen.
   * Durch Tippen auf die Dublette im Viewer kann es vorkommen, dass die ganze Seite gezoomt wird und nicht nur der Viewer mit aktivierter Browser-Seitenanpassung.

* Galaxy S4

   * Gerät, das im Hochformat als Tablet erkannt wird und bei Vollbild in den Browsereinstellungen aktiviert ist.

* Galaxie Nexus

   * Durch Tippen auf die Dublette im Viewer kann es vorkommen, dass die ganze Seite gezoomt wird und nicht nur der Viewer mit aktivierter Browser-Seitenanpassung.

* Galaxy Nexus 10 und Galaxy Tablet

   * E-Katalog mit falscher Seitenausrichtung im Hoch- und Querformat

* HTC-Mobilgeräte

   * HTC-Mobilgeräte unsere Ergebnisse zeigen, dass die Unfähigkeit, natives Pinch-Zoom zu deaktivieren, eine &quot;Funktion&quot; des HTC UI Wrapper (HTC Sense) ist. Dies kann dazu führen, dass die ganze Seite beim Verwenden der Geste &quot;Zum Zoomen ziehen&quot;im Viewer gezoomt wird. Verwenden Sie stattdessen Dublette-Tippen.
   * Imagemap-Symbole können sich überlappen, wenn Imagemaps klein und nahe beieinander sind.

* HTML5-Video

   * Internet Explorer 9: benutzerdefinierte Standbilder werden nicht angezeigt.
   * `IntialBitRate` -Modifikator wird nur für die Wiedergabe von Software-HLS und Flash-HDS unterstützt. Es funktioniert nicht, wenn die Wiedergabe den nativen Player verwendet.
   * Die progressive Wiedergabe von OGG und WebM wird derzeit nicht unterstützt.
   * Die Browser-Skalierung kann dazu führen, dass der Videoplayer in einer falschen Größe angezeigt wird (einschließlich der Anzeigeeinstellungen des Windows OS-Bedienfelds)
   * Die Suche nach Videos mit HLS-Streaming in Safari kann inkonsistent sein.

* Internet Explorer

   * Der Quirks-Modus wird derzeit nicht unterstützt.
   * Der Kompatibilitätsmodus wird derzeit nicht unterstützt.
   * Internet Explorer auf Mobilgeräten wird derzeit nicht unterstützt.

* iOS

   * Große E-Kataloge können auf dem iPad 2 zum Absturz des Browsers führen.
   * iPhone 6+-Telefone werden von den Viewern als Tablets erkannt.

* Safari

   * Safari 6.1 oder höher: Die Einstellungen für Internet-Plug-ins können die Videowiedergabe im Flash verhindern.
   * Video-Suche mit HLS-Streaming in Safari kann inkonsistent sein.
   * Es kann nicht versucht werden, das Ende des Videos in Safari 6 mithilfe des HLS-Streaming zu suchen.

**Bekannte Probleme und Einschränkungen**

* Die Image Serving-Modifikatoren von `iscommands` werden der `req=set`-Anforderung nicht standardmäßig hinzugefügt. Modifikatoren, die sich nur auf die Bildanzeige auswirken, funktionieren einwandfrei. Modifikatoren, die sich auf die Größe auswirken, müssen in einem komplexen Asset verwendet werden. Beispiel:

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [] FlyoutIE9 bleibt manchmal nach dem Ausschalten der Maus auf dem Bildschirm.
* Die Browser-Skalierung führt zu einer falschen Größenanpassung.
* iPad 2: Ein großes E-Katalog-Asset stürzt Safari unter iOS ab.
* Alle Viewer

   * Wasserzeichen, Verschleierung und Sperren werden nicht unterstützt.
   * Bildvorgaben werden nicht unterstützt.
   * Das Hinzufügen oder Entfernen des Viewers aus dem DOM mithilfe von CSS `display:none` oder durch dynamisches Entfernen des Viewers vom übergeordneten Knoten wird derzeit nicht unterstützt.

* HTML5 Alle Viewer

   * Das Einbetten des Viewers in die Tabelle kann zu einer fehlerhaften Größe oder Platzierung des Viewers im nicht nativen Vollbildmodus führen. Verwenden Sie stattdessen DIVs.
   * Parameter mit expliziten Instanznamen im Code erfordern auch Instanznamen in der URL, die überschrieben werden müssen (z. B. `zoomView.iconfeffect=0`).
   * Die Beschneidung des Image Serving-Befehls wird derzeit nicht unterstützt.
   * Die Schaltfläche &quot;Schließen&quot;funktioniert nur, wenn der Viewer im untergeordneten Fenster geöffnet ist.
   * Der Modifikator `iscommands` unterstützt keine Image Serving-Modifikatoren, die sich auf die Bildgröße auswirken.

* HTML5-E-Katalog

   * Wenn Sie zu einer anderen HTML-Seite navigieren und gelegentlich zurückkehren, wird der Viewer auf die erste Seite zurückgesetzt.
   * Das Seitenlayout wird gelegentlich nach dem Drehen des iOS-Geräts falsch angezeigt. Durch das Vergrößern der Seite wird das Layout korrigiert.
   * Interne Links nur zur Seite ganz links in mehrseitigen Druckbögen. Betrifft Mobilgeräte im Hochformat.
   * InitialFrame verknüpft nur mit der Seite ganz links in mehrseitigen Druckbögen. Betrifft Mobilgeräte im Hochformat.
   * Aufgrund von Browserbeschränkungen ist die Druckfunktion in IE9 nicht verfügbar.

* HTML5 MixedMedia

   * Soundtrack-Wiedergabe wird derzeit nicht unterstützt.

* HTML5 Social

   * Um Miniaturansichten in ausgehenden E-Mails korrekt wiedergeben zu können, muss der Modifikator `serverurl` über eine absolute URL verfügen.

* HTML5-Video

   * Beim Standbild kann der Fehler &quot;max. Größe&quot;auftreten. Bei der Firma müssen Sie möglicherweise die Limit-Einstellung für die Veröffentlichung auf dem Image-Server erhöhen.
   * Videountertitel erfordern einen Regelsatz für die Firma, wenn das Hosting der HTML-Seite von einem externen Server (nicht von einem Scene7-Server) bereitgestellt wird. Wenden Sie sich an den Support der Adobe.
   * Die Analytics-Verfolgung kann aufgrund der Pufferung einen falschen Wiedergabeprozentsatz melden
   * Auf iPad- oder Android-Geräten wird möglicherweise ein schwarzer Rahmen anstelle eines Standbilds angezeigt.
   * Beim Laden des Viewers auf iPad- oder Android-Geräten blinkt möglicherweise ein schwarzer Rahmen auf dem Bildschirm.
   * Auf iPad-Geräten werden schwarze Ränder neben der VideoPlayer-Komponente angezeigt, wenn der Hintergrund auf Weiß/Transparent eingestellt ist.
   * Das letzte Videobild kann auf iPad mit iOS 7 verzerrt sein.
   * Während der Videosuche im HLS-Streaming-Modus in Chrome, Firefox und Internet Explorer kann es gelegentlich zu Makroblockierungen kommen.
   * Das Standbild wird möglicherweise zum ersten Besucher nicht im Microsoft Edge-Browser angezeigt.
   * Das Standbild kann nach dem Laden des Videos in Internet Explorer 9 ausgeblendet werden, wenn die progressive Wiedergabe verwendet wird.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

Das Benutzerhandbuch befindet sich im Ordner &quot;Adobe HTML5 Viewer SDK&quot;der Clientinstallation. Die Dokumentation zur Komponenten-API befindet sich im Unterordner docs der Clientinstallation.

**Fehlerbehebungen für 3.0.2**

* VideoPlayer - Videowiedergabe in Internet Explorer 11 unter Windows 7 fehlgeschlagen
* TableOfContents - `initialframe` hatte keine Auswirkungen auf den Hochformat-Modus auf Mobilgeräten für den HTML5-E-Katalog-Viewer.

**Neue Funktionen, Verbesserungen und Fehlerkorrekturen für 3.0.1**

* Allgemein

   * HLS-Streaming-Video-Wiedergabe als Standard-Video-Versand für die meisten Desktop-Systeme hinzugefügt. Flash-basiertes HDS-Video-Streaming ist weiterhin als alternative Wiedergabemöglichkeit verfügbar.
   * SearchManager-, SearchPanel-, SearchEffect- und SearchButton-Komponenten wurden hinzugefügt, um die neue Suchfunktion in E-Katalog-Viewern zu unterstützen.
   * Unterstützung für Geräte mit Maus- und Berührungseingabe im Chrome-Browser hinzugefügt.
   * Erkennung von Android-Versionen neu gestaltet, um zukünftige Versionen des Betriebssystems zu unterstützen
   * hinzufügen Unterstützung für die Ausrichtung von rechts nach links in eCatalog-spezifischen SDK-Komponenten.

* ControlBar

   * Es wurde ein optionaler Bildlauf für ControlBar-Inhalte hinzugefügt, falls dieser nicht in die verfügbare Breite passt.

* FlyoutzoomView

   * Der Fall, in dem `tip=0,-1,0` einen Fehler außerhalb des zulässigen Bereichs verursachte, wurde behoben.

**Anmerkungen zur Kompatibilität**

* Android 4.x

   * Um die Standardeinstellung zu deaktivieren, müssen Sie die folgende CSS-Regel für die Komponente blau markieren:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * Die Videowiedergabe kann beim Ändern von Bitratenströmen in AVS-Sets beendet werden.

* Chrome

   * Sämtliche API-Aufrufe, die die Wiederherstellung der Komponenten erzwingen, können aufgrund der internen Zwischenspeicherung in Chrome ignoriert werden.

* Galaxy SIII

   * Der Viewer kann manchmal nicht in den Vollbildmodus geladen werden.
   * Pageview leidet derzeit unter einem Speicherleck auf dem Gerät.
   * Durch Tippen auf die Dublette werden Viewer und Seite vergrößert, wenn die Browser-seitige Skalierung aktiv ist.

* Galaxie Nexus

   * Artefakte, die über einigen Ansichten angezeigt werden.
   * Durch Tippen auf die Dublette werden Viewer und Seite vergrößert, wenn die Browser-seitige Skalierung aktiv ist.

* iPad 3

   * Das iPad 3 verfügt über eine native Auflösung von 2048 x 1536. Dies kann zu Anzeigeproblemen führen, wenn die Firma &quot;IS publish&quot;hat und die Bildgrößenbeschränkung niedriger als diese eingestellt ist.

* iPhone4

   * Symbol für Wiederholung der Symbolwiedergabe, das nach dem Bildlauf auf der Seite durch das Wiedergabesymbol ersetzt wird.

* Internet Explorer

   * In IE 10 und älteren Vollbildmodus nicht den gesamten Bildschirm belegt, sondern nur die Größe der Anwendung auf die Größe des Browserfensters.
   * Der Rendermodus &quot;Quirks&quot;wird nicht unterstützt.
   * Internet Explorer auf Mobilgeräten wird derzeit nicht unterstützt.
   * Util.js kann beim Laden fehlschlagen, wenn es asynchron eingeschlossen wird.
   * Das Symbol &quot;IconEffect&quot;blockiert Klickkomponenten in SpinView- und ZoomView-Ereignissen.

* Videoplayer für native Geräte

   * Die Überlagerung von Komponenten der Benutzeroberfläche über VideoPlayer wird nicht unterstützt, wenn VideoPlayer zum Aufrufen des nativen Players des Geräts verwendet wird.
   * Die Videowiedergabe im nativen Modus ist in Safari 6 inkonsistent.
   * Bei der nativen Wiedergabe wird das Wiederholungssymbol nach dem Bildlauf durch das Wiedergabesymbol ersetzt.

* Touch-Geräte

   * Der Vollbildmodus belegt nicht den gesamten Gerätebildschirm, sondern ändert lediglich die Größe des Browser-Fensters.
   * Benutzerdefinierte Cursor funktionieren nicht auf Touch-Geräten.
   * Die Seitenanpassung auf Touch-Geräten wird derzeit nicht unterstützt. Zum Einbetten von HTML5-Viewern ist ein Viewport-Meta-Tag mit entsprechenden Einstellungen erforderlich.

* Xoom

   * Durch Tippen auf die Dublette werden Viewer und Seite vergrößert, wenn die Browser-seitige Skalierung aktiv ist.

**Bekannte Probleme und Einschränkungen**

* Alle Komponenten

   * In den Versionen 2.7.2 und früher wurden einige Komponenten mithilfe der API `insertBefore()` zum DOM hinzugefügt. Daher würden sich solche Komponenten in der Stapelreihenfolge am unteren Rand befinden, unabhängig davon, wann eine Komponenteninstanz relativ zu anderen Komponenten erstellt wird. Ab Version 2.8.1 verwenden alle Komponenten jetzt die API `appendChild()`, was bedeutet, dass die Reihenfolge der Komponentenstapelung der Reihenfolge der Instanzerstellung entspricht.

   * Die Verwendung des Modifikators `iscommand` zum Festlegen des Alpha-Kanal-Formats des Bilds wird nicht unterstützt. Verwenden Sie stattdessen den Parameter component `FMT`.
   * Die Eigenschaft CSS transform wird derzeit nicht unterstützt.

* Touch-Geräte

   * Durch die Geste &quot;Pinch&quot;auf Touch-Geräten wird kein Zoom-Ereignis generiert

* Behälter

   * Rahmen, Umrandung und Ränder auf dem Container werden nicht unterstützt. Adobe schlägt vor, dem übergeordneten DIV Stilelemente hinzuzufügen.
   * Sie müssen explizit die Größe des Containers festlegen, damit die Komponentengröße korrekt angepasst werden kann.

* Druckkomponente

   * Aufgrund von Einschränkungen des Browsers kann es vorkommen, dass die Druckkomponente den Inhalt in Internet Explorer 9 nicht ordnungsgemäß auf dem Papier skaliert.

* IconEffect-Komponente

   * IconEffect erzeugt einen Skriptfehler in Internet Explorer, wenn `autohide` deaktiviert ist (auf `0` eingestellt).

* ImageMapEffect-Komponente

   * Verzögerung bei der Neupositionierung des Symbols beim Schwenken des Bilds auf der Ansicht.

* MediaSet-Komponente

   * Inline-Assets erfordern dieselbe Kodierung wie die URL.

* NavigationView-Komponente

   * Derzeit unterstützt die Komponente nicht die Größenanpassung.

* PageScrubber-Komponente

   * Wenn auf dem iPhone 5 die Seitenumbruchzeichenblase auf Text eingestellt ist, werden Artefakte angezeigt, wenn die Schaltfläche entlang der Leiste verschoben wird. Die Verwendung von `-webkit-background-clip: content;` im Stil kann das Problem umgehen.

* SpinView-Komponente

   * SpinView scheint manchmal nach dem Wischen einzufrieren und das Gerät zu drehen, während sich das Bild dreht.

* Farbfeldkomponente

   * Bei der Auswahl eines Felds ohne Rand werden 2 Highlights angezeigt.
   * Auto-Scrolling mit `selectSwatch()`-Methode funktioniert nicht korrekt.

* VideoPlayer

   * Videoframe wird nicht aktualisiert, wenn die Suche auf 100 Prozent eingestellt ist und der Fallback auf auto eingestellt ist.
   * Während der Videosuche im HLS-Streaming-Modus in Chrome, Firefox und Internet Explorer kann es zu gelegentlichen Makro-Blockierungen kommen.
   * Das Standbild wird möglicherweise zum ersten Besucher nicht im Microsoft Edge-Browser angezeigt.
   * Das Standbild kann nach dem Laden des Videos in Internet Explorer 9 ausgeblendet werden, wenn die progressive Wiedergabe verwendet wird.

## Scene7 Image Serving 6.3.2 und Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC-Dienstprogramm - `downsample2x2`-Flag wird nicht mehr unterstützt. Dieses Flag war ein schlechter 2x2 Downsampling, der nicht mehr von IPS verwendet wird.
* CORS-Header - Derzeit ist der CORS-Header für `/is/content/`-Anforderungen konfiguriert.

