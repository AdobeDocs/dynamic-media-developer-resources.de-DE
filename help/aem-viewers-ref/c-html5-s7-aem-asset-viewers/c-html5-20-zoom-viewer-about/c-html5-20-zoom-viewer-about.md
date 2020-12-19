---
description: Der Zoom-Viewer ist ein Bild-Viewer, der ein Zoombild anzeigt. Dieser Viewer funktioniert mit Bildsätzen, und die Navigation erfolgt mithilfe von Farbfeldern. Es verfügt über Zoomwerkzeuge, Vollbildunterstützung, Farbfelder und eine optionale Schließen-Schaltfläche. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.
keywords: responsive
seo-description: Der Zoom-Viewer ist ein Bild-Viewer, der ein Zoombild anzeigt. Dieser Viewer funktioniert mit Bildsätzen, und die Navigation erfolgt mithilfe von Farbfeldern. Es verfügt über Zoomwerkzeuge, Vollbildunterstützung, Farbfelder und eine optionale Schließen-Schaltfläche. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.
seo-title: Zoom
solution: Experience Manager
title: Zoom
topic: Dynamic media
uuid: ec2a91e2-ce2c-48b1-a2b2-8671524288c7
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2460'
ht-degree: 0%

---


# Zoom{#zoom}

Der Zoom-Viewer ist ein Bild-Viewer, der ein Zoombild anzeigt. Dieser Viewer funktioniert mit Bildsätzen, und die Navigation erfolgt mithilfe von Farbfeldern. Es verfügt über Zoomwerkzeuge, Vollbildunterstützung, Farbfelder und eine optionale Schließen-Schaltfläche. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ 502.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Verwenden des Zoom-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der Zoom-Viewer stellt eine Haupt-JavaScript-Datei und eine Reihe von Hilfedateien dar (ein einzelnes JavaScript enthält alle Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Sie können den Zoom-Viewer im Popupmodus verwenden, indem Sie eine produktionsfertige HTML-Seite verwenden, die mit IS-Viewern bereitgestellt wird, oder im eingebetteten Modus, wo er mithilfe der dokumentierten API in die Zielgruppe-Webseite integriert ist.

Konfigurationen und Skins ähneln denen anderer Viewer. Alle Skins werden mithilfe von benutzerdefiniertem CSS erreicht.

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz, die allen Viewern gemein ist - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem Zoom-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der Zoom-Viewer unterstützt die folgenden Berührungsgesten, die in anderen Mobilanwendungen häufig vorkommen. Wenn der Viewer die Blättergeste des Benutzers nicht verarbeiten kann, leitet er das Ereignis an den Webbrowser weiter, um einen nativen Seitenbildlauf durchzuführen. Mit dieser Funktion kann der Benutzer durch die Seite navigieren, selbst wenn der Viewer den größten Teil des Gerätebildschirms einnimmt.

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
   <td colname="col2"> <p> Wählt neue Miniaturansichten in Farbfeldern aus. In der Hauptversion werden Elemente der Benutzeroberfläche ausgeblendet oder eingeblendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dublette Tippen </p> </td> 
   <td colname="col2"> <p> Vergrößert eine Ebene, bis die maximale Vergrößerung erreicht ist. Durch Tippen auf die nächste Dublette wird der Viewer auf den anfänglichen Anzeigestatus zurückgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinch </p> </td> 
   <td colname="col2"> <p>Vergrößert oder verkleinert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontale Blättergeste oder Flick </p> </td> 
   <td colname="col2"> <p> Blättert durch die Liste der Farbfelder in der Farbfeldleiste. </p> <p> Wenn sich das Bild in einem Reset-Zustand befindet und der Parameter <span class="codeph"> frametransition </span> auf "Slide"festgelegt ist, wird das Asset mit der Diashow-Animation geändert. Bei anderen Modi <span class="codeph"> frametransition </span> führt die Geste einen nativen Seitenbildlauf durch. </p> <p> Wenn das Bild vergrößert wird, wird es horizontal verschoben. Wenn das Bild an den Rand der Ansicht verschoben wird und eine Blättergeste in derselben Richtung ausgeführt wird, führt die Geste einen nativen Seitenbildlauf durch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikale Blättergeste </p> </td> 
   <td colname="col2"> <p> Wenn sich das Bild in einem Reset-Status befindet, führt die Geste einen nativen Bildlauf durch. </p> <p> Wenn das Bild vergrößert wird, wird es vertikal verschoben. Wenn das Bild an den Rand der Ansicht verschoben wird und eine Blättergeste in derselben Richtung ausgeführt wird, führt die Geste einen nativen Seitenbildlauf durch. </p> <p> Wenn die Geste innerhalb des Farbfeldbereichs erfolgt, führt sie einen nativen Seitenbildlauf durch. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt sowohl Berührungseingaben als auch Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf die Webbrowser Chrome, Internet Explorer 11 und Edge beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Barrierefreiheit und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des Zoom-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, über den der Viewer bei einem Klick in einem separaten Browserfenster geöffnet wird. In anderen Fällen ist es erforderlich, den Viewer direkt in die Hostingseite einzubetten. In letzterem Fall kann die Webseite ein statisches Layout haben oder reaktionsfähiges Design verwenden, das auf verschiedenen Geräten oder für verschiedene Fenstergrößen im Browser unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung in fester Größe und Einbettung in reaktionsfähiges Design.

**Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Browserfenster-Bereich und passt sich an, falls die Größe des Browsers oder die Geräteausrichtung geändert wird.

Dieser Modus ist der am häufigsten verwendete für Mobilgeräte. Die Webseite lädt den Viewer mit dem JavaScript-Aufruf `window.open()`, dem ordnungsgemäß konfigurierten `A` HTML-Element oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Modus zu verwenden. Die vordefinierte HTML-Seite heißt `ZoomViewer.html` und befindet sich im Unterordner `html5/` Ihrer standardmäßigen IS-Viewer-Bereitstellung wie folgt:

`<s7viewers_root>/html5/ZoomViewer.html`

Wenden Sie benutzerdefiniertes CSS an, um ein benutzerdefiniertes Erscheinungsbild für die Seite zu erhalten.

Im Folgenden finden Sie ein Beispiel für HTML-Code, mit dem der Viewer im neuen Fenster geöffnet wird:

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Einbettungsmodus mit fester Größe und Einbettungsmodus für reaktionsfähiges Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Zusammenhang stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilie der Webseite.

Die wichtigsten Anwendungsfälle sind Webseiten, die auf Desktop- oder Tablet-Geräte ausgerichtet sind, sowie reaktionsfähige Seiten, die das Layout je nach Gerätetyp automatisch anpassen.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Option ist die beste Wahl für Webseiten mit einem statischen Layout.

Der responsive Design-Einbettungsmodus setzt voraus, dass die Größe des Viewers während der Laufzeit aufgrund der Größenänderung des Containers `DIV` angepasst werden muss. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite mit flexiblem Layout.

Im Einbettungsmodus für reaktionsfähiges Design verhält sich der Viewer je nach Größe des Containers `DIV` der Webseite unterschiedlich. Wenn auf der Webseite nur die Breite des Containers `DIV` festgelegt wird und die Höhe nicht eingeschränkt bleibt, wählt der Viewer die Höhe automatisch entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Logik stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten aufgefüllt werden. Dieser Anwendungsfall ist der häufigste Fall für Webseiten, die reaktionsfähige Layout-Frameworks wie Bootstrap, Foundation usw. verwenden.

Wenn die Webseite sowohl die Breite als auch die Höhe des Containers des Viewers `DIV` festlegt, füllt der Viewer diesen Bereich und folgt der auf der Webseite angegebenen Größe. Einbetten des Viewers in eine modale Überlagerung, wobei die Größe der Überlagerung der Größe des Webbrowserfensters entspricht.

## Einbettung fester Größe {#section-44f365e6c0dd40709467a459afa82a7f}

Der Viewer wird wie folgt zu einer Webseite hinzugefügt:

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Container-DIV.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite

   Zum Erstellen eines Viewers müssen Sie im HTML-Kopf ein Skript-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL ZoomViewer.js] einschließen. Die Datei [!DNL ZoomViewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Dynamic Media Classic-Server der Adobe bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Server der Adobe Dynamic Media Classic an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
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

   Das folgende Beispiel zeigt ein definiertes Platzhalter-DIV-Element:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Einstellen der Viewer-Größe.

   In diesem Viewer werden Miniaturansichten angezeigt, wenn Sie mit Sets mit mehreren Elementen arbeiten. Auf Desktop-Systemen werden Miniaturansichten unterhalb der Hauptversion der Ansicht platziert. Gleichzeitig ermöglicht der Viewer den Austausch des Hauptassets in der Laufzeit mit der API `setAsset()`. Als Entwickler haben Sie die Kontrolle darüber, wie der Viewer den Bereich &quot;Miniaturansichten&quot;unten verwaltet, wenn das neue Asset nur ein Element enthält. Es ist möglich, die Größe des äußeren Viewers unverändert zu lassen und die Haupthöhe der Ansicht zu erhöhen und den Bereich der Miniaturansichten zu vergrößern. Oder Sie können die Größe der Hauptversion statisch beibehalten und den äußeren Viewer-Bereich reduzieren, damit der Inhalt der Ansicht nach oben verschoben werden kann, und den freien Bildschirmhintergrund aus den Miniaturbildern verwenden.

   Um die äußeren Viewer-Grenzen intakt zu halten, definieren Sie die Größe der CSS-Klasse der obersten Ebene in absoluten Einheiten. `.s7zoomviewer` Die Größe in CSS kann direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festgelegt werden, die später im Scene7 Publishing System einem Viewer-Vorgabendatensatz zugewiesen oder explizit mit einem Stilbefehl übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Zoom-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0).

   Im Folgenden sehen Sie ein Beispiel für die Definition einer statischen äußeren Viewer-Größe in HTML-Seiten:

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Das Verhalten mit einem festen äußeren Viewer wird im folgenden Beispiel gezeigt. Beachten Sie, dass sich die Größe des äußeren Viewers beim Wechseln zwischen den Sets nicht ändert:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html)

   Um die Hauptabmessungen der Ansicht statisch zu machen, definieren Sie die Viewer-Größe in absoluten Maßeinheiten für die innere Komponente `Container` SDK mit dem CSS-Selektor `.s7zoomviewer` `.s7container` oder mit dem Modifikator `stagesize`.

   Im Folgenden sehen Sie ein Beispiel für die Definition der Viewer-Größe für die innere SDK-Komponente `Container`, sodass der Hauptbereich &quot;Ansicht&quot;beim Wechseln des Assets seine Größe nicht ändert:

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Auf der folgenden Demo-Seite wird das Viewer-Verhalten mit einer festen Größe der Haupt-Ansicht dargestellt. Beachten Sie, dass beim Wechseln zwischen Sets die Hauptinhalt-Ansicht statisch bleibt und der Webseiteninhalt vertikal verschoben wird.

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html)

   Sie können den Modifikator `stagesize` entweder im Viewer-Vorgabendatensatz im Scene7 Publishing System oder explizit mit dem Viewer-Initialisierungscode mit der Sammlung `params` oder als API-Aufruf, wie im Abschnitt &quot;Befehlsreferenz&quot;dieser Hilfe beschrieben, wie im Folgenden beschrieben, festlegen:

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.ZoomViewer`, geben Sie alle Konfigurationsinformationen an den Konstruktor weiter und rufen Sie die Methode `init()` für eine Viewer-Instanz auf.

   Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID und das verschachtelte `params`-JSON-Objekt mit den vom Viewer unterstützten Konfigurationsparametern enthält. In diesem Fall muss für das `params`-Objekt mindestens die Image Serving-URL als `serverUrl`-Eigenschaft und das ursprüngliche Asset als `asset`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und mit einem Beginn versehen.

   Es ist wichtig, dass der Viewer-Container dem DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser zögern die Erstellung von DOM bis zum Ende der Webseite. Um eine maximale Kompatibilität zu gewährleisten, rufen Sie die `init()`-Methode direkt vor dem schließenden `BODY`-Tag oder im Body `onload()`-Ereignis auf.

   Gleichzeitig sollte das Container-Element nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mit dem `display:none`-Stil ausgeblendet werden, der ihm zugewiesen wurde. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der notwendigen Mindestkonfigurationsoptionen an den Konstruktor und Aufrufen der `init()`-Methode. In diesem Beispiel wird davon ausgegangen, dass `zoomViewer` die Viewer-Instanz ist, `s7viewer` der Name des Platzhalters DIV, `http://s7d1.scene7.com/is/image/` die Image Serving-URL und `Scene7SharedAssets/ImageSet-Views-Sample` das Asset.

   ```
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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, die den Video-Viewer mit einer festen Größe einbettet:

   ```
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

## Responsive Design-Einbettung mit unbeschränkter Höhe {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten zum Einbetten in feste Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind identisch mit denen der Einbettung in fester Größe. hinzufügen Sie den Container DIV an das vorhandene `"holder"` DIV. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```
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

Die folgende Beispielseite zeigt die aktuelleren Einsatzmöglichkeiten von reaktionsfähigem Design-Einbettung mit uneingeschränkter Höhe:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Flexible Einbettung mit definierter Breite und Höhe{#section-3674e6c032594441a6576b7fb1de6e64}

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

## Einbetten mit setter-basierter API {#section-44e014925f24418b900696003855c0a9}

Anstatt JSON-basierte Initialisierung zu verwenden, ist es möglich, set-basierte API- und no-args-Konstruktoren zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` und mit separaten JavaScript-Aufrufen angegeben.

Im folgenden Beispiel wird die Einbettung in feste Größe mit setter-basierter API veranschaulicht:

```
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

