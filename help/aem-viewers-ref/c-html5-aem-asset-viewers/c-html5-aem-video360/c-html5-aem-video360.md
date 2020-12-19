---
description: Der HTML5 Video360 Viewer ist ein 360-Grad-Videoplayer, der Streaming- und progressive 360-Videos abspielt, die im H.264-Format kodiert wurden und vom Scene7 Publishing System oder von AEM Dynamic Media geliefert werden.
seo-description: Der HTML5 Video360 Viewer ist ein 360-Grad-Videoplayer, der Streaming- und progressive 360-Videos abspielt, die im H.264-Format kodiert wurden und vom Scene7 Publishing System oder von AEM Dynamic Media geliefert werden.
seo-title: Video360
solution: Experience Manager
title: Video360
topic: Dynamic media
uuid: b03e6289-e012-4c62-835f-814463a27774
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '2613'
ht-degree: 0%

---


# Video360{#video}

Der HTML5 Video360 Viewer ist ein 360-Grad-Videoplayer, der Streaming- und progressive 360-Videos abspielt, die im H.264-Format kodiert wurden und vom Scene7 Publishing System oder von AEM Dynamic Media geliefert werden.

360-Grad-Videos, auch als immersive Videos oder kugelförmige Videos bezeichnet, sind Videoaufnahmen, bei denen eine Ansicht in jede Richtung gleichzeitig aufgezeichnet wird, die mit einer Allrichtungskamera oder einer Kamerasammlung aufgenommen wurden. Es werden sowohl einzelne Video- als auch adaptive Videosets unterstützt. Der Viewer unterstützt außerdem die Arbeit mit progressiven Video- und HLS-Streams, die auf einem externen Speicherort gehostet werden.

Das empfohlene Seitenverhältnis für 360-Videos ist 2:1. Rauschunterdrückung wird nicht unterstützt. Der Viewer kann nur mit 360 Videos verwendet werden. Wenn Sie versuchen, ein Video abzuspielen, das nicht 360 ist, wird die Videowiedergabe verzerrt.

Der Viewer wurde für die Verwendung mit Desktop- und mobilen Webbrowsern entwickelt, die HTML5-Videos unterstützen. Der Viewer unterstützt optionale Werkzeuge zum Weitergeben in sozialen Netzwerken.

Der Video360-Viewer verwendet die HTML5-Streaming-Videowiedergabe im HLS-Format in seiner Standardkonfiguration, wenn das zugrunde liegende System dies unterstützt. Auf Systemen, die kein HTML5-Streaming unterstützen, greift der Viewer auf den progressiven HTML5-Versand zurück.

Der Viewer-Typ ist 517.

## Demo-URLs {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Systemanforderungen {#section-b7270cc4290043399681dc504f043609}

