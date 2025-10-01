---
title: Scene7-Version Herbst 2016
description: Die neuesten Versionshinweise für Adobe Scene7 Version vom Herbst 2016, Teil der Adobe Experience Manager-Lösung in Adobe Experience Cloud.
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '2234'
ht-degree: 0%

---

# Scene7-Version Herbst 2016{#scene-fall-release}

Die neuesten Versionshinweise für Adobe Scene7 vom Herbst 2016 sind Teil der Adobe Experience Manager-Lösung in Adobe Experience Cloud.

## Scene7-Version Herbst 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Die neuesten Versionshinweise für [!DNL Adobe Scene7] Herbst 2016 sind Teil der [!DNL Adobe Experience Manager] in der [!DNL Adobe Experience Cloud].

* [Allgemein](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Viewer (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Viewer (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Viewer (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 und Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Allgemein {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe freut sich, die Verfügbarkeit der Bereitstellung von Inhalten per HTTP/2 bekannt geben zu können, was insgesamt den Vorteil einer verbesserten Leistung bietet.

Siehe [Häufig gestellte Fragen zur Bereitstellung von Inhalten über HTTP/2](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Die vollständige Dokumentation finden Sie unter [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Neue Funktionen, Verbesserungen und Fehlerbehebungen**

* Die Videoausschnittfunktion wurde aus [!DNL Adobe Scene7 Publishing System] Benutzeroberfläche entfernt.
* Authentifizierung wurde nach Bedarf und Möglichkeit zu allen Scene7-Servlets hinzugefügt
* Fehlerbehebung bei der Listenansicht im Papierkorb.
* Die **&quot;Dynamic Media Classic (Scene7) Admin erstellen** wurde aus Sicherheitsgründen aus der Benutzerverwaltung entfernt.
* FTP WebAdmin unterstützt jetzt die OKTA-Authentifizierung.
* Die Funktion des Standardkennworts, das für neue Media Portal-Benutzer erstellt wurde, wurde entfernt.
* Fehlerbehebung bei einem temporären Kennwort, das beim Hinzufügen eines neuen Benutzers generiert wurde. Das Kennwort erfüllte nicht die erforderlichen Kennwortanforderungen.
* Gelöste Probleme mit vollständigem WebAdmin-Stammdatenträger.
* Fehlerbehebung, bei der ein Benutzer deaktiviert wurde, wird nicht sofort in der Benutzeroberfläche angezeigt.
* Fehlerkorrektur - Beim Löschen eines Benutzers kann der Benutzer später nicht neu erstellt werden.
* Fehlerbehebung bei der Begrüßungs-E-Mail, die an neue Scene7-Benutzer gesendet wurde, aber keine Authentifizierung zur Steuerung bestimmter Einstellungen enthielt.
* Fehlerbehebung, durch die eine FTP-Ordnerliste nicht abgerufen werden konnte, wenn ein Ordner Sonderzeichen im Namen enthielt.
* Konfigurieren Sie OKTA-Service-Provider für Scene7-Umgebungen.
* Es wurde Unterstützung für die Experience Cloud-Organisations-ID für Viewer Analytics hinzugefügt.
* Scene7 SAML-Verbraucher implementiert.

## Viewer (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Eine vollständige Dokumentation finden Sie [Viewer-Referenzhandbuch](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Fehlerbehebungen für Image Serving 5.5.3**

* Kompatibilität mit RequireJS- und DOJO-Bibliotheken.

  Konsolidiertes SDK JS-Caching während der Viewer-Bereitstellung.

## Viewer (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Eine vollständige Dokumentation finden Sie [Viewer-Referenzhandbuch](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Fehlerbehebungen für Image Serving 5.5.2**

* Das Video konnte in Internet Explorer 11 unter Windows 7 nicht wiedergegeben werden.
* `initialframe` hat den Hochformat-Modus auf Mobilgeräten für den HTML5 eCatalog nicht beeinflusst.

## Viewer (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Eine vollständige Dokumentation finden Sie [Viewer-Referenzhandbuch](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Neue Funktionen, Verbesserungen und Fehlerbehebungen für Image Serving 5.5.1**

* HTML5 E-Katalog-Viewer mit Suchfunktion.
* HLS-Streaming-Videowiedergabe wurde als Standardmethode für die Videobereitstellung für die meisten Desktop-Systeme hinzugefügt. Flash-basiertes HDS-Video-Streaming ist weiterhin als alternative Wiedergabeoption verfügbar.
* Es wurde Unterstützung für Geräte mit Maus- und Touch-Eingabe hinzugefügt, auf denen der Chrome-Browser ausgeführt wird.
* Unterstützung der Experience Cloud-Organisations-ID zur Analytics-Integration hinzugefügt.
* Aktualisieren Sie die AppMeasurement JavaScript-Bibliothek auf Version 1.6.1.
* Es wurde Unterstützung für die Ausrichtung von rechts nach links im E-Katalog-Viewer hinzugefügt.
* Es wurde ein Problem behoben, bei dem `tip=0,-1,0` einen Fehler außerhalb des zulässigen Bereichs verursachte.

**Kompatibilitätshinweise**

* BlackBerry®

   * Inkompatibilität mit älteren AVS-Sets. Clients müssen AVS-Sets erneut hochladen, um die Wiedergabe zu ermöglichen.

* Allgemein

   * Browser-seitige Skalierung kann dazu führen, dass Benutzeroberfläche und Bilder unscharf werden, wenn Benutzende die Seite vergrößern. Die Formatierung der Benutzeroberfläche wird je nach Zoom möglicherweise auch falsch angezeigt. Dieser Effekt wird in den Vollbildmodus übernommen.
   * Aufgrund der Größenbeschränkung auf Mobilgeräten verwendet der Viewer für gemischte Medien Foliengesten, um Frames in eingebetteten Bildsets auszutauschen, anstatt auf die Komponente für eingebettete Farbfelder zu tippen. Die Komponente ist als visueller Indikator vorhanden.
   * In Internet Explorer-Browsern und einigen Touch-Geräten belegt der Vollbildmodus nicht den gesamten Gerätebildschirm. Stattdessen wird die Größe der Anwendung an die Größe des Browser-Fensters angepasst.
   * Die Schaltfläche „Schließen“ funktioniert nicht in iOS 8.0 und 8.1, tritt aber in iOS 8.2 nicht mehr auf

* Galaxie SIII

   * Speicherverlust bei Zoom- und E-Katalog-HTML5-Viewern. Wiederholte Navigation durch Frames kann dazu führen, dass der Browser abstürzt.
   * Durch Doppeltippen auf den Viewer kann die gesamte Seite vergrößert werden, anstatt nur der Viewer mit aktivierter Browser-seitiger Skalierung.

* Galaxy S4

   * Gerät als Tablet im Hochformat erkannt, Vollbild in den Browser-Einstellungen überprüft.

* Galaxie Nexus

   * Durch Doppeltippen auf den Viewer kann die gesamte Seite vergrößert werden, anstatt nur der Viewer mit aktivierter Browser-seitiger Skalierung.

* Galaxy Nexus 10 und Galaxy Tablet

   * E-Katalog mit falscher Seitenaufteilung mit Hoch- und Querformat.

* HTC-Mobilgeräte

   * HTC-Mobilgeräte Die Ergebnisse von Adobe zeigen, dass die Unfähigkeit, den nativen Pinch-Zoom zu deaktivieren, eine „Funktion“ von HTC UI Wrapper (HTC Sense) ist. Dieses Problem kann dazu führen, dass die gesamte Seite vergrößert wird, wenn die Geste „Zum Zoomen drücken“ im Viewer verwendet wird. Schlagen Sie stattdessen vor, doppelt zu tippen.
   * Imagemap-Symbole können sich überschneiden, wenn die Imagemaps klein sind und nahe beieinander liegen.

* HTML5-Video

   * Internet Explorer 9: Benutzerdefinierte Posterbilder werden nicht angezeigt.
   * `IntialBitRate` Modifikator wird nur mit Software HLS und Flash HDS Wiedergabe unterstützt. Dies funktioniert nicht, wenn die Wiedergabe den nativen Player verwendet.
   * Die progressive Wiedergabe von OGG und WebM wird derzeit nicht unterstützt.
   * Die Browser-Skalierung kann dazu führen, dass der Video-Player in einer falschen Größe angezeigt wird (einschließlich Anzeigeeinstellungen in der Systemsteuerung des Windows-Betriebssystems).
   * Videosuchvorgänge mit HLS-Streaming in Safari können inkonsistent sein.

* Internet Explorer

   * Der Quirks-Modus wird derzeit nicht unterstützt.
   * Der Kompatibilitätsmodus wird derzeit nicht unterstützt.
   * Internet Explorer auf Mobilgeräten wird derzeit nicht unterstützt.

* iOS

   * Große E-Kataloge können einen Browser-Absturz in iPad 2 verursachen.
   * iPhone 6+-Smartphones werden von den Viewern als Tablets erkannt.

* Safari

   * Safari 6.1 oder höher: Die Einstellungen der Internet-Plug-ins können die Flash-Videowiedergabe verhindern.
   * Das „Suchen“ von Videos mit HLS-Streaming in Safari kann inkonsistent sein.
   * Die Suche nach dem Ende des Videos in Safari 6 mit HLS-Streaming ist nicht möglich.

**Bekannte Probleme und Einschränkungen**

* Die Image-Serving-Modifikatoren von `iscommands` werden nicht standardmäßig zur `req=set` hinzugefügt. Modifikatoren, die sich nur auf die Bildanzeige auswirken, funktionieren einwandfrei. Modifikatoren, die sich auf die Größe auswirken, müssen in einem komplexen Asset verwendet werden.
* [Flyout] IE9 bleibt manchmal auf dem Bildschirm, nachdem die Maus ausgeschaltet wurde.
* Die Browser-Skalierung führt zu einer falschen Größenanpassung.
* iPad 2: Safari in iOS stürzt durch großes E-Katalog-Asset ab.
* Alle Betrachter

   * Wasserzeichen, Verschleierung und Sperrung werden nicht unterstützt.
   * Bildvorgaben werden nicht unterstützt.
   * Das Hinzufügen oder Entfernen eines Viewers aus dem DOM mithilfe `display:none` CSS oder durch dynamisches Trennen vom übergeordneten Knoten wird derzeit nicht unterstützt.

* HTML5 - Alle Betrachter

   * Das Einbetten des Viewers in die Tabelle kann dazu führen, dass die Größe des Viewers falsch eingestellt oder der Viewer im nicht nativen Vollbildmodus platziert wird. Schlagen Sie vor, stattdessen DIVs zu verwenden.
   * Parameter mit expliziten Instanznamen im Code erfordern, dass Instanznamen in der URL ebenfalls überschrieben werden (z. B. `zoomView.iconfeffect=0`).
   * Der Image Serving-Befehl „Zuschneiden“ wird derzeit nicht unterstützt.
   * Die Schaltfläche Schließen funktioniert nur, wenn der Viewer im untergeordneten Fenster geöffnet ist.
   * Der `iscommands`-Modifikator unterstützt keine Bildbereitstellungs-Modifikatoren, die sich auf die Bildgröße auswirken.

* HTML5 eCatalog

   * Wenn Sie zu einer anderen HTML-Seite navigieren und gelegentlich zurückkehren, wird der Viewer auf die erste Seite zurückgesetzt.
   * Das Seitenlayout wird nach dem Drehen eines iOS-Geräts gelegentlich falsch angezeigt. Durch das Vergrößern der Seite wird das Layout korrigiert.
   * Interne Links nur zur am weitesten links liegenden Seite in mehrseitigen Druckbögen. Beeinflusst Mobilgeräte im Hochformat.
   * In mehrseitigen Druckbögen ist „InitialFrame“ nur mit der am weitesten links liegenden Seite verknüpft. Beeinflusst Mobilgeräte im Hochformat.
   * Aufgrund von Browserbeschränkungen ist die Druckfunktion in IE9 nicht verfügbar.

* HTML5 MixedMedia

   * Soundtrack-Wiedergabe wird nicht unterstützt.

* HTML5 Social

   * Damit Miniaturansichten in ausgehenden E-Mails ordnungsgemäß gerendert werden können, muss der Modifikator &quot;`serverurl`&quot; über eine absolute URL verfügen.

* HTML5-Video

   * Auf dem Posterbild kann der Fehler „max size“ auftreten. Das Unternehmen muss die Einstellung für das Limit für die Image-Serving-Veröffentlichung erhöhen.
   * Für Videobeschriftungen ist ein Regelsatz des Unternehmens erforderlich, wenn das Hosten der HTML-Seite von einem externen Server (kein Scene7-Server) erfolgt. Wenden Sie sich an den Adobe-Support.
   * Das Analytics-Tracking meldet möglicherweise einen falschen Wiedergabeprozentsatz aufgrund der Pufferung
   * Auf iPad- oder Android™-Geräten wird möglicherweise ein schwarzer Rahmen anstelle eines Posterbilds angezeigt.
   * Beim Laden des Viewers auf iPad- oder Android™-Geräten wird ein schwarzer Frame möglicherweise auf dem Bildschirm blinkt.
   * Schwarze Rahmen werden auf der Seite der VideoPlayer-Komponente angezeigt, wenn der Hintergrund auf iPad-Geräten auf Weiß/Transparent eingestellt ist.
   * Das letzte Einzelbild des Videos könnte auf iPad mit iOS 7 verzerrt sein.
   * Gelegentlich kann es während der Videosuche im HLS-Streaming-Modus in den Browsern Chrome, Firefox und Internet Explorer zu Makroblockierungen kommen.
      * Das Standbild wird im Microsoft® Edge-Browser möglicherweise nicht zum ersten Mal angezeigt.
      * Das Posterbild kann nach dem Laden des Videos in Internet Explorer 9 ausgeblendet werden, wenn die progressive Wiedergabe verwendet wird.

## Scene7 HTML5-Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

Das Benutzerhandbuch befindet sich im Adobe HTML5 Viewer SDK-Ordner der Client-Installation. Die Dokumentation zur Komponenten-API befindet sich im Unterordner „docs“ der Client-Installation.

**Fehlerbehebungen für 3.0.2**

* VideoPlayer - Video konnte in Internet Explorer 11 unter Windows 7 nicht wiedergegeben werden.
* TableOfContents - `initialframe` hat den Hochformat-Modus auf Mobilgeräten für den HTML5 eCatalog-Viewer nicht beeinflusst.

**Neue Funktionen, Verbesserungen und Fehlerbehebungen für 3.0.1**

* Allgemein

   * HLS-Streaming-Videowiedergabe wurde als Standardmethode für die Videobereitstellung für die meisten Desktop-Systeme hinzugefügt. Flash-basiertes HDS-Video-Streaming ist weiterhin als alternative Wiedergabeoption verfügbar.
   * Die Komponenten SearchManager, SearchPanel, SearchEffect und SearchButton wurden hinzugefügt, um die neue Suchfunktion in E-Katalog-Viewern zu unterstützen.
   * Es wurde Unterstützung für Geräte hinzugefügt, auf denen sowohl Maus- als auch Touch-Eingaben im Chrome-Browser ausgeführt werden.
   * Die Android™-Versionserkennung wurde überarbeitet, um zukünftige Versionen des Betriebssystems zu unterstützen.
   * Unterstützung für die Rechts-nach-links-Ausrichtung in eCatalog-spezifischen SDK-Komponenten hinzugefügt.

* ControlBar

   * Optionaler Bildlauf für ControlBar-Inhalt hinzugefügt, falls dieser nicht in die verfügbare Breite passt.

* FlyoutzoomView

   * Es wurde ein Fall behoben, in dem `tip=0,-1,0` einen Fehler außerhalb des zulässigen Bereichs verursachte.

**Kompatibilitätshinweise**

* Android™ 4.x

   * Um die Standardeinstellung zu deaktivieren, markieren Sie mit blauer Maustaste die folgende CSS-Regel, die für die Komponente hinzugefügt werden muss:

     `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * Die Videowiedergabe kann beendet werden, wenn die Bitraten-Streams in den AVS-Sets geändert werden.

* Chrome

   * Alle API-Aufrufe, die eine Komponentenneuerstellung erzwingen, können aufgrund der internen Zwischenspeicherung von Chrome ignoriert werden.

* Galaxie SIII

   * Der Viewer kann manchmal nicht im Vollbildmodus geladen werden.
   * Seitenansicht weist derzeit einen Speicherverlust auf dem Gerät auf.
   * Durch Doppeltippen auf Geste werden Viewer und Seite vergrößert, wenn die Browser-seitige Skalierung aktiv ist.

* Galaxie Nexus

   * Artefakte werden über einigen Ansichtskomponenten angezeigt.
   * Durch Doppeltippen auf Geste werden Viewer und Seite vergrößert, wenn die Browser-seitige Skalierung aktiv ist.

* IPAD 3

   * Der iPad 3 hat eine native Auflösung von 2048 x 1536. Diese Auflösung kann zu Anzeigeproblemen führen, wenn für die IMS-Veröffentlichung des Unternehmens eine niedrigere Bildgrößenbeschränkung festgelegt ist.

* IPHONE4

   * IconEffect-Wiedergabesymbol wurde durch Wiedergabesymbol nach dem Scrollen der Seite ersetzt.

* Internet Explorer

   * Im IE 10-Modus und älteren Vollbildmodus wird nicht der gesamte Bildschirm belegt, sondern nur die Größe der Anwendung an die Größe des Browser-Fensters angepasst.
   * Der Quirks-Rendermodus wird nicht unterstützt.
   * Internet Explorer auf Mobilgeräten wird derzeit nicht unterstützt.
   * Util.js kann möglicherweise nicht geladen werden, wenn es asynchron eingeschlossen ist.
   * Das IconEffect-Symbol blockiert Klickereignisse für SpinView- und ZoomView-Komponenten.

* Native Video-Player für Geräte

   * Das Überlagern von UI-Komponenten über VideoPlayer wird nicht unterstützt, wenn VideoPlayer zum Aufrufen des nativen Players des Geräts verwendet wird.
   * Die Videowiedergabe im nativen Modus ist in Safari 6 inkonsistent.
   * Die native Wiedergabe ersetzt das Wiedergabesymbol durch das Wiedergabesymbol nach dem Scrollen der Seite.

* Touch-Geräte

   * Der Vollbildmodus nimmt nicht den gesamten Gerätebildschirm ein, sondern passt die Anwendung nur an die Größe des Browser-Fensters an.
   * Benutzerdefinierte Cursor funktionieren auf Touch-Geräten nicht.
   * Das Skalieren von Seiten auf Touch-Geräten wird derzeit nicht unterstützt. Zum Einbetten von HTML5-Viewern ist ein Viewport-Meta-Tag mit entsprechenden Einstellungen erforderlich.

* Zoom

   * Durch Doppeltippen auf Geste werden Viewer und Seite vergrößert, wenn die Browser-seitige Skalierung aktiv ist.

**Bekannte Probleme und Einschränkungen**

* Alle Komponenten

   * In den Versionen 2.7.2 und früher wurden einige Komponenten mithilfe `insertBefore()` API zum DOM hinzugefügt. Daher würden sich diese Komponenten selbst an das Ende der Stapelreihenfolge setzen, unabhängig davon, wann die Komponenteninstanz relativ zu anderen Komponenten erstellt wird. In Version 2.8.1 verwenden alle Komponenten jetzt `appendChild()` API, was bedeutet, dass die Stapelreihenfolge der Komponenten mit der Reihenfolge der Instanzerstellung übereinstimmen würde.

   * Die Verwendung `iscommand` Modifikators zum Festlegen des Alphakanalformats für Bilder wird nicht unterstützt. Verwenden Sie stattdessen `FMT` Komponentenparameter .
   * Die CSS-Transformationseigenschaft wird derzeit nicht unterstützt.

* Touch-Geräte

   * Pinch-Geste auf Touch-Geräten generiert kein Zoom-Ereignis

* Behälter

   * Rahmen, Auffüllung und Ränder auf dem Container werden nicht unterstützt. Adobe empfiehlt, dem übergeordneten DIV Stilelemente hinzuzufügen.
   * Muss die Container-Größe explizit festlegen, da ansonsten die Größe der Komponenten korrekt sein kann.

* Komponente drucken

   * Aufgrund von Browser-Einschränkungen kann es sein, dass die Druckkomponente in Internet Explorer 9 den Inhalt auf dem Papier nicht richtig skaliert.

* IconEffect-Komponente

   * IconEffect generiert einen Skriptfehler in Internet Explorer, wenn `autohide` deaktiviert ist (auf `0` gesetzt).

* ImageMapEffect-Komponente

   * Verzögerung mit dem Neupositionierungssymbol beim Schwenken des Bildes auf der Ansichtskomponente.

* MediaSet-Komponente

   * Inline-Assets fordern dieselbe Kodierung an wie in der URL.

* NavigationView-Komponente

   * Die Größe der Komponente wird derzeit nicht unterstützt.

* PageScrubber-Komponente

   * Wenn in iPhone 5 die PageScrubber-Bubble auf Text festgelegt ist, werden beim Verschieben der Schaltfläche entlang der Spur Artefakte angezeigt. Die Verwendung von `-webkit-background-clip: content;` im -Stil umgeht das Problem.

* SpinView-Komponente

   * SpinView scheint manchmal nach Wischen und Drehen des Geräts einzufrieren, während sich das Bild dreht.

* Farbfelder-Komponente

   * Bei der Auswahl eines Farbfelds, das außerhalb der Grenzen liegt, werden zwei Hervorhebungen angezeigt.
   * Automatischer Bildlauf mit `selectSwatch()` Methode funktioniert nicht korrekt.

* Video-Player

   * Videoframe wird nicht aktualisiert, wenn Seek auf 100 % eingestellt ist und der Fallback auf „Auto“ eingestellt ist.
   * Gelegentlich kann es während der Videosuche im HLS-Streaming-Modus in den Browsern Chrome, Firefox und Internet Explorer zu einer Makrosperre kommen.
   * Das Standbild wird im Microsoft® Edge-Browser möglicherweise nicht zum ersten Mal angezeigt.
   * Das Posterbild kann nach dem Laden des Videos in Internet Explorer 9 ausgeblendet werden, wenn die progressive Wiedergabe verwendet wird.

## Dynamic Media Image Serving 6.3.2 und Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC-Dienstprogramm - `downsample2x2`-Flag wird nicht mehr unterstützt. Dieses Flag war ein 2x2 Downsampler von schlechter Qualität, der nicht mehr von IPS verwendet wird.
* CORS-Header - Derzeit ist der CORS-Header für `/is/content/`-Anfragen konfiguriert.
