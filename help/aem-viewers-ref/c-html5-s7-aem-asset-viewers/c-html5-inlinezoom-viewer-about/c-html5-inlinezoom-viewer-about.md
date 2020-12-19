---
description: Der Inline-Zoom-Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version über dem statischen Bild angezeigt, wenn ein Benutzer die Hauptansicht berührt oder den Mauszeiger über die Ansicht bewegt. Dieser Viewer funktioniert mit Bildsätzen, und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.
keywords: responsive
seo-description: Der Inline-Zoom-Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version über dem statischen Bild angezeigt, wenn ein Benutzer die Hauptansicht berührt oder den Mauszeiger über die Ansicht bewegt. Dieser Viewer funktioniert mit Bildsätzen, und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.
seo-title: Inline-Zoom
solution: Experience Manager
title: Inline-Zoom
topic: Dynamic media
uuid: 2287aef0-79ba-4d63-911a-969fa1c63385
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2457'
ht-degree: 0%

---


# Inline-Zoom{#inline-zoom}

Der Inline-Zoom-Viewer ist ein Bild-Viewer. Es wird ein statisches Bild mit der gezoomten Version über dem statischen Bild angezeigt, wenn ein Benutzer die Hauptansicht berührt oder den Mauszeiger über die Ansicht bewegt. Dieser Viewer funktioniert mit Bildsätzen, und die Navigation erfolgt mithilfe von Farbfeldern. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Der Viewer-Typ ist 504.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## Verwenden des Inline-Zoom-Viewers {#section-f21ac23d3f6449ad9765588d69584772}

