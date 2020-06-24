---
description: Der Flyout-Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version angezeigt, die in der Flyout-Ansicht angezeigt wird, die ein Benutzer aktiviert. Dieser Viewer funktioniert mit Bildsätzen, und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.
keywords: responsive
seo-description: Der Flyout-Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version angezeigt, die in der Flyout-Ansicht angezeigt wird, die ein Benutzer aktiviert. Dieser Viewer funktioniert mit Bildsätzen, und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.
seo-title: Flyout
solution: Experience Manager
title: Flyout
topic: Dynamic media
uuid: 588e1baa-4165-4aec-8fbe-1a916c0f409f
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---


# Flyout{#flyout}

Der Flyout-Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version angezeigt, die in der Flyout-Ansicht angezeigt wird, die ein Benutzer aktiviert. Dieser Viewer funktioniert mit Bildsätzen, und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Der Viewer-Typ ist 504.

Siehe [Systemanforderungen und -voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Verwenden des Flyout-Viewers {#section-f21ac23d3f6449ad9765588d69584772}

Der Flyout-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar (ein einzelnes JavaScript enthält alle Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden

Der Flyout-Viewer ist nur für die integrierte Verwendung vorgesehen, d. h. er wird mithilfe der dokumentierten API in die Webseite integriert. Für den Flyout-Viewer ist keine produktionsfertige Webseite verfügbar.

Konfigurationen und Skins ähneln denen anderer Viewer. Sie können benutzerdefinierte CSS verwenden, um Skins anzuwenden.

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem Flyout-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Der Flyout-Viewer unterstützt Single-Touch- und Multi-Touch-Gesten, die in anderen Mobilanwendungen häufig vorkommen.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geste </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Einzelner Tipp </p> </td> 
   <td colname="col2"> <p> Aktiviert die Flyout-Ansicht oder Änderungen zwischen dem primären und dem sekundären Zoomgrad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontale Blättergeste oder Flick </p> </td> 
   <td colname="col2"> <p> Blättert durch die Liste der Farbfelder in der Farbfeldleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikale Blättergeste </p> </td> 
   <td colname="col2"> <p>Wenn die Geste innerhalb des Farbfeldbereichs erfolgt, führt sie einen nativen Seitenbildlauf durch. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt auch die Eingabe per Touch- und Mausklick auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Barrierefreiheit und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)über die Tastatur.

## Einbetten des Flyout-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Die Webseite kann über ein statisches Seitenlayout verfügen oder ein reaktionsfähiges Design verwenden, das auf verschiedenen Geräten oder für unterschiedliche Browserfenster-Größen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer zwei primäre Betriebsmodi: Einbettung in fester Größe und Einbettung in reaktionsfähiges Design.

Der Einbettungsmodus für feste Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Option eignet sich am besten für Webseiten mit einem statischen Seitenlayout.

Der responsive Design-Einbettungsmodus setzt voraus, dass die Größe des Viewers während der Laufzeit je nach Größenänderung des Containers ggf. angepasst werden muss `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Wenn Sie den Einbettungsmodus für reaktionsfähige Designs mit dem Flyout-Viewer verwenden, stellen Sie sicher, dass Sie explizite Haltepunkte für das Hauptbild der Ansicht mit dem `imagereload` Parameter angeben. Im Idealfall sollten Sie Ihre Haltepunkte mit den vom CSS der Webseite diktierten BreitenHaltepunkten des Viewers abgleichen.

Im Einbettungsmodus für reaktionsfähiges Design verhält sich der Viewer je nach Größe des Containers einer Webseite unterschiedlich `DIV`. Wenn die Webseite nur die Breite des Containers festlegt `DIV`und dabei die Höhe unbegrenzt bleibt, wählt der Viewer die Höhe automatisch entsprechend dem Seitenverhältnis des verwendeten Assets aus. Das bedeutet, dass der Vermögenswert perfekt in die Ansicht passt, ohne dass eine seitliche Auffüllung erforderlich ist. Dieser spezielle Anwendungsfall ist der häufigste Fall für Webseiten, die reaktionsfähige Layout-Frameworks wie Bootstrap, Foundation usw. verwenden.

Andernfalls füllt der Viewer, wenn die Webseite sowohl die Breite als auch die Höhe des Containers des Viewers festlegt, nur diesen Bereich `DIV`und folgt der vom Webseitenlayout bereitgestellten Größe. Ein gutes Verwendungsfallbeispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung der Größe des Webbrowser-Fensters entspricht.

**Einbettung fester Größe**

Der Viewer wird wie folgt zu einer Webseite hinzugefügt:

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Containers `DIV`.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite

   Zum Erstellen eines Viewers müssen Sie im HTML-Kopf ein Skript-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie `FlyoutViewer.js`dies berücksichtigen. `FlyoutViewer.js` befindet sich im folgenden [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Scene7-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Scene7-Server an, auf denen die IS-Viewer installiert sind.

Ein relativer Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Sie sollten nur auf die JavaScript- `include` Hauptdatei des Viewers auf Ihrer Seite verweisen. Sie sollten keine weiteren JavaScript-Dateien im Webseitencode referenzieren, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die vom Viewer aus dem `Utils.js` Kontextpfad (so genanntes konsolidiertes SDK) geladene HTML5 SDK- `/s7viewers` Bibliothek `include`. Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig durch die Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Ältere Versionen des sekundären Viewers werden von Adobe nicht `includes` auf dem Server gespeichert.
>
>
>Infolgedessen wird die Viewer-Funktion bei der Bereitstellung einer neuen Produktversion durch direkte Verweise auf sekundäres JavaScript, das vom Viewer auf der Seite `include` verwendet wird, in Zukunft unterbrochen.

1. Definieren des Container-DIV.

   Hinzufügen ein leeres DIV-Element auf die Seite, auf der der Viewer angezeigt werden soll. Die ID des DIV-Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute`eingestellt.

   Es liegt in der Verantwortung der Webseite, das geeignete Element `z-index` für das Platzhalter-DIV-Element anzugeben. Dadurch wird sichergestellt, dass der Flyout-Bereich des Viewers über den anderen Webseitenelementen angezeigt wird.

   Das folgende Beispiel zeigt ein definiertes Platzhalter-DIV-Element:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Einstellen der Viewer-Größe.

   In diesem Viewer werden Miniaturansichten angezeigt, wenn Sie mit Sets mit mehreren Elementen arbeiten. Auf Desktop-Systemen werden Miniaturansichten unterhalb der Hauptversion der Ansicht platziert. Gleichzeitig ermöglicht der Viewer den Austausch des Hauptassets während der Laufzeit mithilfe der `setAsset()` API. Als Entwickler haben Sie die Kontrolle darüber, wie der Viewer den Bereich &quot;Miniaturansichten&quot;im unteren Bereich verwaltet, wenn das neue Asset nur ein Element enthält. Es ist möglich, die Größe des äußeren Viewers beizubehalten und die Haupthöhe der Ansicht zu erhöhen und den Bereich der Miniaturansichten zu belassen. Oder Sie können die Größe der Hauptseite statisch beibehalten und den äußeren Viewer-Bereich reduzieren, damit der Inhalt der Ansicht nach oben verschoben werden kann, und dann die freie Seitenposition verwenden, die von den Miniaturbildern übrig bleibt.

   Um die äußeren Viewer-Grenzen intakt zu halten, definieren Sie die Größe der CSS-Klasse der `.s7flyoutviewer` obersten Ebene in absoluten Einheiten. Die Größe in CSS kann auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei korrigiert werden, die später im Scene7 Publishing System einem Viewer-Vorgabendatensatz zugewiesen oder explizit mit dem Stilbefehl übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Flyout-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) .

   Das folgende Beispiel zeigt die Definition der statischen äußeren Viewer-Größe in einer HTML-Seite:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können das Verhalten mit einem festen äußeren Viewer-Bereich auf der folgenden Beispielseite sehen. Beachten Sie, dass sich die Größe des äußeren Viewers beim Wechseln zwischen den Sets nicht ändert:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   Um die Hauptdimensionen der Ansicht statisch zu machen, definieren Sie die Viewer-Größe in absoluten Maßeinheiten für die innere SDK- mithilfe des `Container` `.s7flyoutviewer .s7container` CSS-Selektors. Darüber hinaus sollten Sie die für die CSS-Klasse der `.s7flyoutviewer` obersten Ebene definierte feste Größe im Standard-Viewer-CSS außer Kraft setzen, indem Sie sie auf `auto`.

   Im Folgenden sehen Sie ein Beispiel für die Definition der Viewer-Größe für die innere `Container` SDK-Komponente, sodass der Hauptbereich Ansicht beim Wechseln des Assets seine Größe nicht ändert:

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Die folgende Beispielseite zeigt das Viewer-Verhalten mit einer festen Größe für die Haupt-Ansicht. Beachten Sie, dass beim Wechseln zwischen Sets die Hauptinhalt-Ansicht statisch bleibt und der Webseiteninhalt vertikal verschoben wird:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   Beachten Sie außerdem, dass das Standard-Viewer-CSS eine feste Größe für den Außenbereich bereitstellt.

1. Erstellen und Initialisieren des Viewers

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der `s7viewers.FlyoutViewer` Klasse, geben Sie alle Konfigurationsinformationen an den Konstruktor weiter und rufen Sie `init()` die Methode für eine Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das `containerId` Feld verfügen, das den Namen der Viewer-Container-ID und das verschachtelte `params` JSON-Objekt mit den vom Viewer unterstützten Konfigurationsparametern enthält. In diesem Fall muss für das `params` Objekt mindestens die Image Serving-URL als `serverUrl` -Eigenschaft und das ursprüngliche Asset als `asset` -Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und Beginn erstellen.

   Es ist wichtig, dass der Viewer-Container dem DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser zögern die Erstellung von DOM bis zum Ende der Webseite. Um eine maximale Kompatibilität zu gewährleisten, rufen Sie die `init()` Methode direkt vor dem schließenden `BODY` Tag oder im Body- `onload()` Ereignis auf.

   Gleichzeitig sollte das Container-Element nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mithilfe des ihr zugewiesenen `display:none` Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel zum Erstellen einer Viewer-Instanz, bei der die notwendigen Mindestkonfigurationsoptionen an den Konstruktor übergeben und die `init()` Methode aufgerufen werden. Im Beispiel wird davon ausgegangen, dass `flyoutViewer` es sich um die Viewer-Instanz handelt. `s7viewer` der Name des Platzhalters `DIV`; `http://s7d1.scene7.com/is/image/` die Image Serving-URL; und `Scene7SharedAssets/ImageSet-Views-Sample` ist das Asset:

   ```
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, die den Flyout Viewer mit einer festen Größe einbettet:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
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

## Responsive Design-Einbettung mit unbeschränkter Höhe {#section-056cb574713c4d07be6d07cf3c598839}

Bei der Integration reaktionsfähiger Designs verfügt die Webseite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers vorgibt `DIV`. Im folgenden Beispiel nehmen Sie an, dass die Webseite dem Container des Viewers erlaubt, 40 % der Fenstergröße des Webbrowsers zu verbrauchen, wobei die Höhe unbegrenzt bleibt. `DIV` Der HTML-Code der Webseite würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten zum Einbetten in feste Größe. Der einzige Unterschied besteht darin, dass Sie die feste Größe vom Standard-Viewer-CSS mit der in relativen Einheiten festgelegten Größe überschreiben müssen.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Containers `DIV`.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers

Alle oben genannten Schritte sind mit den folgenden drei Ausnahmen identisch:

* den Container `DIV` dem bestehenden &quot;Inhaber&quot; hinzufügen `DIV`;
* Parameter mit expliziten Haltepunkten hinzugefügt `imagereload` werden;
* anstatt eine feste Viewer-Größe mit absoluten Einheiten festzulegen, verwenden Sie CSS, das die Breite und Höhe des Viewers wie folgt auf 100 % setzt:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Die folgende Beispielseite zeigt die aktuelleren Einsatzmöglichkeiten von reaktionsfähigem Design-Einbettung mit uneingeschränkter Höhe:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Einbettung flexibler Größe mit definierter Breite und Höhe {#section-0a329016f9414d199039776645c693de}

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

Die übrigen Einbettungsschritte sind identisch mit den Schritten, die für die Einbettung von reaktionsfähigem Design mit uneingeschränkter Höhe verwendet werden. Das resultierende Beispiel lautet:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Einbetten mithilfe der Setter-basierten API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Anstatt JSON-basierte Initialisierung zu verwenden, ist es möglich, set-basierte API- und no-args-Konstruktoren zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit `setContainerId()`-, `setParam()`- und `setAsset()` -API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Im folgenden Beispiel wird die Einbettung in feste Größe mit setter-basierter API veranschaulicht:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```

