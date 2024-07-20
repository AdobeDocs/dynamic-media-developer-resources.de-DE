---
title: Karussell
description: Karussell-Viewer ist ein Viewer, der ein Karussell nicht zoombarer Bannerbilder mit klickbaren Hotspots oder Regionen anzeigt. Mit diesem Viewer können Sie ein Karussellerlebnis mit Shopping-Funktion implementieren, bei dem Benutzer einen Hotspot oder eine Region über dem Bannerbild auswählen können. Sie können zu einer Schnellansichts- oder Produktdetailseite auf der Website des Kunden weitergeleitet werden. Es wurde für Desktops und Mobilgeräte entwickelt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d506dc6e-8929-4f7f-a205-1683e77681f1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1867'
ht-degree: 0%

---

# Karussell{#carousel}

Karussell-Viewer ist ein Viewer, der ein Karussell nicht zoombarer Bannerbilder mit klickbaren Hotspots oder Regionen anzeigt. Mit diesem Viewer können Sie ein Karussellerlebnis mit Shopping-Funktion implementieren, bei dem Benutzer einen Hotspot oder eine Region über dem Bannerbild auswählen können. Sie können zu einer Schnellansichts- oder Produktdetailseite auf der Website des Kunden weitergeleitet werden. Es wurde für Desktops und Mobilgeräte entwickelt.

>[!NOTE]
>
>Bilder, die Image Rendering oder benutzergenerierte Inhalte (UGC) verwenden, werden von diesem Viewer nicht unterstützt.

Der Viewer-Typ ist 511.

## Demo-URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html)

## Systemanforderungen {#section-b7270cc4290043399681dc504f043609}