Der Inline-Zoom-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar (ein einzelnes JavaScript enthält alle Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Der Inline-Zoom-Viewer kann sowohl im Popupmodus mit produktionsfertiger HTML-Seite, die mit Image Serving Viewers bereitgestellt wird, als auch im eingebetteten Modus verwendet werden, wobei er mithilfe der dokumentierten API in eine Zielgruppe-Webseite integriert wird.

Konfigurationen und Skins ähneln denen anderer Viewer. Sie können benutzerdefinierte CSS verwenden, um Skins anzuwenden.

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz, die allen Viewern gemein ist - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem Inline-Zoom-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Der Inline-Zoom-Viewer unterstützt Single-Touch- und Multi-Touch-Gesten, die in anderen Mobilanwendungen häufig vorkommen.

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
   <td colname="col2"> <p> Aktiviert die Flyout-Ansicht oder ändert sich zwischen dem primären und dem sekundären Zoomgrad in Farbfeldern, wählt neue Miniaturansichten aus. </p> </td> 
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

Der Viewer unterstützt auch die Eingabe per Touch- und Mausklick auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf die Webbrowser Chrome, Internet Explorer 11 und Edge beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Barrierefreiheit und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des Inline-Zoom-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen anklickbaren Link bereit, über den der Viewer in einem separaten Browserfenster geöffnet wird. In anderen Fällen ist es ggf. erforderlich, den Viewer direkt in die Hosting-Seite einzubetten. Im letzteren Fall verfügt die Webseite möglicherweise über ein statisches Seitenlayout oder über ein reaktionsfähiges Design, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung in fester Größe und responsives Einbetten.

**Popup**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Browserfenster-Bereich in Anspruch und passt sich an, wenn die Größe des Browserfensters oder die Geräteausrichtung geändert wird.

Dieser Modus ist der am häufigsten verwendete für Mobilgeräte. Die Webseite lädt den Viewer mit dem JavaScript-Aufruf `window.open()`, dem korrekt konfigurierten `A` HTML-Element oder einer anderen geeigneten Methode.

Es wird empfohlen, die vordefinierte HTML-Seite für den Popupmodus `FlyoutViewer.html` zu verwenden. Sie befindet sich im Unterordner [!DNL html5/] Ihrer standardmäßigen Image Serving-Viewers-Bereitstellung:

`<s7viewers_root>/html5/FlyoutViewer.html`

Außerdem muss die FlyoutZoomView-Komponente so konfiguriert sein, dass sie im Inline-Zoommodus funktioniert. Es wird empfohlen, die vordefinierte Vorgabe `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` für den Inline-Zoom-Viewer oder eine daraus abgeleitete benutzerdefinierte Vorgabe zu verwenden. Visuelle Anpassungen können durch Anwendung von benutzerdefiniertem CSS erreicht werden.

Im Folgenden finden Sie ein HTML-Codebeispiel, das den Viewer in einem neuen Fenster öffnet:

```
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Einbettung mit fester Größe und Einbettung mit automatischer Anpassung**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Zusammenhang stehen. Der Viewer belegt normalerweise nur einen Teil der Webseiteneigenschaft.

Der primäre Anwendungsfall sind Webseiten, die auf Desktop- oder Tablet-Geräte ausgerichtet sind, sowie reaktionsfähige Webseiten, die das Layout automatisch an den Gerätetyp anpassen.

Der Einbettungsmodus für feste Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Option eignet sich am besten für Webseiten mit einem statischen Seitenlayout.

Der responsive Design-Einbettungsmodus setzt voraus, dass die Größe des Viewers während der Laufzeit je nach Größenänderung des Containers `DIV` ggf. angepasst werden muss. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Stellen Sie bei Verwendung des interaktiven Entwurfs-Einbettungsmodus mit dem Inline-Zoom-Viewer sicher, dass Sie explizite Haltepunkte für das Hauptbild der Ansicht mit dem Parameter `imagereload` angeben. Im Idealfall sollten Sie Ihre Haltepunkte mit den vom CSS der Webseite diktierten BreitenHaltepunkten des Viewers abgleichen.

Im Einbettungsmodus für reaktionsfähiges Design verhält sich der Viewer je nach Größe des Containers einer Webseite unterschiedlich. `DIV` Wenn auf der Webseite nur die Breite des Containers `DIV` festgelegt wird und die Höhe nicht eingeschränkt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Das bedeutet, dass der Vermögenswert perfekt in die Ansicht passt, ohne dass eine seitliche Auffüllung erforderlich ist. Dieser spezielle Anwendungsfall ist der häufigste Fall für Webseiten, die reaktionsfähige Layout-Frameworks wie Bootstrap, Foundation usw. verwenden.

Andernfalls füllt der Viewer, wenn die Webseite sowohl die Breite als auch die Höhe des Containers des Viewers `DIV` festlegt, nur diesen Bereich und folgt der vom Webseitenlayout bereitgestellten Größe. Ein gutes Verwendungsfallbeispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung der Größe des Webbrowser-Fensters entspricht.

**Einbettung fester Größe**

Der Viewer wird wie folgt zu einer Webseite hinzugefügt:

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Containers `DIV`.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite

   Zum Erstellen eines Viewers müssen Sie im HTML-Kopf ein Skript-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie `FlyoutViewer.js` einschließen. `FlyoutViewer.js` befindet sich im folgenden  [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Scene7-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem Adobe Scene7-Server an, auf dem die IS-Viewer installiert sind.

Ein relativer Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Sie sollten nur auf die JavaScript-Hauptdatei des Viewers `include` auf Ihrer Seite verweisen. Sie sollten keine weiteren JavaScript-Dateien im Webseitencode referenzieren, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Insbesondere sollten Sie nicht direkt auf die HTML5 SDK `Utils.js`-Bibliothek verweisen, die vom Viewer aus dem Kontextpfad `/s7viewers` geladen wird (so genanntes konsolidiertes SDK `include`). Der Grund dafür ist, dass der Speicherort von `Utils.js`- oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig durch die Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Ältere Versionen des sekundären Viewers `includes` werden von der Adobe nicht auf dem Server gespeichert.
>
>
>Infolgedessen wird die Viewer-Funktionalität bei der Bereitstellung einer neuen Produktversion durch die direkte Referenz auf sekundäres JavaScript `include`, das vom Viewer auf der Seite verwendet wird, in Zukunft unterbrochen.

1. Definieren des Container-DIV.

   hinzufügen ein leeres DIV-Element auf die Seite, auf der der Viewer angezeigt werden soll. Die ID des DIV-Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h., die CSS-Eigenschaft ist auf `position` oder `relative` eingestellt.`absolute`

   Es liegt in der Verantwortung der Webseite, das richtige `z-index` für das Platzhalter-DIV-Element anzugeben. Dadurch wird sichergestellt, dass der Flyout-Bereich des Viewers über den anderen Webseitenelementen angezeigt wird.

   Das folgende Beispiel zeigt ein definiertes Platzhalter-DIV-Element:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Einstellen der Viewer-Größe.

   In diesem Viewer werden Miniaturansichten angezeigt, wenn Sie mit Sets mit mehreren Elementen arbeiten. Auf Desktop-Systemen werden Miniaturansichten unterhalb der Hauptversion der Ansicht platziert. Gleichzeitig ermöglicht der Viewer den Austausch des Hauptassets während der Laufzeit mit der API `setAsset()`. Als Entwickler haben Sie die Kontrolle darüber, wie der Viewer den Bereich &quot;Miniaturansichten&quot;im unteren Bereich verwaltet, wenn das neue Asset nur ein Element enthält. Es ist möglich, die Größe des äußeren Viewers beizubehalten und die Haupthöhe der Ansicht zu erhöhen und den Bereich der Miniaturansichten zu belassen. Oder Sie können die Größe der Hauptseite statisch beibehalten und den äußeren Viewer-Bereich reduzieren, damit der Inhalt der Ansicht nach oben verschoben werden kann, und dann die freie Seitenposition verwenden, die von den Miniaturbildern übrig bleibt.

   Um die äußeren Viewer-Grenzen intakt zu halten, definieren Sie die Größe der CSS-Klasse der obersten Ebene in absoluten Einheiten. `.s7flyoutviewer` Die Größe in CSS kann direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festgelegt werden, die später im Scene7 Publishing System einem Viewer-Vorgabendatensatz zugewiesen oder explizit mit dem Stilbefehl übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Inline-Zoom-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451).

   Das folgende Beispiel zeigt die Definition der statischen äußeren Viewer-Größe in einer HTML-Seite:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können das Verhalten mit einem festen äußeren Viewer-Bereich auf der folgenden Beispielseite sehen. Beachten Sie, dass sich die Größe des äußeren Viewers beim Wechseln zwischen den Sets nicht ändert:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html)

   Um die Hauptabmessungen der Ansicht statisch zu machen, definieren Sie die Viewer-Größe in absoluten Maßeinheiten für die innere SDK-Komponente `Container` mithilfe des CSS-Selektors `.s7flyoutviewer .s7container`. Darüber hinaus sollten Sie die für die CSS-Klasse der obersten Ebene definierte feste Größe im Standard-Viewer-CSS außer Kraft setzen, indem Sie sie auf `.s7flyoutviewer` festlegen.`auto`

   Im Folgenden sehen Sie ein Beispiel für die Definition der Viewer-Größe für die innere SDK-Komponente `Container`, sodass der Hauptbereich &quot;Ansicht&quot;beim Wechseln des Assets seine Größe nicht ändert:

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

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html)

   Beachten Sie außerdem, dass das Standard-Viewer-CSS eine feste Größe für den Außenbereich bereitstellt.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.FlyoutViewer`, geben Sie alle Konfigurationsinformationen an den Konstruktor weiter und rufen Sie die Methode `init()` für eine Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID und das verschachtelte `params`-JSON-Objekt mit den vom Viewer unterstützten Konfigurationsparametern enthält. In diesem Fall muss für das `params`-Objekt mindestens die Image Serving-URL als `serverUrl`-Eigenschaft, das anfängliche Asset als `asset`-Parameter, der Basispfad zum Laden der CSS als `contentUrl`-Parameter und der Vorgabenname als `config`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und Beginn erstellen.

   Es ist wichtig, dass der Viewer-Container dem DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser zögern die Erstellung von DOM bis zum Ende der Webseite. Um eine maximale Kompatibilität zu gewährleisten, rufen Sie die `init()`-Methode direkt vor dem schließenden `BODY`-Tag oder im Body `onload()`-Ereignis auf.

   Gleichzeitig sollte das Container-Element nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mit dem `display:none`-Stil ausgeblendet werden, der ihm zugewiesen wurde. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das die notwendigen Mindestkonfigurationsoptionen an den Konstruktor übergibt und die `init()`-Methode aufruft. Das Beispiel geht davon aus, dass `inlineZoomViewer` die Viewer-Instanz ist. `s7viewer` ist der Name des Platzhalters `DIV`; `http://s7d1.scene7.com/is/image/` ist die Image Serving-URL; und `Scene7SharedAssets/ImageSet-Views-Sample` ist das Asset:

   ```
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, die den Inline-Zoom-Viewer mit einer festen Größe einbettet:

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
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Responsive Design-Einbettung mit unbeschränkter Höhe {#section-056cb574713c4d07be6d07cf3c598839}

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten zum Einbetten in feste Größe. Der einzige Unterschied besteht darin, dass Sie die feste Größe vom Standard-Viewer-CSS mit der in relativen Einheiten festgelegten Größe überschreiben müssen.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Containers `DIV`.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit den folgenden drei Ausnahmen identisch:

* den Container `DIV` zum vorhandenen &quot;Halter&quot; `DIV` hinzufügen;
* Parameter `imagereload` mit expliziten Haltepunkten hinzugefügt;
* anstatt eine feste Viewer-Größe mit absoluten Einheiten festzulegen, verwenden Sie CSS, das den Viewer `width` und `height` wie folgt auf 100 % setzt:

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
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
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

## Einbetten flexibler Größe mit definierter Breite und Höhe {#section-0a329016f9414d199039776645c693de}

Bei Einbettung in flexibler Größe mit definierter Breite und Höhe ist der Webseitenstil anders. Es stellt beide Größen für das DIV `"holder"` bereit und zentriert es im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und `BODY` auf 100 Prozent.

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
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Einbetten mit Setter-basierter API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Anstatt JSON-basierte Initialisierung zu verwenden, ist es möglich, set-basierte API- und no-args-Konstruktoren zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` und mit separaten JavaScript-Aufrufen angegeben.

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
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```

