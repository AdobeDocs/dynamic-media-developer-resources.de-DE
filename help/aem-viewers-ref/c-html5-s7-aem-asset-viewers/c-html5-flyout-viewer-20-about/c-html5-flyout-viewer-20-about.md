---
title: Flyout
description: Flyout Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version angezeigt, die in der Flyout-Ansicht angezeigt wird, die von einem Benutzer aktiviert wird. Dieser Viewer arbeitet mit Bildsets, und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für Desktop-PCs und mobile Geräte entwickelt.
keywords: Responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '2011'
ht-degree: 0%

---

# Flyout{#flyout}

Flyout Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version angezeigt, die in der Flyout-Ansicht angezeigt wird, die von einem Benutzer aktiviert wird. Dieser Viewer arbeitet mit Bildsets, und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für Desktop-PCs und mobile Geräte entwickelt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ ist 504.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Verwenden des Flyout-Viewers {#section-f21ac23d3f6449ad9765588d69584772}

Der Flyout-Viewer stellt eine JavaScript-Hauptdatei und einen Satz Hilfsdateien (ein einziges JavaScript Include mit allen Viewer-SDK-Komponenten, die von diesem bestimmten Viewer verwendet werden, Assets, CSS) dar, die vom Viewer zur Laufzeit heruntergeladen wurden

Flyout-Viewer ist nur für die Verwendung in eingebetteten Formularen vorgesehen, was bedeutet, dass er mithilfe der dokumentierten API in die Web-Seite integriert wird. Für den Flyout-Viewer ist keine produktionsbereite Web-Seite verfügbar.

Konfiguration und Skinning sind mit denen der anderen Viewer vergleichbar. Sie können benutzerdefiniertes CSS verwenden, um die Skin anzuwenden.

Siehe [Für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Für alle Viewer gemeinsame Befehlsreferenz - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit Flyout-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Flyout Viewer unterstützt Single-Touch- und Multi-Touch-Gesten, die in anderen Mobile Apps üblich sind.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geste </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Einfaches Tippen </p> </td> 
   <td colname="col2"> <p> Aktiviert die Flyout-Ansicht oder wechselt zwischen primärer und sekundärer Zoom-Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontales Wischen oder Schnipsen </p> </td> 
   <td colname="col2"> <p> Scrollt durch die Liste der Farbfelder in der Farbfeldleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Wischen </p> </td> 
   <td colname="col2"> <p>Wenn die Geste innerhalb des Farbfeldbereichs ausgeführt wird, wird ein nativer Seitenscroll durchgeführt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt auch Touch-Eingabe und Mauseingabe auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.

Dieser Viewer ist vollständig mit der Tastatur zugänglich.

Siehe [Tastaturzugriff und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des Flyout-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Web-Seiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Die Web-Seite kann ein statisches Seiten-Layout haben oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diesen Anforderungen gerecht zu werden, unterstützt der Viewer zwei primäre Betriebsmodi: Einbettung mit fester Größe und Einbetten in responsives Design.

Der Einbettungsmodus für feste Größe wird verwendet, wenn der Viewer nach dem ersten Laden seine Größe nicht ändert. Diese Auswahl eignet sich am besten für Web-Seiten mit statischem Seiten-Layout.

Beim responsiven Design-Einbettungsmodus wird davon ausgegangen, dass die Größe des Viewers während der Laufzeit entsprechend der Größenänderung seiner Container-`DIV` geändert werden muss. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Web-Seite, die ein flexibles Seiten-Layout verwendet.

Wenn Sie den responsiven Design-Einbettungsmodus mit dem Flyout-Viewer verwenden, stellen Sie sicher, dass Sie explizite Haltepunkte für das Hauptansichtsbild mithilfe des `imagereload` angeben. Idealerweise sollten Sie Ihre Breakpoints entsprechend den Viewer-Breitenhaltepunkten der Web-Seiten-CSS anpassen.

Im responsiven Design-Einbettungsmodus verhält sich der Viewer je nach der Größe eines Web-Seiten-Containers anders `DIV`. Wenn die Web-Seite nur die Breite des Container-`DIV` festlegt und seine Höhe nicht beschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktionalität bedeutet, dass das Asset perfekt in die Ansicht passt, ohne dass an den Seiten ein Abstand vorhanden ist. Dieser spezielle Anwendungsfall ist der häufigste für Web-Seiten, die responsive Design-Layout-Frameworks wie Bootstrap und Foundation verwenden.

Wenn die Web-Seite jedoch sowohl die Breite als auch die Höhe für die Container-`DIV` des Viewers festlegt, füllt der Viewer nur diesen Bereich aus und folgt der vom Web-Seiten-Layout bereitgestellten Größe. Ein gutes Anwendungsbeispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung an die Fenstergröße des Webbrowsers angepasst ist.

**Einbetten in fester Größe**

Sie können den Viewer wie folgt zu einer Web-Seite hinzufügen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Container-`DIV` definieren.
1. Festlegen der Viewer-Größe.
1. Viewer erstellen und initialisieren.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.

   Um einen Viewer zu erstellen, müssen Sie ein -Skript-Tag in der Kopfzeile von HTML hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie `FlyoutViewer.js` einbeziehen. `FlyoutViewer.js` befindet sich im folgenden [!DNL html5/js/]-Unterordner Ihrer standardmäßigen IS-Viewers-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media-Server bereitgestellt wird und er von derselben Domain bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media-Server an, auf denen die IS-Viewer installiert sind.

Ein relativer Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Verweisen Sie auf Ihrer Seite nur auf die JavaScript-`include`-Datei des Haupt-Viewers. Verweisen Sie nicht auf zusätzliche JavaScript-Dateien im Web-Seiten-Code, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die HTML5 SDK `Utils.js`-Bibliothek, die vom Viewer aus `/s7viewers` Kontextpfad geladen wird (so genannte konsolidierte SDK-`include`). Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Runtime-Viewer-Bibliotheken vollständig von der Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Adobe speichert keine älteren Versionen der sekundären Viewer-`includes` auf dem Server.
>
>
>Wenn Sie also auf der Seite einen direkten Verweis auf eine sekundäre JavaScript-`include` einfügen, die vom Viewer verwendet wird, wird die Viewer-Funktionalität in Zukunft unterbrochen, wenn eine neue Produktversion bereitgestellt wird.

1. Definieren des Container-DIV.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres DIV-Element hinzu. Für das DIV-Element muss eine ID definiert sein, da diese ID später an die Viewer-API übergeben wird.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute` festgelegt.

   Es liegt in der Verantwortung der Web-Seite, die richtige `z-index` für das Platzhalter-DIV-Element anzugeben. Dadurch wird sichergestellt, dass der Flyout-Teil des Viewers über den anderen Web-Seitenelementen angezeigt wird.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-DIV-Element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Festlegen der Viewer-Größe.

   Dieser Viewer zeigt Miniaturen bei der Arbeit mit Sets mit mehreren Elementen an. Auf Desktop-Systemen werden Miniaturansichten unter der Hauptansicht platziert. Gleichzeitig ermöglicht der Viewer den Austausch des Haupt-Assets während der Laufzeit mithilfe `setAsset()` API. Als Entwickler haben Sie die Kontrolle darüber, wie der Viewer den Bereich mit den Miniaturen im unteren Bereich verwaltet, wenn das neue Asset nur ein Element enthält. Es ist möglich, die äußere Viewer-Größe intakt zu halten und die Hauptansicht ihre Höhe erhöhen und den Bereich für Miniaturen belegen zu lassen. Sie können auch die Größe der Hauptansicht unverändert lassen und den äußeren Viewer-Bereich reduzieren, sodass der Webseiteninhalt nach oben verschoben wird, und dann die freie Seitenumgebung links von den Miniaturen verwenden.

   Um die äußeren Viewer-Grenzen intakt zu halten, definieren Sie die Größe für `.s7flyoutviewer` CSS-Klasse der obersten Ebene in absoluten Einheiten. Die Größenanpassung in CSS kann direkt auf der HTML-Seite oder in einer benutzerdefinierten CSS-Viewer-Datei vorgenommen, später einem Viewer-Vorgabeneintrag in Dynamic Media Classic zugewiesen oder explizit mit dem Stilbefehl übergeben werden.

   Weitere Informationen [&#x200B; Formatieren des Viewers mit CSS finden Sie unter „Anpassen &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) Flyout-Viewers“ .

   Im Folgenden finden Sie ein Beispiel für die Definition der statischen äußeren Viewer-Größe auf einer HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können das Verhalten mit einem festen äußeren Viewer-Bereich auf der folgenden Beispielseite sehen. Beachten Sie, dass sich beim Wechseln zwischen Sets die Größe des äußeren Viewers nicht ändert:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   Um die Hauptansichtsdimensionen statisch zu machen, definieren Sie die Viewer-Größe in absoluten Einheiten für die SDK-Komponente des inneren `Container` mithilfe `.s7flyoutviewer .s7container` CSS-Selektors. Darüber hinaus sollten Sie die feste Größe überschreiben, die für die `.s7flyoutviewer` CSS-Klasse der obersten Ebene in der Standard-Viewer-CSS definiert ist, indem Sie sie auf `auto` setzen.

   Im Folgenden finden Sie ein Beispiel dafür, wie Sie die Viewer-Größe für die SDK-Komponente des inneren `Container` definieren, sodass der Hauptansichtsbereich beim Wechseln des Assets seine Größe nicht ändert:

   ```html {.line-numbers}
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

   Außerdem bietet das standardmäßige Viewer-CSS vorkonfiguriert eine feste Größe für den äußeren Bereich.

1. Viewer erstellen und initialisieren.

   Wenn Sie die obigen Schritte ausgeführt haben, erstellen Sie eine Instanz `s7viewers.FlyoutViewer` Klasse, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen `init()` Methode in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID enthält und `params` JSON-Objekt mit Konfigurationsparametern verschachtelt ist, die der Viewer unterstützt. In diesem Fall muss für das `params`-Objekt mindestens die Bildbereitstellungs-URL als `serverUrl`-Eigenschaft übergeben werden und das anfängliche Asset muss `asset` Parameter sein. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzigen Codezeile erstellen und starten.

   Es ist wichtig, dass der Viewer-Container zum DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser verzögern die Erstellung von DOM bis zum Ende der Web-Seite. Um maximale Kompatibilität zu erzielen, rufen Sie die `init()`-Methode unmittelbar vor dem schließenden `BODY`-Tag oder im body-`onload()` auf.

   Gleichzeitig sollte das Container-Element noch nicht unbedingt Teil des Web-Seiten-Layouts sein. Beispielsweise kann sie mithilfe `display:none` ihr zugewiesenen Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Moment, an dem die Web-Seite das Container-Element wieder zum Layout zurückbringt. Wenn diese Aktion stattfindet, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()`-Methode. Im Beispiel wird davon ausgegangen, `flyoutViewer` die Viewer-Instanz ist, `s7viewer` der Name des Platzhalters `DIV` ist, `http://s7d1.scene7.com/is/image/` die Bildbereitstellungs-URL ist und `Scene7SharedAssets/ImageSet-Views-Sample` das Asset ist:

   ```html {.line-numbers}
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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, auf der der Flyout-Viewer mit einer festen Größe eingebettet ist:

   ```html {.line-numbers}
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

## Responsives Design mit unbegrenzter Höhe {#section-056cb574713c4d07be6d07cf3c598839}

Beim Einbetten eines responsiven Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße der Container-`DIV` des Viewers bestimmt. Nehmen wir für das folgende Beispiel an, dass die Web-Seite dem Container-`DIV` des Viewers ermöglicht, 40 % der Fenstergröße des Webbrowsers zu verwenden, wobei seine Höhe nicht beschränkt wird. Der Web-Seiten-HTML-Code würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten für Einbetten in fester Größe. Der einzige Unterschied besteht darin, dass Sie die feste Größe aus dem Standard-Viewer-CSS mit der in relativen Einheiten festgelegten Größe überschreiben müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Container-`DIV` definieren.
1. Festlegen der Viewer-Größe.
1. Viewer erstellen und initialisieren.

Alle oben genannten Schritte sind dieselben wie bei der Einbettung fester Größe mit den folgenden drei Ausnahmen:

* Fügen Sie die Container-`DIV` zum vorhandenen `DIV` „Halter“ hinzu.
* `imagereload` Parameter mit expliziten Haltepunkten hinzugefügt;
* Anstatt eine feste Viewer-Größe mit absoluten Einheiten festzulegen, verwenden Sie CSS, das die Breite und Höhe des Viewers wie im Folgenden beschrieben auf 100 % festlegt:

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn der Browser skaliert wird, und wie das Seitenverhältnis des Viewers mit dem Asset übereinstimmt.

```html {.line-numbers}
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

Die folgende Beispielseite zeigt weitere reale Verwendungen der responsiven Designeinbettung mit unbegrenzter Höhe:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demo-Speicherort](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Flexible Einbettungsgröße mit definierter Breite und Höhe {#section-0a329016f9414d199039776645c693de}

Wenn es Einbettungen in flexibler Größe gibt, bei denen Breite und Höhe definiert sind, ist der Web-Seiten-Stil anders. Es stellt dem `"holder"`-DIV beide Größen zur Verfügung und zentriert ihn im Browser-Fenster. Außerdem legt die Web-Seite die Größe des `HTML`- und `BODY` auf 100 Prozent fest.

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

Die restlichen Einbettungsschritte sind identisch mit den Schritten für responsive Designeinbettung mit unbegrenzter Höhe. Das daraus resultierende Beispiel lautet:

```html {.line-numbers}
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

Anstatt die JSON-basierte Initialisierung zu verwenden, ist es möglich, eine Setter-basierte API und einen Nicht-Args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors sind keine Parameter erforderlich und Konfigurationsparameter werden mithilfe von `setContainerId()`-, `setParam()`- und `setAsset()`-API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel veranschaulicht die Verwendung der Einbettung fester Größe mit einer Setter-basierten API:

```html {.line-numbers}
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
