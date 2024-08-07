---
title: Video360
description: Der HTML5 Video360 Viewer ist ein 360-Grad-Videoplayer, der Streaming- und progressive 360-Grad-Videos wiedergibt, die im H.264-Format kodiert sind und von Dynamic Media Classic oder Adobe Experience Manager, Dynamic Media bereitgestellt werden.
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

Der HTML5 Video360 Viewer ist ein 360-Grad-Videoplayer, der Streaming- und progressive 360-Grad-Videos wiedergibt, die im H.264-Format kodiert sind und von Dynamic Media Classic oder Adobe Experience Manager, Dynamic Media bereitgestellt werden.

360-Grad-Videos, auch als interaktive Videos oder kugelförmige Videos bezeichnet, sind Videoaufnahmen, bei denen gleichzeitig eine Ansicht in jede Richtung aufgezeichnet wird, die mit einer omnidirektionalen Kamera oder einer Kamerasammlung aufgenommen wurde. Es werden sowohl einzelne Video- als auch adaptive Videosets unterstützt. Der Viewer unterstützt auch die Arbeit mit progressiven Videos und HLS-Streams, die auf einem externen Speicherort gehostet werden.

Das empfohlene Seitenverhältnis für 360-Grad-Videos ist 2:1. Geodätischer Klang wird nicht unterstützt. Der Viewer wurde nur für 360-Grad-Videos entwickelt. Ein Versuch, ein Video abzuspielen, das nicht 360 ist, führt zu einer verzerrten Videowiedergabe.

Der Viewer ist für Desktop- und mobile Webbrowser konzipiert, die HTML5-Videos unterstützen. Der Viewer unterstützt optionale Tools zur Freigabe in sozialen Netzwerken.

Der Video360-Viewer verwendet die HTML5-Streaming-Videowiedergabe im HLS-Format in seiner Standardkonfiguration, wenn das zugrunde liegende System dies unterstützt. Auf Systemen, die HTML5-Streaming nicht unterstützen, greift der Viewer auf die progressive HTML5-Videowiedergabe zurück.

Der Viewer-Typ ist 517.

## Demo-URLs {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Systemanforderungen {#section-b7270cc4290043399681dc504f043609}

