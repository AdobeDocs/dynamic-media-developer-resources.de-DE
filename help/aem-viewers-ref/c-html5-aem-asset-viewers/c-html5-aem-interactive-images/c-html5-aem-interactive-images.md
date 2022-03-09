---
title: Interaktives Bild
description: Der Viewer für interaktive Bilder ist ein Viewer, der ein einzelnes, nicht zoombares Bild mit klickbaren Hotspots anzeigt. Der Zweck dieses Viewers besteht darin, ein "Shop-fähiges Banner"-Erlebnis zu implementieren. Das heißt, der Benutzer kann einen Hotspot über dem Bannerbild auswählen und zu einer Schnellansichts- oder Produktdetailseite auf Ihrer Website weitergeleitet werden. Es wurde für Desktops und Mobilgeräte entwickelt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1720'
ht-degree: 0%

---

# Interaktives Bild{#interactive-image}

Der Viewer für interaktive Bilder ist ein Viewer, der ein einzelnes, nicht zoombares Bild mit klickbaren Hotspots anzeigt. Der Zweck dieses Viewers besteht darin, ein &quot;Shop-fähiges Banner&quot;-Erlebnis zu implementieren. Das heißt, der Benutzer kann einen Hotspot über dem Bannerbild auswählen und zu einer Schnellansichts- oder Produktdetailseite auf Ihrer Website weitergeleitet werden. Es wurde für Desktops und Mobilgeräte entwickelt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Der Viewer-Typ ist 508.

## Demo-URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## Systemanforderungen {#section-b7270cc4290043399681dc504f043609}

