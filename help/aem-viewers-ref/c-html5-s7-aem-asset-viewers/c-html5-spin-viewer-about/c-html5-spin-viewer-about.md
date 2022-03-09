---
title: Spin
description: Rotationsset-Viewer ist ein Bild-Viewer, der eine 360-Grad-Ansicht des Bildes oder sogar eine mehrdimensionale Ansicht bietet, wenn ein entsprechendes Rotationsset verwendet wird. Es verfügt über Zoom- und Rotationstools, Vollbildunterstützung und eine optionale Schließen-Schaltfläche. Es wurde für Desktops und Mobilgeräte entwickelt.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---

# Rotation{#spin}

Rotationsset-Viewer ist ein Bild-Viewer, der eine 360-Grad-Ansicht des Bildes oder sogar eine mehrdimensionale Ansicht bietet, wenn ein entsprechendes Rotationsset verwendet wird. Es verfügt über Zoom- und Rotationstools, Vollbildunterstützung und eine optionale Schließen-Schaltfläche. Es wurde für Desktops und Mobilgeräte entwickelt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ 503.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## Verwenden des Rotationsset-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der Rotationsset-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar (ein einzelnes JavaScript-Include mit allen Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Der Rotationsset-Viewer kann sowohl im Popup-Modus mit einer produktionsbereiten HTML-Seite verwendet werden, die mit IS-Viewern bereitgestellt wird, als auch im eingebetteten Modus, wo er mithilfe einer dokumentierten API in die Ziel-Web-Seite integriert wird.

Die Konfiguration und die Skinning-Funktion ähneln denen der anderen Viewer. Alle Skins können über benutzerdefinierte CSS erstellt werden.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem Rotationsset-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der Rotationsset-Viewer unterstützt die folgenden Berührungsgesten, die in anderen Mobile Apps häufig vorkommen. Wenn der Viewer die Wischgeste eines Benutzers nicht verarbeiten kann, leitet er das Ereignis an den Webbrowser weiter, um einen nativen Seitenbildlauf durchzuführen. Mit dieser Funktion kann der Benutzer durch die Seite navigieren, selbst wenn der Viewer den größten Teil des Gerätebildschirms einnimmt.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geste </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Doppeltippen </p> </td> 
   <td colname="col2"> <p> Vergrößert eine Ebene, bis die maximale Vergrößerung erreicht ist. Mit der nächsten doppelten Tippen-Geste wird der Viewer auf den anfänglichen Anzeigestatus zurückgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinch </p> </td> 
   <td colname="col2"> <p>Vergrößert oder verkleinert das Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontales Wischen oder Klick </p> </td> 
   <td colname="col2"> <p> Wenn das Bild einen Reset-Status aufweist, wird es horizontal durch das Set gedreht. </p> <p> Wenn das Bild vergrößert wird, wird es horizontal verschoben. Wenn das Bild an die Ansichtskante verschoben wird und weiterhin in diese Richtung gewischt wird, führt die Geste einen nativen Bildlauf durch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Wischen oder Klick </p> </td> 
   <td colname="col2"> <p> Wenn sich das Bild in einem Zurücksetzungsstatus befindet, ändert es den vertikalen Blickwinkel, falls ein mehrdimensionales Rotationsset verwendet wird. In einem eindimensionalen Rotationsset führt die Geste einen nativen Seitenbildlauf durch. Oder wenn sich ein mehrdimensionales Rotationsset auf der letzten oder ersten Achse befindet, sodass das vertikale Wischen nicht zu einer Änderung des vertikalen Blickwinkels führt, führt die Geste auch einen nativen Seitenbildlauf durch. </p> <p> Wenn das Bild vergrößert wird, wird es vertikal verschoben. Wenn das Bild an die Ansichtskante verschoben wird und weiterhin in diese Richtung gewischt wird, führt die Geste einen nativen Bildlauf durch. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Viewer unterstützt auch Touch-Eingabe- und Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome-, Internet Explorer 11- und Edge-Webbrowser beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Tastaturzugriff und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des Rotationsset-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, der, wenn ausgewählt, den Viewer in einem separaten Browserfenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt in die Hosting-Seite einzubetten. In letzterem Fall kann die Webseite ein statisches Seitenlayout aufweisen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung fester Größe und Einbettung responsiver Designs.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Bereich des Browser-Fensters und passt sich an, falls die Größe des Browsers geändert wird oder die Ausrichtung eines Mobilgeräts geändert wird.

