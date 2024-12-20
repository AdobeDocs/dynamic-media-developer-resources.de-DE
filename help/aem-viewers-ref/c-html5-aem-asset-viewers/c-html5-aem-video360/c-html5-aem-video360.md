---
title: Video360
description: Der HTML5 Video360 Viewer ist ein 360-Grad-Videoplayer, der Streaming- und progressive 360-Grad-Videos im H.264-Format wiedergibt, die von Dynamic Media Classic oder Adobe Experience Manager, Dynamic Media, bereitgestellt werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2562'
ht-degree: 0%

---

# Video360{#video}

Der HTML5 Video360 Viewer ist ein 360-Grad-Videoplayer, der Streaming- und progressive 360-Grad-Videos im H.264-Format wiedergibt, die von Dynamic Media Classic oder Adobe Experience Manager, Dynamic Media, bereitgestellt werden.

360-Grad-Videos, auch als immersive Videos oder sphärische Videos bezeichnet, sind Videoaufnahmen, bei denen eine Ansicht in jede Richtung gleichzeitig aufgezeichnet wird, und zwar mit einer omnidirektionalen Kamera oder einer Sammlung von Kameras. Es werden sowohl einzelne als auch adaptive Videosets unterstützt. Der Viewer unterstützt auch das Arbeiten mit progressiven Video- und HLS-Streams, die an einem externen Speicherort gehostet werden.

Das empfohlene Seitenverhältnis für 360-Grad-Videos lautet 2:1. Räumlicher Klang wird nicht unterstützt. Der Viewer ist nur für die Verwendung mit 360-Grad-Videos konzipiert. Der Versuch, ein Nicht-360-Grad-Video abzuspielen, führt zu einer verzerrten Videowiedergabe.

Der Viewer wurde für Desktop- und mobile Webbrowser entwickelt, die HTML5-Videos unterstützen. Der Viewer unterstützt optionale Social-Sharing-Tools.

Der Video360-Viewer verwendet die HTML5-Streaming-Videowiedergabe im HLS-Format in der Standardkonfiguration, wenn das zugrunde liegende System dies unterstützt. Auf Systemen, die HTML5-Streaming nicht unterstützen, wird der Viewer auf die progressive HTML5-Videobereitstellung zurückgesetzt.

Viewer-Typ ist 517.

## Demo-URLs {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Systemanforderungen {#section-b7270cc4290043399681dc504f043609}

