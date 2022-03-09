---
title: Zoom
description: Zoom-Viewer ist ein Bild-Viewer, der ein Zoombild anzeigt. Dieser Viewer arbeitet mit Bildsets und die Navigation erfolgt mithilfe von Farbfeldern. Es verfügt über Zoom-Tools, Vollbildunterstützung, Farbfelder und eine optionale Schaltfläche zum Schließen. Es wurde für Desktops und Mobilgeräte entwickelt.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2395'
ht-degree: 0%

---

# Zoom{#zoom}

Zoom-Viewer ist ein Bild-Viewer, der ein Zoombild anzeigt. Dieser Viewer arbeitet mit Bildsets und die Navigation erfolgt mithilfe von Farbfeldern. Es verfügt über Zoom-Tools, Vollbildunterstützung, Farbfelder und eine optionale Schaltfläche zum Schließen. Es wurde für Desktops und Mobilgeräte entwickelt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ 502.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Verwenden des Zoom-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der Zoom-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar (ein einzelnes JavaScript-Element mit allen Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Sie können den Zoom-Viewer im Popup-Modus verwenden, indem Sie eine produktionsbereite HTML-Seite verwenden, die mit IS-Viewern bereitgestellt wird, oder im eingebetteten Modus, wo sie mithilfe einer dokumentierten API in die Ziel-Web-Seite integriert wird.

Die Konfiguration und die Skinning-Funktion ähneln denen der anderen Viewer. Alle Skins werden über benutzerdefiniertes CSS erstellt.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem Zoom-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der Zoom-Viewer unterstützt die folgenden Berührungsgesten, die in anderen Apps häufig vorkommen. Wenn der Viewer die Wischgeste des Benutzers nicht verarbeiten kann, leitet er das Ereignis an den Webbrowser weiter, um einen nativen Bildlauf der Seite durchzuführen. Mit dieser Funktion kann der Benutzer durch die Seite navigieren, selbst wenn der Viewer den Großteil des Gerätebildschirms einnimmt.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geste </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Einzeltippen </p> </td> 
   <td colname="col2"> <p> Wählt neue Miniaturansichten in Farbfeldern aus. In der Hauptansicht werden Elemente der Benutzeroberfläche ausgeblendet oder angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doppeltippen </p> </td> 
   <td colname="col2"> <p> Vergrößert eine Ebene, bis die maximale Vergrößerung erreicht ist. Mit der nächsten doppelten Tippen-Geste wird der Viewer auf den anfänglichen Anzeigestatus zurückgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinch </p> </td> 
   <td colname="col2"> <p>Zoomt ein oder aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontales Wischen oder Klick </p> </td> 
   <td colname="col2"> <p> Scrollt durch die Liste der Farbfelder in der Farbfeldleiste. </p> <p> Wenn sich das Bild im Status "Zurücksetzen"befindet und die <span class="codeph"> frametransition </span> auf "Folie"festgelegt ist, wird das Asset mit der Animation der Folie geändert. Für andere <span class="codeph"> frametransition </span> -Modi verwendet, führt die Geste einen nativen Seitenscrollvorgang durch. </p> <p> Wenn das Bild vergrößert wird, wird es horizontal verschoben. Wenn das Bild an den Ansichtsrand verschoben wird und ein Wischen in derselben Richtung erfolgt, führt die Geste einen nativen Seitenscrollen durch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Wischen </p> </td> 
   <td colname="col2"> <p> Wenn das Bild einen Reset-Status aufweist, führt die Geste einen nativen Bildlauf durch. </p> <p> Wenn das Bild vergrößert wird, wird es vertikal verschoben. Wenn das Bild an die Ansichtskante verschoben wird und eine Wischbewegung in die gleiche Richtung erfolgt, führt die Geste einen nativen Seitenbildlauf durch. </p> <p> Wenn die Geste innerhalb des Farbfeldbereichs ausgeführt wird, führt sie einen nativen Bildlauf durch. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt sowohl die Touch-Eingabe als auch die Mauseingabe auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome-, Internet Explorer 11- und Edge-Webbrowser beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Tastaturzugriff und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des Zoom-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, der, wenn ausgewählt, den Viewer in einem separaten Browserfenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt in die Hosting-Seite einzubetten. In letzterem Fall kann die Webseite ein statisches Layout aufweisen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung fester Größe und Einbettung responsiver Designs.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Bereich des Browser-Fensters und passt sich an, falls die Größe des Browsers geändert oder die Geräteausrichtung geändert wird.

Dieser Modus wird am häufigsten für Mobilgeräte verwendet. Die Webseite lädt den Viewer mit `window.open()` JavaScript-Aufruf, ordnungsgemäß konfiguriert `A` HTML-Element oder eine andere geeignete Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Die vordefinierte HTML-Seite heißt `ZoomViewer.html` und sich unter der `html5/` Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung wie im Folgenden gezeigt:

`<s7viewers_root>/html5/ZoomViewer.html`

Wenden Sie benutzerdefiniertes CSS an, um ein benutzerdefiniertes Erscheinungsbild für die Seite zu erhalten.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer im neuen Fenster öffnet:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Über den Einbettungsmodus mit fester Größe und den Einbettungsmodus für responsives Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Web-Seite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien der Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Seiten, auf denen das Layout je nach Gerätetyp automatisch angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Option eignet sich am besten für Webseiten mit statischem Layout.

Responsive Designeinbettungsmodus setzt voraus, dass die Größenanpassung des Viewers während der Laufzeit aufgrund der Größenänderung seines Containers erforderlich ist `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Layout verwendet.

Im Einbettungsmodus für responsives Design verhält sich der Viewer unterschiedlich, je nachdem, wie die Web-Seite den Container dimensioniert `DIV`. Wenn die Webseite nur die Breite des Containers festlegt `DIV`Wenn die Höhe nicht eingeschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Logik stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten einen Abstand aufweisen. Dieser Anwendungsfall ist der häufigste bei Webseiten, die responsive Layout-Frameworks wie Bootstrap und Foundation verwenden.

Wenn die Webseite sowohl die Breite als auch die Höhe für den Container des Viewers festlegt `DIV`, füllt der Viewer diesen Bereich und folgt der Größe, die die Webseite bietet. Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

## Einbettung fester Größe {#section-44f365e6c0dd40709467a459afa82a7f}

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie wie folgt vorgehen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Container-DIV.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL ZoomViewer.js]. Die [!DNL ZoomViewer.js] befindet sich unter der [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf dem die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
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

1. Festlegen der Viewer-Größe

   Dieser Viewer zeigt Miniaturansichten bei der Arbeit mit Sets für mehrere Elemente an. Miniaturansichten auf Desktop-Systemen werden unter der Hauptansicht platziert. Gleichzeitig ermöglicht der Viewer den Austausch des Haupt-Assets zur Laufzeit mithilfe von `setAsset()` API. Als Entwickler haben Sie die Kontrolle darüber, wie der Viewer den Bereich für Miniaturansichten am unteren Rand verwaltet, wenn das neue Asset nur ein Element enthält. Es ist möglich, die Größe des äußeren Viewers intakt zu halten und die Größe der Hauptansicht zu erhöhen und den Bereich der Miniaturansichten zu vergrößern. Alternativ können Sie die Größe der Hauptansicht statisch halten und den äußeren Viewer-Bereich reduzieren, den Webseiteninhalt nach oben verschieben und die freie Bildschirmseite aus den Miniaturansichten verwenden.

   Um die äußeren Viewer-Grenzen beizubehalten, legen Sie die Größe für die `.s7zoomviewer` CSS-Klasse der obersten Ebene in absoluten Einheiten. Die Größe in CSS kann direkt auf der HTML-Seite festgelegt werden. Oder sie kann in eine benutzerdefinierte Viewer-CSS-Datei eingefügt werden, die später in Dynamic Media Classic einem Viewer-Vorgabendatensatz zugewiesen oder explizit mithilfe eines Stilbefehls übergeben wird.

   Siehe [Anpassen des Zoom-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) Weitere Informationen zum Formatieren des Viewers mit CSS.

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen äußeren Viewer-Größe auf der HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Im folgenden Beispiel wird das Verhalten mit einem festen äußeren Viewer angezeigt. Beachten Sie, dass sich die äußere Viewer-Größe beim Wechsel zwischen Sets nicht ändert:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

   Um die Hauptansichtsdimensionen statisch zu machen, definieren Sie die Viewer-Größe in absoluten Einheiten für die innere `Container` SDK-Komponente mit `.s7zoomviewer` `.s7container` CSS-Selektor oder durch Verwendung von `stagesize` -Modifikator.

   Im Folgenden finden Sie ein Beispiel für die Definition der Viewer-Größe für den inneren `Container` SDK-Komponente, damit der Hauptansichtsbereich beim Wechseln des Assets seine Größe nicht ändert:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Die folgende Demoseite zeigt das Viewer-Verhalten mit einer festen Hauptansichtsgröße. Beachten Sie, dass beim Wechseln zwischen Sets die Hauptansicht statisch bleibt und der Webseiteninhalt vertikal verschoben wird.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

   Sie können die `stagesize` -Modifikator im Viewer-Vorgabendatensatz in Dynamic Media Classic. Oder Sie können sie explizit mit dem Viewer-Initialisierungscode mit dem `params` -Sammlung oder als API-Aufruf, wie im Abschnitt Befehlsreferenz dieser Hilfe beschrieben, wie im Folgenden gezeigt:

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz von `s7viewers.ZoomViewer` -Klasse, übergeben Sie alle Konfigurationsinformationen an ihren Konstruktor und rufen Sie `init()` -Methode in einer Viewer-Instanz verwenden.

   Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens `containerId` -Feld, das den Namen der Viewer-Container-ID enthält und verschachtelt ist `params` JSON-Objekt mit Konfigurationsparametern, die vom Viewer unterstützt werden. In diesem Fall wird die `params` -Objekt muss mindestens über die Image Serving-URL verfügen, die als `serverUrl` -Eigenschaft und das erste Asset als `asset` Parameter. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder im Hauptteil `onload()` -Ereignis.

   Gleichzeitig sollte das Containerelement nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit `display:none` Stil zugewiesen. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Wenn diese Aktion auftritt, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. Dieses Beispiel geht von `zoomViewer` die Viewer-Instanz ist, `s7viewer` der Name des PlatzhalterDIV ist, `http://s7d1.scene7.com/is/image/` ist die Image Serving-URL und `Scene7SharedAssets/ImageSet-Views-Sample` ist das Asset.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Video-Viewer mit einer festen Größe einbettet:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Responsives Design mit uneingeschränkter Höhe {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

Mit responsiver Designeinbettung verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers bestimmt `DIV`. Im folgenden Beispiel wird angenommen, dass die Webseite den Container des Viewers zulässt `DIV` , um 40 % der Fenstergröße des Webbrowsers zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite würde wie folgt aussehen:

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

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Fügen Sie dem vorhandenen Container-DIV hinzu. `"holder"` DIV. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

Die folgende Beispielseite zeigt die reale Nutzung responsiver Designs, die mit unbegrenzter Höhe eingebettet werden:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Flexible Einbettung von Größe mit definierter Breite und Höhe {#section-3674e6c032594441a6576b7fb1de6e64}

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

Die übrigen Schritte zum Einbetten sind mit den Schritten für responsives Design identisch, das mit uneingeschränkter Höhe eingebettet wird. Das folgende Beispiel zeigt:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

## Einbetten mit einer setter-basierten API {#section-44e014925f24418b900696003855c0a9}

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit `setContainerId()`, `setParam()`und `setAsset()` API-Methoden mit separaten JavaScript-Aufrufen.

Das folgende Beispiel zeigt die Verwendung der Einbettung fester Größe in eine setter-basierte API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