Siehe [Systemanforderungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Verwenden des Video360 Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar (eine JavaScript-Datei enthält alle von diesem Viewer verwendeten HTML5 Viewer-SDK-Komponenten, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen wurden.

HTML5 Video360 Viewer kann sowohl im Popup-Modus mithilfe einer produktionsbereiten HTML-Seite, die mit IS-Viewern bereitgestellt wird, als auch im eingebetteten Modus verwendet werden, wo er mithilfe einer dokumentierten API in die Ziel-Web-Seite integriert wird.

Die Konfiguration und das Skinning ähneln denen der anderen in diesem Handbuch beschriebenen Viewer. Die gesamte Skinnerung erfolgt über benutzerdefinierte CSS-Stylesheets (Cascading Style Sheets).

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Für 360-Grad-Videoinhalte sind höhere Kodierungseinstellungen erforderlich als für standardmäßige Videos, die nicht 360 sind. Anders ausgedrückt: 360 Inhalte müssen in einer höheren Auflösung als 360 Videos vorliegen, um die gleiche wahrnehmbare Qualität zu erzielen. Es wird empfohlen, die folgenden Einstellungen für adaptive Videovorgaben für 360-Grad-Videos zu berücksichtigen:

* 720 p, 2500 kBit/s
* 1080p, 5000 kBit/s
* 1440p, 6600 kBit/s

Beachten Sie jedoch, dass die Bereitstellung von Videos, die mit solchen Einstellungen hoher Qualität kodiert wurden, eine Verbindung mit hoher Bandbreite auf dem Gerät eines Endbenutzers erfordert.

## Interagieren mit Video360 Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 Viewer bietet eine Reihe von Standardsteuerelementen für die Videowiedergabe, wie z. B. Wiedergabe/Pause-Schaltfläche, Video-Scrubber-Videozeitblase, Wiedergabe/Gesamtzeit-Anzeige, Lautstärkeregler und Vollbildschaltflächen. Alle diese Steuerelemente sind in der unteren Leiste der Viewer-Benutzeroberfläche in eine Steuerleiste gruppiert.

Auf Touch-Geräten ist die Lautstärkeregelung in der Benutzeroberfläche ausgeblendet, da es nur möglich ist, die Lautstärke mithilfe der Hardwaretasten des Geräts zu steuern.

Wenn der Viewer im Popup-Modus ausgeführt wird, ist in der Benutzeroberfläche keine Vollbildschaltfläche verfügbar.

Der Viewer unterstützt auch verschiedene Tools zur Freigabe in Social Media. Sie sind als einzelne Schaltfläche in der Benutzeroberfläche verfügbar, die sich zu einer Freigabesymbolleiste erweitert, wenn der Benutzer darauf klickt oder tippt. Die Freigabesymbolleiste enthält ein Symbol für jeden unterstützten Freigabekanaltyp wie Facebook, Twitter, E-Mail-Freigabe, Einbettungscode-Freigabe und Linkfreigabe. Wenn die Tools für die Freigabe von E-Mails, die Einbettung von Freigabe oder die Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Dateneingabeformular an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer von einem Social-Media-Dienst zu einem standardmäßigen Dialogfeld für die Freigabe um. Außerdem wird die Videowiedergabe automatisch angehalten, wenn ein Freigabe-Tool aktiviert wird. Die Freigabe-Tools sind aufgrund der Sicherheitseinschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

Der Viewer unterstützt die 360-Grad-Videowiedergabe in folgenden Fällen:

* VR-Headsets (wie Oculus Go und Oculus Rift)
* VR-HMD-Reittiere (mit vorinstalliertem Display) (wie Google-Pinnwand)
* Nicht für VR aktivierte Geräte (wie Desktop-Browser, Tablets und Mobiltelefone, die nicht mit VR-HMD-Bereitstellungen verbunden sind)

Zur Anzeige von 360-Grad-Videoinhalten auf VR-Headset ist keine zusätzliche Konfiguration erforderlich. Der Viewer erkennt automatisch das Vorhandensein eines VR-Headsets und zeigt die Schaltfläche &quot;VR&quot;über dem Videoinhalt an. Durch Aktivierung dieser &quot;VR&quot;-Schaltfläche wird das Video-Rendering in den VR-Modus geändert. Der Viewer unterstützt das VR-Rendering nur in Browsern mit WebVR-Unterstützung.

Um VR HTML-Reittierungen zu verwenden, muss der Modifikator `Video360Player.vrrender` in der Viewer-Konfiguration auf `1` gesetzt werden, was das stereoskopische Rendering erzwingt.

Bei VR-Headsets und VR-HMD-Bereitstellungen erfolgt eine Sichtänderung als Reaktion auf die Kopfzeilenbewegung. Im VR-Modus wird keine andere Wiedergabesteuerung bereitgestellt.

Beim Ansehen von 360-Grad-Videos auf nicht VR-fähigen Geräten kann der Endbenutzer die Maus, Berührung oder Tastatur verwenden, um die Videowiedergabe und den Anzeigepunkt zu steuern.

Der Viewer unterstützt sowohl die Touch-Eingabe als auch die Mauseingabe auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome-, Internet Explorer 11- und Edge-Webbrowser beschränkt.

Der Viewer ist vollständig über die Tastatur zugänglich. Siehe [Barrierefreiheit und Navigation auf der Tastatur](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des Video360-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, der, wenn ausgewählt, den Viewer in einem separaten Browserfenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt auf der Hosting-Seite einzubetten. In letzterem Fall kann die Webseite ein statisches Seitenlayout aufweisen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei Hauptbetriebsmodi: Popup, Einbettung fester Größe und Einbettung responsiver Designs.

Das Einbetten mehrerer Videos auf derselben Seite wird auf Tablets und Mobilgeräten unterstützt. Normalerweise kann nur ein Video gleichzeitig wiedergegeben werden. Wenn ein Benutzer mit der Wiedergabe eines Videos beginnt und dann versucht, ein weiteres Video abzuspielen, wird das erste Video automatisch angehalten. Das automatisch angehaltene Video speichert die aktuelle Wiedergabedauer, sodass der Benutzer jederzeit darauf zugreifen und die Wiedergabe fortsetzen kann. Die einzige Ausnahme bildet der Chrome-Browser auf Geräten mit Android™ 4.x, die Videos parallel wiedergeben können.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Bereich des Browser-Fensters und passt sich an, falls die Größe des Browsers geändert oder die Geräteausrichtung geändert wird.

Dieser Modus wird am häufigsten für Mobilgeräte verwendet. Die Webseite lädt den Viewer mit dem Aufruf `window.open()` JavaScript , dem ordnungsgemäß konfigurierten Element `A` HTML oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Es heißt [!DNL Video360Viewer.html] und befindet sich im Unterordner [!DNL html5/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erreichen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Über den Einbettungsmodus mit fester Größe und den Einbettungsmodus für responsives Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Seiten, auf denen das Layout automatisch an den Gerätetyp angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Methode eignet sich am besten für Webseiten mit statischem Layout.

Responsives Einbetten von Design setzt voraus, dass die Größe des Viewers zur Laufzeit geändert werden muss, um auf die Größenänderung des Containers `DIV` reagieren zu können. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für responsive Designs verhält sich der Viewer unterschiedlich, je nachdem, wie die Größe des Containers auf der Webseite angepasst wird `DIV`. Wenn die Webseite nur die Breite des Containers &quot;`DIV`&quot; festlegt und die Höhe nicht eingeschränkt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten einen Abstand aufweisen. Dieser Anwendungsfall ist der häufigste für Webseiten, die responsive Webdesign-Layoutrahmen wie Bootstrap und Foundation verwenden.

Wenn die Web-Seite andernfalls die Breite und Höhe für den Container des Viewers `DIV` festlegt, füllt der Viewer nur diesen Bereich und folgt der Größe, die das Layout der Web-Seite bietet. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

**Einbettung fester Größe**

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie Folgendes ausführen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Containers `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL Video360Viewer.js] einbeziehen. Die Datei [!DNL Video360Viewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf dem die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Referenzieren Sie nur die JavaScript `include` -Hauptdatei des Viewers auf Ihrer Seite. Referenzieren Sie keine zusätzlichen JavaScript-Dateien im Webseitencode, die möglicherweise von der Viewer-Logik zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die vom Viewer aus dem Kontextpfad `/s7viewers` geladene HTML5 SDK `Utils.js`-Bibliothek (das so genannte konsolidierte SDK `include`). Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig durch die Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Adobe hält ältere Versionen des sekundären Viewers `includes` nicht auf dem Server.
>
>
>Infolgedessen wird die Viewer-Funktion bei der Bereitstellung einer neuen Produktversion durch direkte Referenzierung auf alle sekundären JavaScript `include`, die vom Viewer auf der Seite verwendet werden, in Zukunft beeinträchtigt.

1. Definieren des Containers `DIV`.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres `DIV` -Element hinzu. Für das Element `DIV` muss die Kennung definiert sein, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird über CSS angegeben.

   Der Platzhalter `DIV` ist ein positioniertes Element, d. h. die CSS-Eigenschaft `position` ist auf `relative` oder `absolute` festgelegt.

   Damit die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert, dürfen keine anderen Elemente im DOM vorhanden sein, die eine höhere Stapelreihenfolge aufweisen als Ihr Platzhalter `DIV`.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalterelement `DIV` :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für die CSS-Klasse der obersten Ebene in absoluten Einheiten deklarieren oder den Modifikator `stagesize` verwenden.`.s7video360viewer`

   Sie können die Größe in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festlegen, die später einem Viewer-Vorgabendatensatz in Adobe Experience Manager Assets - On-Demand zugewiesen oder explizit mit dem Befehl `style` übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Video360-Viewers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf der HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Sie können den Modifikator `stagesize` im Viewer-Vorgabendatensatz in AEM Assets - On-Demand festlegen. Oder Sie können sie explizit mit dem Viewer-Initialisierungscode mit der `params` -Sammlung oder als API-Aufruf übergeben, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben:

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.Video360Viewer`, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode `init()` in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID und das verschachtelte JSON-Objekt `params` mit Konfigurationsparametern enthält, die vom Viewer unterstützt werden.

   In diesem Fall muss für das Objekt `params` mindestens die Image Serving-URL als `serverUrl`-Eigenschaft und das anfängliche Asset als `asset`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile, einer Videoserver-URL, die als `videoserverurl` -Eigenschaft übergeben wird, einem anfänglichen Asset als `asset` -Parameter und interaktiven Daten als `interactivedata` -Eigenschaft erstellen und starten. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder das body `onload()` -Ereignis auf.

   Gleichzeitig sollte das Containerelement nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit dem ihm zugewiesenen `display:none` -Stil ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. Im Beispiel wird von Folgendem ausgegangen:

   * Die Viewer-Instanz ist `video360Viewer`.
   * Der Name des Platzhalters `DIV` ist `s7viewer`.
   * Die Image-Serving-URL ist `https://s7d9.scene7.com/is/image`.
   * Die Videoserver-URL lautet &quot;`https://s7d9.scene7.com/is/content`&quot;.
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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Video360-Viewer mit einer festen Größe einbettet:

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

**Responsives Design, eingebettet in unbeschränkte Höhe**

Bei der Einbettung responsiver Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers `DIV` vorgibt. Im folgenden Beispiel nehmen Sie an, dass die Web-Seite es dem Container `DIV` des Viewers ermöglicht, 40 % der Fenstergröße des Webbrowsers zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten zum Einbetten fester Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Fügen Sie das Container-DIV zum vorhandenen DIV `"holder"` hinzu. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

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

Wenn eine responsive Einbettung mit definierter Breite und Höhe erfolgt, unterscheidet sich der Webseitenstil. Es bietet beide Größen für den DIV `"holder"` und zentriert ihn im Browserfenster. Außerdem setzt die Webseite die Größe der Elemente `HTML` und `BODY` auf 100 Prozent.

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

Die übrigen Schritte zum Einbetten sind mit den Schritten identisch, die für das responsive Einbetten mit uneingeschränkter Höhe verwendet werden. Das folgende Beispiel zeigt:

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

**Einbetten mit setFilter-basierter API**

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Verwendung der Einbettung mit fester Größe in die setter-basierte API:

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