Siehe [Systemanforderungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Verwenden von Video360 Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Der HTML5-Video360-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar (ein einzelnes JavaScript enthält alle von diesem Viewer verwendeten HTML5-Viewer-SDK-Komponenten, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Der HTML5 Video360 Viewer kann sowohl im Popupmodus mithilfe einer produktionsfertigen HTML-Seite, die mit IS-Viewern bereitgestellt wird, als auch im eingebetteten Modus verwendet werden, wobei er mithilfe der dokumentierten API in die Zielgruppe-Webseite integriert wird.

Konfiguration und Skin ähneln denen der anderen in diesem Handbuch beschriebenen Viewer. Alle Skins werden mithilfe von CSS (Custom Cascading Style Sheets) realisiert.

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz, die allen Viewern gemein ist - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Für 360-Videoinhalte sind höhere Kodierungseinstellungen erforderlich als für Videos, die nicht dem 360-Standard entsprechen. Das heißt, 360 Inhalte müssen in einer höheren Auflösung als 360 Videos vorliegen, um die gleiche wahrnehmbare Qualität zu erzielen. Es wird empfohlen, die folgenden Einstellungen für adaptive Video-Vorgaben für 360-Videos zu berücksichtigen:

* 720p, 2500 Kbit/s
* 1080p, 5000 Kbit/s
* 1440p, 6600 Kbit/s

Beachten Sie jedoch, dass die Bereitstellung von Videos, die mit solchen Einstellungen hoher Qualität kodiert wurden, eine Verbindung mit hoher Bandbreite auf dem Gerät des Endbenutzers erfordert.

## Interaktion mit Video360 Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der HTML5 Video360 Viewer bietet eine Reihe standardmäßiger Steuerelemente der Benutzeroberfläche für die Videowiedergabe, z. B. &quot;Abspielen/Anhalten&quot;-Schaltfläche, Video-Scrubber-Videozeitblase, Wiedergabedauer/Gesamtzeit-Indikator, Lautstärkeregler und Vollbildschaltfläche. Alle diese Steuerelemente werden in der Steuerleiste ganz unten in der Benutzeroberfläche des Viewers gruppiert.

Beachten Sie, dass auf Touch-Geräten die Lautstärkeregelung in der Benutzeroberfläche ausgeblendet ist, da die Lautstärke nur über die Hardwareschaltflächen des Geräts gesteuert werden kann.

Wenn der Viewer im Popupmodus ausgeführt wird, ist in der Benutzeroberfläche keine Vollbildschaltfläche verfügbar.

Der Viewer unterstützt außerdem eine Reihe von Social Media-Sharing-Werkzeugen. Sie stehen als eine einzige Schaltfläche in der Benutzeroberfläche zur Verfügung, die durch Klicken oder Tippen auf eine Freigabebeschaltfläche in eine Freigabebeschaltfläche umgewandelt wird. Die Freigabe-Symbolleiste enthält ein Symbol für jeden unterstützten Freigabetyp, z. B. Facebook, Twitter, E-Mail-Freigabe, Einbettungscode-Freigabe und Linkfreigabe. Wenn die Tools für die Freigabe per E-Mail, die Einbettung von Teilen oder die Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Dateneingabeformular an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer über einen Social Media-Dienst zu einem Standardfreigabedialogfeld um. Wenn ein Freigabe-Tool aktiviert ist, wird die Videowiedergabe automatisch angehalten. Die Freigabe von Werkzeugen ist im Vollbildmodus aufgrund von Webbrowser-Sicherheitsbeschränkungen nicht verfügbar.

Der Viewer unterstützt 360 Videowiedergaben auf VR-Headsets (wie Oculus Go und Oculus Rift), VR HMD (Head-Motion Display)-Halterungen (wie Google Pboard) und nicht für VR geeignete Geräte (wie Desktop-Browser, Tablets und Mobiltelefone, die nicht mit VR HMD-Halterungen verbunden sind).

Zur Ansicht von 360-Videoinhalten auf VR-Headset ist keine zusätzliche Konfiguration erforderlich. Der Viewer erkennt automatisch das Vorhandensein des VR-Headsets und zeigt die Schaltfläche &quot;VR&quot;über dem Videoinhalt an. Durch Aktivierung dieser &quot;VR&quot;-Schaltfläche wird die Videowiedergabe in den VR-Modus umgeschaltet. Der Viewer unterstützt das VR-Rendering nur in Browsern mit WebVR-Unterstützung.

Um VR HMD-Anschlüsse verwenden zu können, muss der Modifikator `Video360Player.vrrender` in der Konfiguration des Viewers auf `1` eingestellt werden, was das stereoskopische Rendering erzwingt.

Bei VR-Headsets und VR-HMD-Befestigungspunkten erfolgt eine Änderung der Ansicht je nach Headset-Bewegung. Im VR-Modus wird keine andere Wiedergabesteuerung bereitgestellt.

Beim Anzeigen von 360 Videos auf Geräten ohne VR-Unterstützung kann der Endbenutzer die Video-Wiedergabe und -Ansicht mit Maus, Touch oder Tastatur steuern.

Der Viewer unterstützt sowohl Berührungseingaben als auch Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.

Der Viewer kann vollständig über die Tastatur aufgerufen werden. Siehe [Barrierefreiheit und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten von Video360 Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, über den der Viewer bei einem Klick in einem separaten Browserfenster geöffnet wird. In anderen Fällen ist es erforderlich, den Viewer direkt auf der Hostingseite einzubetten. Im letzteren Fall verfügt die Webseite möglicherweise über ein statisches Seitenlayout oder über ein reaktionsfähiges Design, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung in fester Größe und Einbettung in reaktionsfähiges Design.

Das Einbetten mehrerer Videos auf derselben Seite wird auf Tablets und Mobilgeräten unterstützt. In den meisten Fällen kann jeweils nur ein Video abgespielt werden. Wenn ein Beginn ein Video abspielt und dann versucht, ein weiteres Video abzuspielen, wird das erste Video automatisch angehalten. Das automatisch angehaltene Video speichert seine aktuelle Wiedergabezeit, sodass der Benutzer jederzeit darauf zurückgreifen und die Wiedergabe fortsetzen kann. Die einzige Ausnahme für diese Regel ist der Chrome-Browser auf Android 4.x-Geräten, die Videos parallel abspielen können.

**Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Browserfenster-Bereich und passt sich an, falls die Größe des Browsers oder die Geräteausrichtung geändert wird.

Dieser Modus ist der am häufigsten verwendete für Mobilgeräte. Die Webseite lädt den Viewer mit dem JavaScript-Aufruf `window.open()`, dem ordnungsgemäß konfigurierten `A` HTML-Element oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Es heißt [!DNL Video360Viewer.html] und befindet sich im Unterordner [!DNL html5/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erzielen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, mit dem der Viewer in einem neuen Fenster geöffnet wird:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Einbettungsmodus mit fester Größe und Einbettungsmodus für reaktionsfähiges Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer zusammenhängen. Der Viewer belegt normalerweise nur einen Teil der Immobilie einer Webseite.

Die wichtigsten Anwendungsfälle sind Webseiten, die auf Desktop- oder Tablet-Geräte ausgerichtet sind, sowie reaktionsfähige Seiten, die das Layout automatisch an den Gerätetyp anpassen.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Dies ist die beste Wahl für Webseiten mit einem statischen Layout.

Bei der responsiven Designeinbettung wird davon ausgegangen, dass die Größe des Viewers zur Laufzeit entsprechend der Größenänderung des Containers `DIV` ggf. angepasst werden muss. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für reaktionsfähiges Design verhält sich der Viewer je nach Größe des Containers `DIV` der Webseite unterschiedlich. Wenn auf der Webseite nur die Breite des Containers `DIV` festgelegt wird und die Höhe nicht eingeschränkt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass es an den Seiten aufgefüllt werden muss. Dieser Anwendungsfall ist der häufigste Fall für Webseiten mit reaktionsfähigen Webdesign-Layoutrahmen wie Bootstrap, Foundation usw.

Andernfalls füllt der Viewer, wenn die Webseite sowohl die Breite als auch die Höhe des Containers des Viewers `DIV` festlegt, nur diesen Bereich und folgt der vom Webseitenlayout bereitgestellten Größe. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung je nach Webbrowser-Fenstergröße angepasst wird.

**Einbettung fester Größe**

Der Viewer wird wie folgt zu einer Webseite hinzugefügt:

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Containers `DIV`.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite

   Zum Erstellen eines Viewers müssen Sie im HTML-Kopf ein Skript-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL Video360Viewer.js] einschließen. Die Datei [!DNL Video360Viewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Dynamic Media Classic-Server der Adobe bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Server der Adobe Dynamic Media Classic an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Sie sollten nur auf die JavaScript-Hauptdatei des Viewers `include` auf Ihrer Seite verweisen. Sie sollten keine weiteren JavaScript-Dateien im Webseitencode referenzieren, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Insbesondere sollten Sie nicht direkt auf die HTML5 SDK `Utils.js`-Bibliothek verweisen, die vom Viewer aus dem Kontextpfad `/s7viewers` geladen wird (so genanntes konsolidiertes SDK `include`). Der Grund dafür ist, dass der Speicherort von `Utils.js`- oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig durch die Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Ältere Versionen des sekundären Viewers `includes` werden von der Adobe nicht auf dem Server gespeichert.
>
>
>Infolgedessen wird die Viewer-Funktionalität bei der Bereitstellung einer neuen Produktversion durch die direkte Referenz auf sekundäres JavaScript `include`, das vom Viewer auf der Seite verwendet wird, in Zukunft unterbrochen.

1. Definieren des Containers `DIV`.

   hinzufügen Sie ein leeres `DIV`-Element auf die Seite, auf der der Viewer angezeigt werden soll. Das `DIV`-Element muss seine ID definiert haben, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird durch CSS festgelegt.

   Der Platzhalter `DIV` ist ein positioniertes Element, d. h., die CSS-Eigenschaft ist auf `relative` oder `absolute` eingestellt.`position`

   Damit die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert, müssen Sie sicherstellen, dass keine anderen Elemente im DOM vorhanden sind, die eine höhere Stapelreihenfolge aufweisen als Ihr Platzhalter `DIV`.

   Das folgende Beispiel zeigt ein definiertes Platzhalterelement `DIV`:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Einstellen der Viewer-Größe

   Sie können die statische Größe des Viewers festlegen, indem Sie sie entweder für die CSS-Klasse der obersten Ebene in absoluten Maßeinheiten deklarieren oder indem Sie den Modifikator `stagesize` verwenden.`.s7video360viewer`

   Sie können die Größe in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festlegen, die später einem Viewer-Vorgabendatensatz in AEM Assets zugewiesen wird - On-Demand oder explizit mit dem Befehl `style` weitergegeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Video360-Viewers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0).

   Im Folgenden finden Sie ein Beispiel zum Definieren einer statischen Viewer-Größe auf der HTML-Seite:

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Sie können den Modifikator `stagesize` im Viewer-Vorgabendatensatz in AEM Assets - On-Demand festlegen. Oder Sie können sie explizit mit dem Viewer-Initialisierungscode mit der Sammlung `params` oder als API-Aufruf, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben, übergeben:

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.Video360Viewer`, geben Sie alle Konfigurationsinformationen an den Konstruktor weiter und rufen Sie die Methode `init()` für eine Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID und das verschachtelte `params`-JSON-Objekt mit vom Viewer unterstützten Konfigurationsparametern enthält.

   In diesem Fall muss für das `params`-Objekt mindestens die Image Serving-URL als `serverUrl`-Eigenschaft und das ursprüngliche Asset als `asset`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und mit einer Videoserver-URL, die als `videoserverurl`-Eigenschaft übergeben wird, einem anfänglichen Asset als `asset`-Parameter und interaktiven Daten als `interactivedata`-Eigenschaft übergeben. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und Beginn erstellen.

   Es ist wichtig, dass der Viewer-Container dem DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser zögern die Erstellung von DOM bis zum Ende der Webseite. Um eine maximale Kompatibilität zu gewährleisten, rufen Sie die `init()`-Methode direkt vor dem schließenden `BODY`-Tag oder im Body `onload()`-Ereignis auf.

   Gleichzeitig sollte das Container-Element nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mit dem `display:none`-Stil ausgeblendet werden, der ihm zugewiesen wurde. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das die notwendigen Mindestkonfigurationsoptionen an den Konstruktor übergibt und die `init()`-Methode aufruft. Das Beispiel geht von Folgendem aus:

   * Die Viewer-Instanz ist `video360Viewer`.
   * Der Name des Platzhalters `DIV` ist `s7viewer`.
   * Die Image Serving-URL ist `https://s7d9.scene7.com/is/image`.
   * Die URL des Videoservers ist `https://s7d9.scene7.com/is/content`.
   * Das Asset ist `Viewers/space_station_360-AVS`.

   ```
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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, die den Video360-Viewer mit einer festen Größe einbettet:

   ```
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

**Responsive Design-Einbettung mit unbeschränkter Höhe**

Bei der Integration reaktionsfähiger Designs verfügt die Webseite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers `DIV` vorgibt. Im folgenden Beispiel nehmen Sie an, dass die Webseite dem Container des Viewers `DIV` erlaubt, 40 % der Größe des Webbrowser-Fensters zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite würde wie folgt aussehen:

```
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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten zum Einbetten in feste Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind identisch mit denen der Einbettung in fester Größe. hinzufügen Sie den Container DIV an das vorhandene `"holder"` DIV. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```
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

Bei responsiver Einbettung mit definierter Breite und Höhe ist der Webseitenstil anders. Es stellt beide Größen für das DIV `"holder"` bereit und zentriert es im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und `BODY` auf 100 Prozent.

```
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

Die übrigen Einbettungsschritte sind identisch mit den Schritten, die für eine reaktionsfähige Einbettung mit uneingeschränkter Höhe verwendet werden. Das resultierende Beispiel lautet:

```
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

Anstatt JSON-basierte Initialisierung zu verwenden, ist es möglich, set-basierte API- und no-args-Konstruktoren zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` und mit separaten JavaScript-Aufrufen angegeben.

Im folgenden Beispiel wird die Einbettung in feste Größe mit der setter-basierten API veranschaulicht:

```
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