Der Pop-up-Modus ist der häufigste für Mobilgeräte. Die Webseite lädt den Viewer mit `window.open()` JavaScript-Aufruf, ordnungsgemäß konfiguriert `A` HTML-Element oder eine andere geeignete Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. In diesem Fall wird sie [!DNL SpinViewer.html] und sich innerhalb der [!DNL html5/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erreichen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**Über den Einbettungsmodus mit fester Größe und den Einbettungsmodus für responsives Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Design-Seiten, auf denen das Layout automatisch an den Gerätetyp angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Aktion eignet sich am besten für Webseiten mit statischem Layout.

Responsives Design-Einbetten setzt voraus, dass die Größe des Viewers zur Laufzeit geändert werden muss, wenn die Größe des Containers geändert wird `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für responsives Design verhält sich der Viewer unterschiedlich, je nachdem, wie die Web-Seite den Container dimensioniert `DIV`. Wenn die Webseite nur die Breite des Containers festlegt `DIV`Wenn die Höhe nicht eingeschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten einen Abstand aufweisen. Dieser Anwendungsfall ist am häufigsten für Webseiten mit responsiven Design-Layout-Frameworks wie Bootstrap oder Foundation.

Andernfalls, wenn die Webseite sowohl die Breite als auch die Höhe für den Container des Viewers festlegt `DIV`, füllt der Viewer nur diesen Bereich und folgt der Größe, die das Layout der Webseite bietet. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

**Einbettung fester Größe**

Sie können den Rotationsset-Viewer wie folgt zu einer Web-Seite hinzufügen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Container definieren `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie `SpinViewer.js`. `SpinViewer.js` befindet sich unter der [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media-Server an, auf dem die IS-Viewer installiert sind.

   Der relative Pfad sieht wie folgt aus:

   ```html {.line-numbers}
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Nur auf das JavaScript des Haupt-Viewers verweisen `include` -Datei auf Ihrer Seite. Referenzieren Sie keine zusätzlichen JavaScript-Dateien im Webseitencode, die möglicherweise von der Viewer-Logik zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf das HTML5 SDK. `Utils.js` Bibliothek, die vom Viewer aus geladen wird `/s7viewers` Kontextpfad (so genanntes konsolidiertes SDK) `include`). Der Grund dafür ist, dass der Standort `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig von der Logik des Viewers verwaltet und der Speicherort zwischen Viewer-Versionen geändert wird. Adobe behält ältere Versionen des sekundären Viewers nicht bei `includes` auf dem Server.
   >
   >
   >Daher können Sie einen direkten Verweis auf sekundäres JavaScript einfügen `include` wird vom Viewer auf der Seite verwendet und unterbricht die Viewer-Funktionalität in Zukunft, wenn eine neue Produktversion bereitgestellt wird.

1. Definieren des Container-DIV.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres DIV-Element hinzu. Die ID des DIV-Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. das `position` Die CSS-Eigenschaft ist auf `relative` oder `absolute`.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-DIV-Element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für `.s7spinviewer` CSS-Klasse der obersten Ebene in absoluten Einheiten oder durch Verwendung von `stagesize` -Modifikator.

   Sie können die Größe in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festlegen. Sie wird später einem Viewer-Vorgabendatensatz in Dynamic Media Classic zugewiesen oder explizit mithilfe eines Stilbefehls übergeben.

   Siehe [Anpassen des Rotationsset-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) Weitere Informationen zum Formatieren des Viewers mit CSS.

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf der HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können die `stagesize` -Modifikator entweder im Viewer-Vorgabendatensatz in Dynamic Media Classic. Oder Sie können sie explizit mit dem Viewer-Initialisierungscode mit `params` -Sammlung oder als API-Aufruf, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben, wie folgt:

   ```html {.line-numbers}
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz von `s7viewers.SpinViewer` -Klasse, übergeben Sie alle Konfigurationsinformationen an ihren Konstruktor und rufen Sie `init()` -Methode in einer Viewer-Instanz verwenden. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt hat mindestens `containerId` -Feld, das den Namen der Viewer-Container-ID und verschachtelt enthält `params` JSON-Objekt mit Konfigurationsparametern, die vom Viewer unterstützt werden. In diesem Fall `params` -Objekt, muss mindestens die Image Serving-URL als `serverUrl` Eigenschaft und anfängliches Asset als `asset` Parameter. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder im Hauptteil `onload()` -Ereignis.

   Gleichzeitig sollte das Container-Element nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit dem `display:none` Stil zugewiesen. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Wenn diese Aktion auftritt, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. Das Beispiel geht von `spinViewer` die Viewer-Instanz ist, `s7viewer` ist der Name des Platzhalters `DIV`, [!DNL http://s7d1.scene7.com/is/image/] ist die Image Serving-URL und [!DNL Scene7SharedAssets/SpinSet_Sample] ist das Asset.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Rotationsset-Viewer mit einer festen Größe einbettet:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsives Design mit uneingeschränkter Höhe**

Mit responsiver Designeinbettung verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers bestimmt `DIV`. Für die Zwecke dieses Beispiels nehmen Sie an, dass die Webseite den Container des Viewers zulässt `DIV` , um 40 % der Fenstergröße des Webbrowsers zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der resultierende HTML-Code der Webseite sieht wie folgt aus:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt der Einbettung in feste Größe, wobei der einzige Unterschied darin besteht, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Container hinzufügen `DIV` an den bestehenden &quot;Inhaber&quot; `DIV`. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Die folgende Beispielseite zeigt reale Anwendungsfälle responsiven Designs, die mit unbegrenzter Höhe eingebettet werden:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demostandort](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Flexible Größeneinbettung mit definierter Breite und Höhe**

Wenn eine Einbettung in flexibler Größe mit definierter Breite und Höhe erfolgt, unterscheidet sich der Webseitenstil. Das heißt, es stellt dem Inhaber beide Größen zur Verfügung. `DIV` und zentriert sie im Browserfenster. Außerdem legt die Webseite die Größe der `HTML` und `BODY` -Element auf 100 %:

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

Die restlichen Einbettungsschritte sind mit dem responsiven Design identisch, das mit uneingeschränkter Höhe eingebettet wird. Das folgende Beispiel zeigt:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Einbetten mit der Setter-basierten API**

Statt die JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Mit diesem API-Konstruktor nehmen keine Parameter auf und Konfigurationsparameter werden mit `setContainerId()`, `setParam()`und `setAsset()` API-Methoden mit separaten JavaScript-Aufrufen.

Das folgende Beispiel zeigt die Einbettung von fester Größe in eine setter-basierte API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
