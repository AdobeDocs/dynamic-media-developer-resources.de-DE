---
description: Der Karussell-Viewer ist ein Viewer, der ein Karussell nicht zoombarer Bannerbilder mit klickbaren Hotspots oder Regionen anzeigt. Der Zweck dieses Viewers ist die Implementierung eines "Einkaufswagenerlebnisses", bei dem Benutzer einen Hotspot oder eine Region über dem Bannerbild auswählen und zu einer Quickview- oder Produktdetailseite auf der Website des Kunden umgeleitet werden können. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.
seo-description: Der Karussell-Viewer ist ein Viewer, der ein Karussell nicht zoombarer Bannerbilder mit klickbaren Hotspots oder Regionen anzeigt. Der Zweck dieses Viewers ist die Implementierung eines "Einkaufswagenerlebnisses", bei dem Benutzer einen Hotspot oder eine Region über dem Bannerbild auswählen und zu einer Quickview- oder Produktdetailseite auf der Website des Kunden umgeleitet werden können. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.
seo-title: Karussell
solution: Experience Manager
title: Karussell
topic: Dynamic media
uuid: 0ba4f40b-8dde-4479-b906-3115f09ab249
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Karussell{#carousel}

Der Karussell-Viewer ist ein Viewer, der ein Karussell nicht zoombarer Bannerbilder mit klickbaren Hotspots oder Regionen anzeigt. Der Zweck dieses Viewers ist die Implementierung eines &quot;Einkaufswagenerlebnisses&quot;, bei dem Benutzer einen Hotspot oder eine Region über dem Bannerbild auswählen und zu einer Quickview- oder Produktdetailseite auf der Website des Kunden umgeleitet werden können. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.

>[!NOTE]
>
>Bilder, die Image Rendering oder User-Generated Content (UGC) verwenden, werden von diesem Viewer nicht unterstützt.

Der Viewer-Typ ist 511.

## Demo-URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewerDemo.html)

## Systemanforderungen {#section-b7270cc4290043399681dc504f043609}

Siehe [Systemanforderungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Karussell-Viewer verwenden {#section-e6c68406ecdc4de781df182bbd8088b4}

Der Karussell-Viewer stellt eine Haupt-JavaScript-Datei und eine Reihe von Hilfedateien dar (ein einzelnes JavaScript enthält alle Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Der Karussell-Viewer kann sowohl im Popupmodus mit einer produktionsfertigen HTML-Seite, die mit IS Viewers bereitgestellt wird, als auch im eingebetteten Modus verwendet werden, wo er mithilfe der dokumentierten API in die Zielgruppe-Webseite integriert wird.

Konfigurationen und Skins ähneln denen anderer Viewer, die in dieser Hilfe beschrieben werden. Alle Skins werden mithilfe von benutzerdefiniertem CSS erreicht.

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem Karussell-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Das Navigieren durch den Karussellsatz erfolgt über eine horizontale Blättergeste über der Haupt-Ansicht oder mit zwei Pfeiltasten auf dem Desktop. Die Punkte für die Anzeige zeigen die aktuelle Position im Satz an.

Der Viewer kann Hotspots oder Regionen über dem Bannerbild rendern, um den interaktiven Bereich des Produkts anzuzeigen.

Durch Klicken oder Tippen auf einen Hotspot oder eine Region wird während der Autorenzeit eine Aktion ausgelöst, die mit dem Hotspot oder einer Region verknüpft ist. Die Aktion kann auf eine andere Seite der Website umgeleitet werden oder sie kann Produktinformationen an die Webseitenlogik zurückgeben, was wiederum eine Quickview mit verwandten Produktinhalten auslösen kann.

Der Viewer kann vollständig über die Tastatur aufgerufen werden.

Siehe [Barrierefreiheit und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)über die Tastatur.

## Karussell-Viewer einbetten {#section-6bb5d3c502544ad18a58eafe12a13435}

**Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Browserfenster-Bereich und passt sich an, falls die Größe des Browsers oder die Ausrichtung des Mobilgeräts geändert wird.

Der Popupmodus ist der häufigste für Mobilgeräte. Die Webseite lädt den Viewer mit dem `window.open()` JavaScript-Aufruf, dem ordnungsgemäß konfigurierten `A` HTML-Element oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. In diesem Fall wird es aufgerufen `CarouselViewer.html` und befindet sich im `html5/` Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

`<s7viewers_root>/html5/CarouselViewer.html`

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erzielen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, mit dem der Viewer in einem neuen Fenster geöffnet wird:

```
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**Einbettungsmodus mit fester Größe und Einbettungsmodus für reaktionsfähiges Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt. Diese Webseite enthält möglicherweise bereits Inhalte von Kunden, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilie einer Webseite.

Die wichtigsten Anwendungsfälle sind Webseiten, die auf Desktop- oder Tablet-Geräte ausgerichtet sind, und reaktionsfähige Seiten, die das Layout automatisch an den Gerätetyp anpassen.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Dies ist die beste Wahl für Webseiten mit einem statischen Layout.

Bei der responsiven Design-Einbettung wird davon ausgegangen, dass der Viewer die Größe zur Laufzeit ändern muss, je nach Größenänderung des Containers `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für reaktionsfähiges Design verhält sich der Viewer je nach Größe des Containers der Webseite unterschiedlich `DIV`. Wenn die Webseite nur die Breite des Containers festlegt `DIV`und dabei die Höhe unbegrenzt bleibt, wählt der Viewer die Höhe automatisch entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass es an den Seiten aufgefüllt werden muss. Dieser Anwendungsfall ist der häufigste Fall für Webseiten, die reaktionsfähige Webdesign-Layoutrahmen wie Bootstrap, Foundation usw. verwenden.

Andernfalls füllt der Viewer nur diesen Bereich, wenn die Webseite sowohl die Breite als auch die Höhe des Containers des Viewers festlegt `DIV`. Es folgt auch der Größe des Webseitenlayouts. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung je nach Webbrowser-Fenstergröße angepasst wird.

**Einbettung fester Größe**

Der Viewer wird wie folgt zu einer Webseite hinzugefügt:

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Containers `DIV`.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite

   Zum Erstellen eines Viewers müssen Sie im HTML-Kopf ein Skript-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL CarouselViewer.js]dies berücksichtigen. Die [!DNL CarouselViewer.js] Datei befindet sich im [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>Sie sollten nur auf die JavaScript- `include` Hauptdatei des Viewers auf Ihrer Seite verweisen. Sie sollten keine weiteren JavaScript-Dateien im Webseitencode referenzieren, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die vom Viewer aus dem `Utils.js` Kontextpfad (so genanntes konsolidiertes SDK) geladene HTML5 SDK- `/s7viewers` Bibliothek `include`. Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig durch die Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Ältere Versionen des sekundären Viewers werden von Adobe nicht `includes` auf dem Server gespeichert.
>
>
>Infolgedessen wird die Viewer-Funktion bei der Bereitstellung einer neuen Produktversion durch direkte Verweise auf sekundäres JavaScript, das vom Viewer auf der Seite `include` verwendet wird, in Zukunft unterbrochen.

1. Definieren des Containers `DIV`.

   Hinzufügen Sie ein leeres `DIV` Element auf der Seite, auf der der Viewer angezeigt werden soll. Die ID des `DIV` Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird durch CSS festgelegt.

   Der Platzhalter `DIV` ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute`eingestellt.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalterelement `DIV` :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Einstellen der Viewer-Größe

   Sie können die statische Größe des Viewers festlegen, indem Sie ihn entweder für die CSS-Klasse der `.s7carouselviewer` obersten Ebene in absoluten Einheiten deklarieren oder einen `stagesize` Modifikator verwenden.

   Sie können die Größe in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festlegen, die später einem Viewer-Vorgabendatensatz in AEM Assets zugewiesen wird - auf Anforderung oder explizit mit dem `style` Befehl weitergegeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Karussell-Viewers](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Im Folgenden finden Sie ein Beispiel zum Definieren einer statischen Viewer-Größe auf der HTML-Seite:

   ```
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Sie können den `stagesize` Modifikator explizit mit dem Viewer-Initialisierungscode an die `params` Sammlung oder als API-Aufruf übergeben, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben:

   ```
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der `s7viewers.CarouselViewer` Klasse, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode für eine Viewer-Instanz auf `init()` . Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über ein `containerId` Feld verfügen, das den Namen der Viewer-Container-ID und das verschachtelte `params` JSON-Objekt mit vom Viewer unterstützten Konfigurationsparametern enthält. In diesem Fall muss für das `params` Objekt mindestens die Image Serving-URL als `serverUrl` -Eigenschaft und das ursprüngliche Asset als `asset` -Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und mit einem Beginn versehen.

   Es ist wichtig, dass der Viewer-Container dem DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser zögern die Erstellung von DOM bis zum Ende der Webseite. Um eine maximale Kompatibilität zu gewährleisten, rufen Sie die `init()` Methode direkt vor dem schließenden `BODY` Tag oder im Body- `onload()` Ereignis auf.

   Gleichzeitig sollte das Container-Element nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mithilfe des ihr zugewiesenen `display:none` Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das die erforderlichen Mindestkonfigurationsoptionen an den Konstruktor übergibt und die `init()` Methode aufruft. Im Beispiel wird davon ausgegangen, dass `carouselViewer` es sich um die Viewer-Instanz handelt. der Name `s7viewer` des Platzhalters `DIV`; ist `https://adobedemo62-h.assetsadobe.com/is/image` die Image Serving-URL und `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` das Asset:

   ```
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, die den Karussell-Viewer mit einer festen Größe einbettet:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsive Design-Einbettung mit unbeschränkter Höhe**

Bei der Integration reaktionsfähiger Designs verfügt die Webseite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers vorgibt `DIV`. Nehmen wir beispielsweise an, dass der Container des Viewers auf der Webseite 40 % der Größe des Webbrowser-Fensters `DIV` annehmen kann. Und seine Höhe bleibt unbegrenzt. Der HTML-Code der Webseite würde wie folgt aussehen:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 80%; 
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
1. Definieren des Containers `DIV`.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind identisch mit denen der Einbettung in fester Größe. Hinzufügen Sie den Container `DIV` zum bestehenden `"holder"``DIV`. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 80%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Die folgende Beispielseite zeigt die aktuelleren Einsatzmöglichkeiten von reaktionsfähigem Design-Einbettung mit uneingeschränkter Höhe:

[https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/CarouselViewer-responsive-unrestricted-height.html)

**Flexible Einbettung mit definierter Breite und Höhe**

Bei Einbettung in flexibler Größe mit definierter Breite und Höhe ist der Webseitenstil anders. Es bietet beide Größen für das `"holder"` DIV und zentriert es im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und des `BODY` Elements auf 100 Prozent.

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
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Einbetten mithilfe der Setter-basierten API**

Anstatt JSON-basierte Initialisierung zu verwenden, ist es möglich, set-basierte API- und no-args-Konstruktoren zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit `setContainerId()`-, `setParam()`- und `setAsset()` -API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Im folgenden Beispiel wird die Einbettung in feste Größe mit der setter-basierten API veranschaulicht:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```