Siehe [Systemanforderungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Verwenden des Karussellanzeige {#section-e6c68406ecdc4de781df182bbd8088b4}

Der Karussell-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar (eine JavaScript-Datei enthält alle Viewer-SDK-Komponenten, die von diesem Viewer, den Assets und CSS verwendet werden), die vom Viewer zur Laufzeit heruntergeladen wurden.

Karussell-Viewer können sowohl im Popup-Modus mit einer produktionsbereiten HTML-Seite mit IS-Viewern verwendet werden als auch im eingebetteten Modus, wo sie mithilfe einer dokumentierten API in die Ziel-Web-Seite integriert wird.

Die Konfiguration und das Skinning ähneln denen der anderen in dieser Hilfe beschriebenen Viewer. Die gesamte Skinning-Funktion wird über benutzerdefiniertes CSS erreicht.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit Karussellansicht {#section-642e66ca38cd4032992840ec6c0b0cd2}

Das Navigieren durch das Karussellset erfolgt über eine horizontale Wischbewegung über die Hauptansicht oder mit zwei Pfeiltasten, die auf dem Desktop-Gerät verfügbar sind. Anzeigepunkte festlegen zeigt die aktuelle Position im Satz an.

Der Viewer kann Hotspots oder Regionen über dem Bannerbild rendern, um den interaktiven Bereich im Produkt anzuzeigen.

Durch Klicken oder Tippen auf einen Hotspot oder eine Region wird während der Autorenzeit eine mit ihm verknüpfte Aktion Trigger. Die Aktion kann auf eine andere Seite der Website umgeleitet werden oder sie kann Produktinformationen zurück an die Webseitenlogik übergeben, wodurch wiederum eine Schnellansicht mit zugehörigen Produktinhalten Trigger werden kann.

Der Viewer ist vollständig über die Tastatur zugänglich.

Siehe [Barrierefreiheit und Navigation auf der Tastatur](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten von Karussell-Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Bereich des Browser-Fensters und passt sich an, falls die Größe des Browsers geändert wird oder die Ausrichtung eines Mobilgeräts geändert wird.

Der Pop-up-Modus ist der häufigste für Mobilgeräte. Die Webseite lädt den Viewer mit dem Aufruf `window.open()` JavaScript , dem ordnungsgemäß konfigurierten Element `A` HTML oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. In diesem Fall wird es als `CarouselViewer.html` bezeichnet und befindet sich im Unterordner `html5/` Ihrer standardmäßigen IS-Viewer-Bereitstellung:

`<s7viewers_root>/html5/CarouselViewer.html`

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erreichen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```html {.line-numbers}
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**Über den Einbettungsmodus mit fester Größe und den Einbettungsmodus für responsives Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt. Diese Webseite kann bereits über Kundeninhalte verfügen, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Seiten, auf denen das Layout automatisch an den Gerätetyp angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Methode eignet sich am besten für Webseiten mit statischem Layout.

Responsives Einbetten von Design setzt voraus, dass die Größe des Viewers zur Laufzeit geändert werden muss, um auf die Größenänderung des Containers `DIV` reagieren zu können. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für responsive Designs verhält sich der Viewer unterschiedlich, je nachdem, wie die Größe des Containers auf der Webseite angepasst wird `DIV`. Wenn die Webseite nur die Breite des Containers &quot;`DIV`&quot; festlegt und die Höhe nicht eingeschränkt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten einen Abstand aufweisen. Dieser Anwendungsfall ist der häufigste für Webseiten, die responsive Webdesign-Layoutrahmen wie Bootstrap und Foundation verwenden.

Andernfalls füllt der Viewer nur diesen Bereich aus, wenn die Web-Seite sowohl die Breite als auch die Höhe für den Container des Viewers `DIV` festlegt. Es folgt auch der Größe, die das Webseitenlayout bietet. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

**Einbettung fester Größe**

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie Folgendes ausführen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Containers `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL CarouselViewer.js] einbeziehen. Die Datei [!DNL CarouselViewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf dem die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
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

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalterelement `DIV` :

   ```CSS {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für die CSS-Klasse der obersten Ebene in absoluten Einheiten deklarieren oder den Modifikator `stagesize` verwenden.`.s7carouselviewer`

   Sie können die Größenanpassung in CSS direkt auf die HTML-Seite setzen. Oder Sie können die Größe in eine benutzerdefinierte Viewer-CSS-Datei einfügen, die später in AEM Assets einem Viewer-Vorgabendatensatz zugewiesen - On-Demand oder explizit mit dem Befehl `style` übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Karussell-Viewers](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf der HTML-Seite:

   ```CSS {.line-numbers}
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Sie können den Modifikator `stagesize` explizit mit dem Viewer-Initialisierungscode mit der Sammlung `params` oder als API-Aufruf übergeben, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben:

   ```CSS {.line-numbers}
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.CarouselViewer`, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode `init()` in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID und das verschachtelte JSON-Objekt `params` mit Konfigurationsparametern enthält, die vom Viewer unterstützt werden. In diesem Fall muss für das Objekt `params` mindestens die Image Serving-URL als `serverUrl`-Eigenschaft und das anfängliche Asset als `asset`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder das body `onload()` -Ereignis auf.

   Gleichzeitig sollte das Containerelement nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit dem ihm zugewiesenen `display:none` -Stil ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Wenn diese Funktion auftritt, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. Im Beispiel wird angenommen, dass `carouselViewer` die Viewer-Instanz ist; `s7viewer` der Name des Platzhalters `DIV`; `https://adobedemo62-h.assetsadobe.com/is/image` die Image Serving-URL und `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` das Asset ist:

   ```javascript {.line-numbers}
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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Karussell-Viewer mit einer festen Größe einbettet:

   ```html {.line-numbers}
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

**Responsives Design, eingebettet in unbeschränkte Höhe**

Bei der Einbettung responsiver Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers `DIV` vorgibt. Für das folgende Beispiel nehmen Sie an, dass die Webseite es dem Container `DIV` des Viewers ermöglicht, 40 % der Fenstergröße des Webbrowsers zu übernehmen. Und seine Höhe bleibt unbegrenzt. Der HTML-Code der Webseite würde wie folgt aussehen:

```html {.line-numbers}
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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten zum Einbetten fester Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Containers `DIV`.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Fügen Sie den Container `DIV` der vorhandenen `"holder"` `DIV` hinzu. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```html {.line-numbers}
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

Die folgende Beispielseite zeigt die reale Nutzung responsiver Designs, die mit unbegrenzter Höhe eingebettet werden:

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html)

**Flexible Größe Einbetten mit definierter Breite und Höhe**

Bei der Einbettung in flexibler Größe mit definierter Breite und Höhe unterscheidet sich der Webseitenstil. Es bietet beide Größen für den DIV `"holder"` und zentriert ihn im Browserfenster. Außerdem setzt die Webseite die Größe der Elemente `HTML` und `BODY` auf 100 Prozent.

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

**Einbetten mit setFilter-basierter API**

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Verwendung der Einbettung mit fester Größe in die setter-basierte API:

```html {.line-numbers}
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