Siehe [Systemanforderungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Verwenden des interaktiven Bild-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der Viewer für interaktive Bilder stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar (ein einzelnes JavaScript-Include mit allen Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Der interaktive Bild-Viewer kann nur im eingebetteten Modus verwendet werden, wo er mithilfe der dokumentierten API in die Ziel-Web-Seite integriert wird.

Die Konfiguration und das Skinning ähneln denen der anderen in dieser Hilfe beschriebenen Viewer. Alle Skins werden über benutzerdefiniertes CSS erstellt.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem interaktiven Bild-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Die vom Video Image Viewer unterstützte Interaktion ist die Aktivierung von Hotspots auf Desktop-Systemen. Diese Aktivierung erfolgt bei Klick- und Touch-Geräten mit einem einzigen Tippen.

Auf den Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Tastaturzugriff und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des interaktiven Bild-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Der interaktive Bild-Viewer ist in die Hosting-Seite eingebettet. Eine solche Webseite kann ein statisches Layout aufweisen oder &quot;responsiv&quot;sein und auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt werden.

Um diese Anforderungen zu erfüllen, unterstützt der Viewer zwei primäre Betriebsmodi: Einbetten in feste Größe und responsives Einbetten.

**Über den Einbettungsmodus mit fester Größe und den Einbettungsmodus für responsives Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt. Diese Webseite kann bereits über Kundeninhalte verfügen, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Seiten, auf denen das Layout automatisch an den Gerätetyp angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Methode eignet sich am besten für Webseiten mit statischem Layout.

Responsives Design-Einbetten setzt voraus, dass die Größe des Viewers zur Laufzeit geändert werden muss, wenn die Größe des Containers geändert wird `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für responsives Design verhält sich der Viewer unterschiedlich, je nachdem, wie die Web-Seite den Container dimensioniert `DIV`. Wenn die Webseite nur die Breite des Containers festlegt `DIV`Wenn die Höhe nicht eingeschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten einen Abstand aufweisen. Dieser Anwendungsfall ist der häufigste bei Webseiten, die responsive Webdesign-Layoutrahmen wie Bootstrap und Foundation verwenden.

Andernfalls, wenn die Webseite sowohl die Breite als auch die Höhe für den Container des Viewers festlegt `DIV`, füllt der Viewer nur diesen Bereich aus. Es folgt auch der Größe, die das Webseitenlayout bietet. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

**Einbettung fester Größe**

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie wie folgt vorgehen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Container definieren `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL InterativeImage.js]. Die [!DNL InteractiveImage.js] befindet sich unter der [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf dem die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Nur auf das JavaScript des Haupt-Viewers verweisen `include` -Datei auf Ihrer Seite. Referenzieren Sie keine zusätzlichen JavaScript-Dateien im Webseitencode, die möglicherweise von der Viewer-Logik zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf das HTML5 SDK. `Utils.js` Bibliothek, die vom Viewer aus geladen wird `/s7viewers` Kontextpfad (so genanntes konsolidiertes SDK) `include`). Der Grund dafür ist, dass der Standort `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig von der Logik des Viewers verwaltet und der Speicherort zwischen Viewer-Versionen geändert wird. Adobe behält ältere Versionen des sekundären Viewers nicht bei `includes` auf dem Server.
>
>
>Daher können Sie einen direkten Verweis auf sekundäres JavaScript einfügen `include` wird vom Viewer auf der Seite verwendet und unterbricht die Viewer-Funktionalität in Zukunft, wenn eine neue Produktversion bereitgestellt wird.

1. Container definieren `DIV`.

   Leeren hinzufügen `DIV` -Element zu der Seite hinzugefügt, auf der der Viewer angezeigt werden soll. Die `DIV` -Element muss seine ID definiert haben, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird über CSS angegeben.

   Der Platzhalter `DIV` ein positioniertes Element ist, d. h., das `position` Die CSS-Eigenschaft ist auf `relative` oder `absolute`.

   Im Folgenden finden Sie ein Beispiel für einen definierten Platzhalter. `DIV` element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für `.s7interactiveimage` CSS-Klasse der obersten Ebene in absoluten Einheiten oder durch Verwendung von `stagesize` -Modifikator.

   Sie können die Größenanpassung in CSS direkt auf die HTML-Seite setzen. Oder Sie können die Größe in eine benutzerdefinierte Viewer-CSS-Datei einfügen, die später in Adobe Experience Manager Assets On-Demand einem Viewer-Vorgabendatensatz zugewiesen oder explizit mit `style` Befehl.

   Siehe [Video](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) Weitere Informationen zum Formatieren des Viewers mit CSS.

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf der HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Sie können die `stagesize` Modifikator mit dem Viewer-Initialisierungscode mit `params` -Sammlung oder als API-Aufruf, wie im Abschnitt Befehlsreferenz beschrieben:

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz von `s7viewers.InteractiveImage` -Klasse, übergeben Sie alle Konfigurationsinformationen an den -Konstruktor und rufen Sie `init()` -Methode in einer Viewer-Instanz verwenden. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens `containerId` -Feld, das den Namen der Viewer-Container-ID und verschachtelt enthält `params` JSON-Objekt mit Konfigurationsparametern, die vom Viewer unterstützt werden. In diesem Fall wird die `params` -Objekt muss mindestens über die Image Serving-URL verfügen, die als `serverUrl` -Eigenschaft und das erste Asset als `asset` Parameter. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder im Hauptteil `onload()` -Ereignis.

   Gleichzeitig sollte das Containerelement nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit `display:none` Stil zugewiesen. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Wenn dieses Ereignis eintritt, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. Das Beispiel geht von `interactiveImage` ist die Viewer-Instanz; `s7viewer` ist der Name des Platzhalters `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` ist die Image Serving-URL und `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` ist das Asset:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Video-Bild-Viewer mit einer festen Größe einbettet:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Responsives Design mit uneingeschränkter Höhe**

Mit responsiver Designeinbettung verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers bestimmt `DIV`. Im folgenden Beispiel wird angenommen, dass die Webseite den Container des Viewers zulässt `DIV` , um 40 % der Fenstergröße des Webbrowsers zu übernehmen. Und seine Höhe bleibt unbegrenzt. Der HTML-Code der Webseite würde wie folgt aussehen:

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
1. Container definieren `DIV`.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Container hinzufügen `DIV` zu `"holder"` `DIV`. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

Die folgende Beispielseite zeigt die reale Nutzung responsiver Designs, die mit unbegrenzter Höhe eingebettet werden:

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**Flexible Größe Einbetten mit definierter Breite und Höhe**

Wenn eine Einbettung in flexibler Größe mit definierter Breite und Höhe erfolgt, unterscheidet sich der Webseitenstil. Sie bietet beide Größen für die `"holder"` DIV und zentrieren Sie sie im Browserfenster. Außerdem legt die Webseite die Größe der `HTML` und `BODY` auf 100 Prozent.

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
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Einbetten mit Setter-basierter API**

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit `setContainerId()`, `setParam()`und `setAsset()` API-Methoden mit separaten JavaScript-Aufrufen.

Das folgende Beispiel zeigt die Verwendung der Einbettung mit fester Größe in die setter-basierte API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```
