---
title: Flyout
description: Flyout-Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version angezeigt, die in der Flyout-Ansicht angezeigt wird, die ein Benutzer aktiviert. Dieser Viewer arbeitet mit Bildsets und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für Desktops und Mobilgeräte entwickelt.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '2065'
ht-degree: 0%

---

# Flyout{#flyout}

Flyout-Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version angezeigt, die in der Flyout-Ansicht angezeigt wird, die ein Benutzer aktiviert. Dieser Viewer arbeitet mit Bildsets und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für Desktops und Mobilgeräte entwickelt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Der Viewer-Typ ist 504.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Verwenden des Flyout-Viewers {#section-f21ac23d3f6449ad9765588d69584772}

Der Flyout-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar (ein einzelnes JavaScript-Include mit allen Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden

Der Flyout-Viewer ist nur für die integrierte Verwendung vorgesehen. Das bedeutet, dass er mithilfe einer dokumentierten API in die Webseite integriert wird. Für den Flyout-Viewer ist keine produktionsbereite Webseite verfügbar.

Die Konfiguration und die Skinning-Funktion ähneln denen der anderen Viewer. Sie können benutzerdefiniertes CSS verwenden, um Skinning anzuwenden.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem Flyout-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Flyout-Viewer unterstützt Einzelkontakt- und Multi-Touch-Gesten, die in anderen Mobile Apps häufig vorkommen.

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
   <td colname="col2"> <p> Aktiviert die Flyout-Ansicht oder Änderungen zwischen dem primären und dem sekundären Zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontales Wischen oder Klick </p> </td> 
   <td colname="col2"> <p> Scrollt durch die Liste der Farbfelder in der Farbfeldleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Wischen </p> </td> 
   <td colname="col2"> <p>Wenn die Geste innerhalb des Farbfeldbereichs ausgeführt wird, führt sie einen nativen Bildlauf durch. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt auch Touch-Eingabe- und Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome-, Internet Explorer 11- und Edge-Webbrowser beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Tastaturzugriff und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des Flyout-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Die Webseite kann ein statisches Seitenlayout aufweisen oder ein responsives Design verwenden, das auf verschiedenen Geräten unterschiedlich angezeigt wird, oder für verschiedene Browserfenstergrößen. Um diese Anforderungen zu erfüllen, unterstützt der Viewer zwei primäre Betriebsmodi: Einbetten in feste Größe und Einbetten in responsives Design.

Der Einbettungsmodus für feste Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Auswahl eignet sich am besten für Webseiten mit statischem Seitenlayout.

Responsives Design-Einbettungsmodus setzt voraus, dass die Größe des Viewers während der Laufzeit entsprechend der Größenänderung seines Containers geändert werden muss `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Stellen Sie bei Verwendung des Einbettungsmodus für responsives Design mit dem Flyout-Viewer sicher, dass Sie explizite Haltepunkte für das Hauptansichtsbild mit der `imagereload` Parameter. Idealerweise sollten Sie Ihre Haltepunkte mit den Viewer-Breitenhaltepunkten abgleichen, wie von der Web-Seiten-CSS vorgeschrieben.

Im Einbettungsmodus für responsives Design verhält sich der Viewer je nach Art des Webseitenbehälters unterschiedlich `DIV` ist größer. Wenn die Webseite nur die Breite des Containers festlegt `DIV`, wobei die Höhe unbegrenzt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion bedeutet, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten aufgefüllt werden. Dieser Anwendungsfall ist der häufigste bei Webseiten, die responsive Design-Layout-Frameworks wie Bootstrap und Foundation verwenden.

Andernfalls, wenn die Webseite sowohl die Breite als auch die Höhe für den Container des Viewers festlegt `DIV`, füllt der Viewer nur diesen Bereich aus und folgt der Größe, die durch das Web-Seitenlayout angegeben wird. Ein gutes Anwendungsbeispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

**Einbettung fester Größe**

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie wie folgt vorgehen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Container definieren `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie `FlyoutViewer.js`. `FlyoutViewer.js` im Folgenden [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media-Server an, auf dem die IS-Viewer installiert sind.

Ein relativer Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
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

   Es liegt in der Verantwortung der Webseite, die richtige `z-index` für das Platzhalter-DIV-Element. Dadurch wird sichergestellt, dass der Flyout-Teil des Viewers über den anderen Webseitenelementen angezeigt wird.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-DIV-Element:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Festlegen der Viewer-Größe

   Dieser Viewer zeigt Miniaturansichten bei der Arbeit mit Sets für mehrere Elemente an. Auf Desktop-Systemen werden Miniaturansichten unter der Hauptansicht platziert. Gleichzeitig ermöglicht der Viewer den Austausch des Haupt-Assets während der Laufzeit mithilfe von `setAsset()` API. Als Entwickler haben Sie die Kontrolle darüber, wie der Viewer den Bereich für Miniaturansichten im unteren Bereich verwaltet, wenn das neue Asset nur ein Element enthält. Es ist möglich, die Größe des äußeren Viewers intakt zu halten und die Größe der Hauptansicht zu erhöhen und den Bereich der Miniaturansichten zu belassen. Alternativ können Sie die Größe der Hauptansicht statisch halten und den äußeren Viewer-Bereich reduzieren, den Webseiteninhalt nach oben verschieben und dann die freie Seitenposition links von den Miniaturansichten verwenden.

   Definieren Sie die Größe für `.s7flyoutviewer` CSS-Klasse der obersten Ebene in absoluten Einheiten. Die Größe in CSS kann direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festgelegt, später einem Viewer-Vorgabendatensatz in Dynamic Media Classic zugewiesen oder explizit mithilfe des Stilbefehls übergeben werden.

   Siehe [Anpassen des Flyout-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) Weitere Informationen zum Formatieren des Viewers mit CSS.

   Im Folgenden finden Sie ein Beispiel für die Definition der statischen äußeren Viewer-Größe auf einer HTML-Seite:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können das Verhalten mit einem festen äußeren Viewer-Bereich auf der folgenden Beispielseite sehen. Beachten Sie, dass sich die äußere Viewer-Größe beim Wechsel zwischen Sets nicht ändert:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   Um die Hauptansichtsdimensionen statisch zu machen, definieren Sie die Viewer-Größe in absoluten Einheiten für die innere `Container` SDK-Komponente mit `.s7flyoutviewer .s7container` CSS-Selektor. Darüber hinaus sollten Sie die für die Variable `.s7flyoutviewer` CSS-Klasse der obersten Ebene im Standard-Viewer-CSS, indem sie `auto`.

   Im Folgenden finden Sie ein Beispiel für die Definition der Viewer-Größe für den inneren `Container` SDK-Komponente, damit der Hauptansichtsbereich beim Wechseln des Assets seine Größe nicht ändert:

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

   Die folgende Beispielseite zeigt das Viewer-Verhalten mit einer festen Hauptansichtsgröße. Beachten Sie, dass beim Wechseln zwischen Sets die Hauptansicht statisch bleibt und der Webseiteninhalt vertikal verschoben wird:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   Darüber hinaus bietet die standardmäßige Viewer-CSS eine feste Größe für den äußeren Bereich.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz von `s7viewers.FlyoutViewer` -Klasse, übergeben Sie alle Konfigurationsinformationen an ihren Konstruktor und rufen Sie `init()` -Methode in einer Viewer-Instanz verwenden. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens die `containerId` -Feld, das den Namen der Viewer-Container-ID und verschachtelt enthält `params` JSON-Objekt mit Konfigurationsparametern, die vom Viewer unterstützt werden. In diesem Fall wird die `params` -Objekt muss mindestens über die Image Serving-URL verfügen, die als `serverUrl` -Eigenschaft und das erste Asset als `asset` Parameter. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss zum DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder im Hauptteil `onload()` -Ereignis.

   Gleichzeitig sollte das Containerelement nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit `display:none` Stil zugewiesen. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Wenn diese Aktion erfolgt, wird der Viewer automatisch neu geladen.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. Das Beispiel geht von `flyoutViewer` ist die Viewer-Instanz; `s7viewer` ist der Name des Platzhalters `DIV`; `http://s7d1.scene7.com/is/image/` ist die Image Serving-URL; und `Scene7SharedAssets/ImageSet-Views-Sample` ist das Asset:

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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Flyout-Viewer mit einer festen Größe einbettet:

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

## Responsives Design mit uneingeschränkter Höhe {#section-056cb574713c4d07be6d07cf3c598839}

Mit responsiver Designeinbettung verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers bestimmt `DIV`. Im folgenden Beispiel wird angenommen, dass die Webseite den Container des Viewers zulässt `DIV` , um 40 % der Fenstergröße des Webbrowsers zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten zum Einbetten fester Größe. Der einzige Unterschied besteht darin, dass Sie die feste Größe von der standardmäßigen Viewer-CSS mit der in relativen Einheiten festgelegten Größe überschreiben müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Container definieren `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung in feste Größe identisch, mit den folgenden drei Ausnahmen:

* Container hinzufügen `DIV` an den bestehenden &quot;Inhaber&quot; `DIV`;
* hinzugefügt `imagereload` Parameter mit expliziten Haltepunkten;
* Anstatt eine feste Viewer-Größe mit absoluten Einheiten festzulegen, verwenden Sie CSS, das die Breite und Höhe des Viewers auf 100 % festlegt, wie im Folgenden gezeigt:

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

Die folgende Beispielseite zeigt die reale Nutzung responsiver Designs, die mit unbegrenzter Höhe eingebettet werden:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demostandort](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Flexible Größeneinbettung mit definierter Breite und Höhe {#section-0a329016f9414d199039776645c693de}

Wenn eine Einbettung in flexibler Größe mit definierter Breite und Höhe erfolgt, unterscheidet sich der Webseitenstil. Sie bietet beide Größen für die `"holder"` DIV und zentriert es im Browserfenster. Außerdem legt die Webseite die Größe der `HTML` und `BODY` auf 100 Prozent.

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

Die übrigen Schritte zum Einbetten sind mit den Schritten für responsives Design identisch, das mit uneingeschränkter Höhe eingebettet wird. Das folgende Beispiel zeigt:

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

## Einbetten mit der Setter-basierten API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit `setContainerId()`, `setParam()`und `setAsset()` API-Methoden mit separaten JavaScript-Aufrufen.

Das folgende Beispiel zeigt die Verwendung der Einbettung fester Größe in eine setter-basierte API:

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
