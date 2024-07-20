---
title: Interaktives Bild
description: Der Viewer für interaktive Bilder ist ein Viewer, der ein einzelnes, nicht zoombares Bild mit klickbaren Hotspots anzeigt. Der Zweck dieses Viewers ist die Implementierung eines Erlebnisses mit Shopping-Funktion. Das heißt, der Benutzer kann einen Hotspot über dem Bannerbild auswählen und zu einer Schnellansichts- oder Produktdetailseite auf Ihrer Website weitergeleitet werden. Es wurde für Desktops und Mobilgeräte entwickelt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1703'
ht-degree: 0%

---

# Interaktives Bild{#interactive-image}

Der Viewer für interaktive Bilder ist ein Viewer, der ein einzelnes, nicht zoombares Bild mit klickbaren Hotspots anzeigt. Der Zweck dieses Viewers ist die Implementierung eines Erlebnisses mit Shopping-Funktion. Das heißt, der Benutzer kann einen Hotspot über dem Bannerbild auswählen und zu einer Schnellansichts- oder Produktdetailseite auf Ihrer Website weitergeleitet werden. Es wurde für Desktops und Mobilgeräte entwickelt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Der Viewer-Typ ist 508.

## Demo-URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## Systemanforderungen {#section-b7270cc4290043399681dc504f043609}

Siehe [Systemanforderungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Interaktiver Bild-Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Der Viewer für interaktive Bilder stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar (eine JavaScript-Datei enthält alle Viewer-SDK-Komponenten, die von diesem Viewer, Assets und CSS verwendet werden), die vom Viewer zur Laufzeit heruntergeladen werden.

Der interaktive Bild-Viewer kann nur im eingebetteten Modus verwendet werden, wo er mithilfe der dokumentierten API in die Ziel-Web-Seite integriert wird.

Die Konfiguration und das Skinning ähneln denen der anderen in dieser Hilfe beschriebenen Viewer. Die gesamte Skinning-Funktion wird über benutzerdefiniertes CSS erreicht.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem interaktiven Bild-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Die vom Video Image Viewer unterstützte Interaktion ist die Aktivierung von Hotspots auf Desktop-Systemen. Diese Aktivierung erfolgt bei Klick- und Touch-Geräten mit einem einzigen Tippen.

Der Viewer ist vollständig über die Tastatur zugänglich.

Siehe [Barrierefreiheit und Navigation auf der Tastatur](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des interaktiven Bild-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Der interaktive Bild-Viewer ist in die Hosting-Seite eingebettet. Eine solche Webseite kann ein statisches Layout aufweisen oder &quot;responsiv&quot;sein und auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt werden.

Um diese Anforderungen zu erfüllen, unterstützt der Viewer zwei Hauptbetriebsmodi: Einbettung in feste Größe und responsive Einbettung.

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

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL InterativeImage.js] einbeziehen. Die Datei [!DNL InteractiveImage.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf dem die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
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

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für die CSS-Klasse der obersten Ebene in absoluten Einheiten deklarieren oder den Modifikator `stagesize` verwenden.`.s7interactiveimage`

   Sie können die Größenanpassung in CSS direkt auf die HTML-Seite setzen. Oder Sie können die Größe in eine benutzerdefinierte Viewer-CSS-Datei einfügen, die später in Adobe Experience Manager Assets einem Viewer-Vorgabendatensatz zugewiesen - On-Demand oder explizit mit dem Befehl `style` übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Video](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf der HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Sie können den Modifikator `stagesize` explizit mit dem Viewer-Initialisierungscode mit der Sammlung `params` oder als API-Aufruf übergeben, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben:

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.InteractiveImage`, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode `init()` in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID und das verschachtelte JSON-Objekt `params` mit Konfigurationsparametern enthält, die vom Viewer unterstützt werden. In diesem Fall muss für das Objekt `params` mindestens die Image Serving-URL als `serverUrl`-Eigenschaft und das anfängliche Asset als `asset`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder das body `onload()` -Ereignis auf.

   Gleichzeitig sollte das Containerelement nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit dem ihm zugewiesenen `display:none` -Stil ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Wenn dieses Ereignis eintritt, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. Im Beispiel wird angenommen, dass `interactiveImage` die Viewer-Instanz ist; `s7viewer` der Name des Platzhalters `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` die Image Serving-URL und `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` das Asset ist:

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

**Responsives Design, eingebettet in unbeschränkte Höhe**

Bei der Einbettung responsiver Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers `DIV` vorgibt. Für das folgende Beispiel nehmen Sie an, dass die Webseite es dem Container `DIV` des Viewers ermöglicht, 40 % der Fenstergröße des Webbrowsers zu übernehmen. Und seine Höhe bleibt unbegrenzt. Der HTML-Code der Webseite würde wie folgt aussehen:

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
1. Definieren des Containers `DIV`.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Fügen Sie den Container `DIV` der vorhandenen `"holder"` `DIV` hinzu. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

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

Wenn eine Einbettung in flexibler Größe mit definierter Breite und Höhe erfolgt, unterscheidet sich der Webseitenstil. Es bietet beide Größen für den DIV `"holder"` und zentriert ihn im Browserfenster. Außerdem setzt die Webseite die Größe der Elemente `HTML` und `BODY` auf 100 Prozent.

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

**Einbetten mit setFilter-basierter API**

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` mit separaten JavaScript-Aufrufen angegeben.

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