Siehe [Systemanforderungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Verwenden des Video360-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der HTML5-Video360-Viewer stellt eine JavaScript-Hauptdatei und einen Satz Hilfsdateien (ein einziges JavaScript-Include mit allen von diesem Viewer verwendeten HTML5-Viewer-SDK-Komponenten, Assets, CSS) dar, die der Viewer zur Laufzeit heruntergeladen hat.

Der HTML5 Video360 Viewer kann sowohl im Popup-Modus mit der produktionsbereiten HTML-Seite von IS-Viewers als auch im eingebetteten Modus verwendet werden, wo er mithilfe der dokumentierten API in die Ziel-Web-Seite integriert wird.

Konfiguration und Skinning ähneln denen der anderen Viewer, die in diesem Handbuch beschrieben werden. Die gesamte Gestaltung erfolgt über benutzerdefinierte Cascading Style Sheets (CSS).

Siehe [Für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Für alle Viewer gemeinsame Befehlsreferenz - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Für 360-Grad-Videoinhalte sind höhere Kodierungseinstellungen erforderlich als für Standard-360-Grad-Videos. Mit anderen Worten: 360-Grad-Inhalte müssen in einer höheren Auflösung vorliegen als nicht-360-Grad-Videos, um die gleiche wahrnehmbare Qualität zu erzielen. Es wird empfohlen, die folgenden Einstellungen für adaptive Videovorgaben für 360-Grad-Videos zu berücksichtigen:

* 720p, 2500 kBit/s
* 1080p, 5000 kBit/s
* 1440p, 6600 kBit/s

Beachten Sie jedoch, dass für die Bereitstellung von mit solchen hochwertigen Einstellungen kodierten Videos eine Verbindung mit hoher Bandbreite auf dem Gerät des Endbenutzers erforderlich ist.

## Interagieren mit dem Video360-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der HTML5 Video360 Viewer bietet eine Reihe von Standardbenutzeroberflächensteuerelementen für die Videowiedergabe, z. B. die Wiedergabe-/Pausentaste, die Video-Scrubber-Videozeitblase, die Anzeige der wiedergegebenen Zeit/Gesamtzeit, die Lautstärkeregelung und die Vollbildtaste. Alle diese Steuerelemente werden in einer Steuerleiste am unteren Rand der Viewer-Benutzeroberfläche gruppiert.

Auf Touch-Geräten wird die Lautstärkeregelung in der Benutzeroberfläche ausgeblendet, da die Lautstärkeregelung nur über die Hardwaretasten des Geräts gesteuert werden kann.

Wenn der Viewer im Popup-Modus ausgeführt wird, ist in der Benutzeroberfläche keine Vollbildschaltfläche verfügbar.

Der Viewer unterstützt auch verschiedene Tools zur Freigabe in Social Media. Sie sind in der Benutzeroberfläche als einzelne Schaltfläche verfügbar, die in eine Freigabesymbolleiste erweitert wird, wenn Benutzende darauf klicken oder tippen. Die Freigabesymbolleiste enthält ein Symbol für jeden unterstützten Freigabekanaltyp wie Facebook, Twitter, E-Mail-Freigabe, Einbettungs-Code-Freigabe und Link-Freigabe. Wenn die Tools E-Mail-Freigabe, Einbettungsfreigabe oder Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Dateneingabeformular an. Wenn Facebook oder Twitter aufgerufen werden, leitet der Viewer den Benutzer von einem Social-Media-Service zu einem Standarddialogfeld für die Freigabe um. Außerdem wird die Videowiedergabe automatisch angehalten, wenn ein Freigabetool aktiviert ist. Freigabetools sind aufgrund von Sicherheitsbeschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

Der Viewer unterstützt 360-Grad-Videowiedergabe für Folgendes:

* VR-Headsets (wie Oculus Go und Oculus Rift)
* VR HMD (Head-Mounted Display)-Halterungen (wie Google-Karton)
* Nicht VR-fähige Geräte (z. B. Desktop-Browser, Tablets und Mobiltelefone, die nicht mit VR-HMD-Halterungen verbunden sind)

Es ist keine zusätzliche Konfiguration erforderlich, um 360-Grad-Videoinhalte auf dem VR-Headset anzuzeigen. Der Viewer erkennt automatisch das Vorhandensein des VR-Headsets und zeigt die Schaltfläche „VR“ über dem Videoinhalt an. Durch Aktivieren dieser Schaltfläche „VR“ wird das Video-Rendering in den VR-Modus umgeschaltet. Der Viewer unterstützt VR-Rendering nur in Browsern mit WebVR-Unterstützung.

Um VR-HMD-Halterungen verwenden zu können, muss der `Video360Player.vrrender`-Modifikator in der Viewer-Konfiguration auf `1` gesetzt werden, was das stereoskopische Rendering erzwingt.

Bei VR-Headsets und VR-HMD-Halterungen erfolgt der Blickwinkelwechsel als Reaktion auf die Bewegung des Headsets, keine andere Wiedergabesteuerung ist im VR-Modus vorgesehen.

Beim Ansehen von 360-Grad-Videos auf nicht VR-fähigen Geräten kann der Endbenutzer die Maus, Touch-Funktion oder Tastatur verwenden, um die Videowiedergabe und den Blickwinkel zu steuern.

Der Viewer unterstützt sowohl Touch-Eingaben als auch Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.

Der Viewer ist vollständig mit der Tastatur zugänglich. Siehe [Tastaturzugriff und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des Video360-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Web-Seiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal enthält eine Web-Seite einen Link, der bei Auswahl den Viewer in einem separaten Browser-Fenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt auf der Hosting-Seite einzubetten. Im letzteren Fall kann die Web-Seite über ein statisches Seiten-Layout verfügen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diesen Anforderungen gerecht zu werden, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung mit fester Größe und Einbetten von responsivem Design.

Das Einbetten mehrerer Videos auf derselben Seite wird auf Tablets und Mobilgeräten unterstützt. Normalerweise kann immer nur ein Video wiedergegeben werden. Wenn ein(e) Benutzende(r) beginnt, ein Video abzuspielen und dann versucht, ein anderes Video abzuspielen, wird das erste Video automatisch angehalten. Das automatisch angehaltene Video speichert die aktuelle Wiedergabezeit, sodass der/die Benutzende immer darauf zurückgreifen und die Wiedergabe fortsetzen kann. Die einzige Ausnahme von dieser Regel ist der Chrome-Browser auf Android™ 4.x-Geräten, auf dem Videos parallel wiedergegeben werden können.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Fenster oder einer separaten Registerkarte des Webbrowsers geöffnet. Sie nimmt den gesamten Browser-Fensterbereich und passt sich an, falls die Größe des Browsers geändert oder die Ausrichtung des Geräts geändert wird.

Dieser Modus ist bei Mobilgeräten am häufigsten. Die Web-Seite lädt den Viewer mithilfe `window.open()` JavaScript-Aufrufs, eines ordnungsgemäß konfigurierten HTML-Elements `A` einer anderen geeigneten Methode.

Es wird empfohlen, eine vorkonfigurierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Sie wird als [!DNL Video360Viewer.html] bezeichnet und befindet sich im [!DNL html5/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Sie können die visuelle Anpassung erreichen, indem Sie benutzerdefiniertes CSS anwenden.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Über den Einbettungsmodus für feste Größe und den Einbettungsmodus für responsives Design**

Im eingebetteten Modus wird der Viewer zur vorhandenen Web-Seite hinzugefügt, die möglicherweise bereits einige Kundeninhalte enthält, die nicht mit dem Viewer verknüpft sind. Der Viewer belegt normalerweise nur einen Teil des Grundbesitzes einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die für Desktops oder Tablet-Geräte ausgerichtet sind, sowie responsive Design-Seiten, deren Layout automatisch an den Gerätetyp angepasst wird.

Einbetten in fester Größe wird verwendet, wenn der Viewer seine Größe nach dem ersten Laden nicht ändert. Diese Methode ist die beste Wahl für Web-Seiten mit statischem Layout.

Beim Einbetten eines responsiven Designs wird davon ausgegangen, dass die Größe des Viewers zur Laufzeit entsprechend der Größenänderung seiner Container-`DIV` geändert werden muss. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Web-Seite, die ein flexibles Seiten-Layout verwendet.

Im responsiven Design-Einbettungsmodus verhält sich der Viewer unterschiedlich, je nachdem, wie die Größe der Web-Seite seinen Container-`DIV` bestimmt. Wenn die Web-Seite nur die Breite des Container-`DIV` festlegt und seine Höhe nicht eingeschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass an den Seiten ein Abstand vorhanden ist. Dieser Anwendungsfall ist der häufigste bei Web-Seiten, die responsive Web-Design-Layout-Frameworks wie Bootstrap und Foundation verwenden.

Wenn die Web-Seite jedoch sowohl die Breite als auch die Höhe für die Container-`DIV` des Viewers festlegt, füllt der Viewer nur diesen Bereich aus und folgt der Größe, die das Web-Seiten-Layout bereitstellt. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung an die Fenstergröße des Webbrowsers angepasst ist.

**Einbetten in fester Größe**

Sie können den Viewer wie folgt zu einer Web-Seite hinzufügen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Container-`DIV` definieren.
1. Festlegen der Viewer-Größe.
1. Viewer erstellen und initialisieren.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.

   Zum Erstellen eines Viewers müssen Sie dem HTML-Head ein Script-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL Video360Viewer.js] einbeziehen. Die [!DNL Video360Viewer.js]-Datei befindet sich im [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewers-Bereitstellung:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und er von derselben Domain bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Verweisen Sie auf Ihrer Seite nur auf die JavaScript-`include`-Datei des Haupt-Viewers. Verweisen Sie nicht auf zusätzliche JavaScript-Dateien im Web-Seiten-Code, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die vom Viewer aus `/s7viewers` Kontextpfad geladene HTML5 SDK `Utils.js`-Bibliothek (so genannte konsolidierte SDK-`include`). Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Runtime-Viewer-Bibliotheken vollständig von der Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Adobe speichert ältere Versionen der sekundären Viewer-`includes` nicht auf dem Server.
>
>
>Wenn Sie also auf der Seite einen direkten Verweis auf eine sekundäre JavaScript-`include` einfügen, die vom Viewer verwendet wird, wird die Viewer-Funktionalität in Zukunft unterbrochen, wenn eine neue Produktversion bereitgestellt wird.

1. Container-`DIV` definieren.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres `DIV` hinzu. Für das `DIV`-Element muss eine ID definiert sein, da diese ID später an die Viewer-API übergeben wird. Die Größe des DIV wird durch CSS angegeben.

   Der `DIV` ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute` festgelegt.

   Damit die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert, stellen Sie sicher, dass es keine anderen Elemente im DOM gibt, die eine höhere Stapelreihenfolge aufweisen als Ihre `DIV`.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-`DIV`:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Festlegen der Viewer-Größe

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für `.s7video360viewer` CSS-Klasse der obersten Ebene in absoluten Einheiten deklarieren oder `stagesize` Modifikator verwenden.

   Sie können die Größenanpassung in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten CSS-Viewer-Datei festlegen, die später einem Viewer-Vorgabeneintrag in Adobe Experience Manager Assets zugewiesen wird - On-Demand oder explizit mit `style` Befehl übergeben wird.

   Weitere Informationen [ Formatieren des Viewers mit CSS finden ](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) unter „Anpassen des Video360-Viewers“.

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf der HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Sie können den `stagesize` im Datensatz „Viewer-Vorgabe“ in AEM Assets - On-Demand festlegen. Sie können sie auch explizit mit dem Viewer-Initialisierungs-Code mit `params` Sammlung oder als API-Aufruf wie im Abschnitt „Befehlsreferenz“ beschrieben übergeben, wie hier zu sehen:

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Ein CSS-basierter Ansatz wird empfohlen und wird in diesem Beispiel verwendet.

1. Viewer erstellen und initialisieren.

   Wenn Sie die obigen Schritte ausgeführt haben, erstellen Sie eine Instanz `s7viewers.Video360Viewer` Klasse, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen `init()` Methode in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über `containerId` Feld verfügen, das den Namen der Viewer-Container-ID enthält und `params` JSON-Objekt mit Konfigurationsparametern verschachtelt ist, die vom Viewer unterstützt werden.

   In diesem Fall muss für das `params`-Objekt mindestens die Bildbereitstellungs-URL als `serverUrl`-Eigenschaft übergeben werden und das anfängliche Asset muss `asset` Parameter sein. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzigen Codezeile erstellen und starten, wobei die Video-Server-URL als `videoserverurl`-Eigenschaft übergeben wird, das anfängliche Asset als `asset`-Parameter und interaktive Daten als `interactivedata`-Eigenschaft. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzigen Codezeile erstellen und starten.

   Es ist wichtig, dass der Viewer-Container zum DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser verzögern die Erstellung von DOM bis zum Ende der Web-Seite. Um maximale Kompatibilität zu erzielen, rufen Sie die `init()`-Methode unmittelbar vor dem schließenden `BODY`-Tag oder im body-`onload()` auf.

   Gleichzeitig sollte das Container-Element noch nicht unbedingt Teil des Web-Seiten-Layouts sein. Beispielsweise kann sie mithilfe `display:none` ihr zugewiesenen Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Moment, an dem die Web-Seite das Container-Element wieder zum Layout zurückbringt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()`-Methode. Das Beispiel setzt Folgendes voraus:

   * Die Viewer-Instanz ist `video360Viewer`.
   * Der Name des Platzhalters `DIV` ist `s7viewer`.
   * Die Bildbereitstellungs-URL ist `https://s7d9.scene7.com/is/image`.
   * Die Videoserver-URL ist `https://s7d9.scene7.com/is/content`.
   * Das Asset ist `Viewers/space_station_360-AVS`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, in die der Video360-Viewer mit einer festen Größe eingebettet ist:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsives Design mit unbegrenzter Höhe**

Beim Einbetten eines responsiven Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße der Container-`DIV` des Viewers bestimmt. Nehmen wir für das folgende Beispiel an, dass die Web-Seite dem Container-`DIV` des Viewers ermöglicht, 40 % der Fenstergröße des Webbrowsers zu verwenden, wobei seine Höhe nicht beschränkt wird. Der Web-Seiten-HTML-Code würde wie folgt aussehen:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten für Einbetten in fester Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Definieren des Container-DIV.
1. Viewer erstellen und initialisieren.

Alle oben genannten Schritte sind dieselben wie bei der Einbettung in fester Größe. Fügen Sie das Container-DIV zum vorhandenen `"holder"`-DIV hinzu. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn der Browser skaliert wird, und wie das Seitenverhältnis des Viewers mit dem Asset übereinstimmt.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Responsive Einbettung mit definierter Breite und Höhe**

Wenn eine responsive Einbettung mit definierter Breite und Höhe vorliegt, ist der Stil der Web-Seite anders. Es bietet beide Größen für den `"holder"` DIV und zentriert ihn im Browser-Fenster. Außerdem legt die Web-Seite die Größe des `HTML`- und `BODY` auf 100 Prozent fest.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Die übrigen Einbettungsschritte sind identisch mit den Schritten für responsives Einbetten mit unbegrenzter Höhe. Das daraus resultierende Beispiel lautet:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Einbetten mithilfe der Setter-basierten API**

Anstatt die JSON-basierte Initialisierung zu verwenden, ist es möglich, eine Setter-basierte API und einen Nicht-Args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors sind keine Parameter erforderlich und Konfigurationsparameter werden mithilfe von `setContainerId()`-, `setParam()`- und `setAsset()`-API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel veranschaulicht die Verwendung der Einbettung fester Größe mit der Setter-basierten API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
