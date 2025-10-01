---
title: Panorama-Betrachter
description: HTML5 Panoramic Viewer ist ein Bild-Viewer, der ein Panoramabild anzeigt. Der Zweck dieses Viewers ist es, ein kugelförmiges Panorama, auch als äquirektanguläres Bild bekannt, anzuzeigen. Es unterstützt das automatische Schwenken und Schwenken durch gyroskopische Bewegung. Es wurde für Desktop-PCs und mobile Geräte entwickelt. Der Virtual-Reality-Anzeigemodus ist auf unterstützenden Mobilgeräten verfügbar.
keywords: Responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '1920'
ht-degree: 0%

---

# panoramisch{#panoramic}

HTML5 Panoramic Viewer ist ein Bild-Viewer, der ein Panoramabild anzeigt. Der Zweck dieses Viewers ist es, ein kugelförmiges Panorama, auch als äquirektanguläres Bild bekannt, anzuzeigen. Es unterstützt das automatische Schwenken und Schwenken durch gyroskopische Bewegung. Es wurde für Desktop-PCs und mobile Geräte entwickelt. Der Virtual-Reality-Anzeigemodus ist auf unterstützenden Mobilgeräten verfügbar.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Viewer-Typ 514.

<!--
## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)
-->

## Verwenden des Panorama-Viewers {#section-f21ac23d3f6449ad9765588d69584772}

Der HTML5-Panorama-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar, die der Viewer zur Laufzeit heruntergeladen hat. Der Satz von Hilfsdateien ist ein einzelnes JavaScript-Include in allen HTML5 Viewer-SDK-Komponenten, die von diesem bestimmten Viewer verwendet werden, Assets, CSS.
Der HTML5-Panoramabilder kann sowohl im Popup-Modus mit der produktionsbereiten HTML-Seite, die mit IS-Viewers bereitgestellt wird, als auch im eingebetteten Modus verwendet werden, wo er mithilfe der dokumentierten API in die Ziel-Web-Seite integriert wird.
Die Konfiguration und Skinning ähneln denen der anderen HTML5-Viewer. Die gesamte Skin-Erstellung kann mithilfe von benutzerdefiniertem CSS erfolgen.

Siehe [Für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Für alle Viewer gemeinsame Befehlsreferenz - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem HTML5-Panorama-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Der HTML5 Panoramic Viewer unterstützt das automatische Schwenken und Navigieren durch Ziehen oder gyroskopische Bewegungen.

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Navigation </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Desktop </p> </td> 
   <td colname="col2"> <p>Automatisches Schwenken und Ziehen zum Navigieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Touch-Gerät </p> </td> 
   <td colname="col2"> <p>Standardmäßig zur Navigation durch automatisches Schwenken und Ziehen. Navigieren Sie durch gyroskopische Bewegung im VR-Render-Modus (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt sowohl Touch-Eingaben als auch Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.
Der Panorama-Viewer kann Panoramabilder im Virtual-Reality-Modus (VR) rendern, indem er den Render-Modifikator angibt. Wenn das Rendern aktiviert ist, wird ein Panoramabild auf geteilten Bildschirmen angezeigt. Ein gängiger Anwendungsfall wäre die Bereitstellung des Bildes in einem Mobiltelefon, das in einem Virtual-Reality-Headset montiert ist und separate Bilder für jedes Auge bereitstellt. Der Betrachter reagiert auf die Kreiselbewegung des Kopfes und navigiert durch das Bild.

## Einbetten des HTML5-Panorama-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Web-Seiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal enthält eine Webseite einen Link. Wenn Sie auf diesen Link klicken, wird der Viewer in einem separaten Browser-Fenster geöffnet. In anderen Fällen kann es erforderlich sein, den Viewer in die Hosting-Seite einzubetten. Im letzteren Fall kann die Web-Seite ein statisches Layout haben oder „responsiv“ sein und auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt werden. Um diesen Anforderungen gerecht zu werden, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung mit fester Größe und responsive Einbettung.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Fenster oder einer separaten Registerkarte des Webbrowsers geöffnet. Sie nimmt den gesamten Browser-Fensterbereich in Anspruch und passt sich an, falls die Größe des Browsers geändert oder die Ausrichtung des Geräts geändert wird.

Dieser Modus ist bei Mobilgeräten am häufigsten. Die Web-Seite lädt den Viewer mithilfe `window.open()` JavaScript-Aufrufs, eines ordnungsgemäß konfigurierten HTML-Elements oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vorkonfigurierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Sie wird als [!DNL PanoramicViewer.html] bezeichnet und befindet sich im [!DNL html5/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

Visuelle Anpassung kann durch Anwenden von benutzerdefiniertem CSS erreicht werden.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer im neuen Fenster öffnet:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Über den Einbettungsmodus mit fester Größe und den responsiven Einbettungsmodus**

Im eingebetteten Modus wird der Viewer zu der vorhandenen Web-Seite hinzugefügt, die möglicherweise bereits einige Kundeninhalte enthält, die nicht mit dem Viewer verknüpft sind. Der Viewer belegt normalerweise nur einen Teil des Grundbesitzes von Web-Seiten.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die für Desktops oder Tablet-Geräte ausgerichtet sind, sowie responsive Web-Seiten, deren Layout automatisch an den Gerätetyp angepasst wird.

Einbetten in fester Größe wird verwendet, wenn der Viewer nach dem ersten Laden seine Größe nicht ändert. Diese Methode ist die beste Wahl für Web-Seiten mit statischem Layout.

Beim responsiven Einbetten wird davon ausgegangen, dass die Größe des Viewers zur Laufzeit entsprechend der Größenänderung seines Container-DIV geändert werden muss. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Web-Seite, die ein flexibles Layout verwendet.

Im responsiven Modus verhält sich der Viewer unterschiedlich, je nachdem, wie die Web-Seite die Größe ihres Container-DIVs bestimmt. Wenn die Web-Seite nur die Breite des Container-DIV festlegt und seine Höhe nicht eingeschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Auf diese Weise wird sichergestellt, dass das Asset perfekt in die Ansicht passt, ohne dass an den Seiten ein Abstand vorhanden ist. Dieser Anwendungsfall ist der häufigste bei Web-Seiten, die responsive Layout-Frameworks wie Bootstrap, Foundation usw. verwenden.

Wenn die Web-Seite jedoch sowohl die Breite als auch die Höhe für das Container-DIV des Viewers festlegt, füllt der Viewer diesen Bereich aus und folgt der vom Web-Seiten-Layout bereitgestellten Größe. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung an die Fenstergröße des Webbrowsers angepasst ist.

**Einbetten in fester Größe**

Sie können den Viewer wie folgt zu einer Web-Seite hinzufügen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Container-`DIV` definieren.
1. Festlegen der Viewer-Größe.
1. Viewer erstellen und initialisieren.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.

   Um einen Viewer zu erstellen, müssen Sie ein -Skript-Tag in der Kopfzeile von HTML hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL PanoramicViewer.js] einbeziehen. Die [!DNL PanoramicViewer.js]-Datei befindet sich im [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewers-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und er von derselben Domain bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Verweisen Sie auf Ihrer Seite nur auf die JavaScript-`include`-Datei des Haupt-Viewers. Verweisen Sie nicht auf zusätzliche JavaScript-Dateien im Web-Seiten-Code, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die HTML5 SDK `Utils.js`-Bibliothek, die vom Viewer aus `/s7viewers` Kontextpfad geladen wird (so genannte konsolidierte SDK-`include`). Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Runtime-Viewer-Bibliotheken vollständig von der Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Adobe speichert keine älteren Versionen der sekundären Viewer-`includes` auf dem Server.
>
>
>Wenn Sie also auf der Seite einen direkten Verweis auf eine sekundäre JavaScript-`include` einfügen, die vom Viewer verwendet wird, wird die Viewer-Funktionalität in Zukunft unterbrochen, wenn eine neue Produktversion bereitgestellt wird.

1. Definieren des Container-DIV.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres DIV-Element hinzu. Für das DIV-Element muss eine ID definiert sein, da diese ID später an die Viewer-API übergeben wird. Die Größe des DIV wird durch CSS angegeben.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute` festgelegt.


   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-DIV-Element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Festlegen der Viewer-Größe

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für `.s7panoramicviewer` CSS-Klasse der obersten Ebene in absoluten Einheiten deklarieren oder den Modifikator `stagesize` verwenden.

   Die Größe in CSS kann direkt auf der HTML-Seite oder in der benutzerdefinierten CSS-Viewer-Datei festgelegt werden, die später einem Viewer-Vorgabeneintrag in AOD zugewiesen oder explizit mit dem Stilbefehl übergeben wird. Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter Anpassen des Viewers . Nachfolgend finden Sie ein Beispiel für die Definition der statischen Viewer-Größe auf der HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` -Modifikator kann explizit mit dem Viewer-Initialisierungs-Code mit der params-Auflistung oder als API-Aufruf wie im Abschnitt Befehlsreferenz beschrieben übergeben werden, wie hier zu sehen:

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   Der CSS-basierte Ansatz wird empfohlen und wird in diesem Beispiel verwendet.

1. Viewer erstellen und initialisieren.

   Wenn Sie die obigen Schritte ausgeführt haben, erstellen Sie eine Instanz `s7viewers.PanoramicViewer` Klasse, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die `init(`)-Methode auf einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über ein Feld containerId verfügen, das den Namen der Viewer-Container-ID und des verschachtelten JSON-Parameterobjekts mit Konfigurationsparametern enthält, die vom Viewer unterstützt werden. In diesem Fall müssen für das Parameterobjekt mindestens die Bildbereitstellungs-URL als `serverUrl` und das anfängliche Asset als Asset-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzigen Codezeile erstellen und starten.

   Es ist wichtig, dass der Viewer-Container zum DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser verzögern die Erstellung von DOM bis zum Ende der Web-Seite. Um maximale Kompatibilität zu erzielen, rufen Sie die `init()`-Methode unmittelbar vor dem schließenden `BODY`-Tag oder im body-`onload()` auf.

   Gleichzeitig sollte das Container-Element noch nicht unbedingt Teil des Web-Seiten-Layouts sein. Beispielsweise kann sie mithilfe `display:none` ihr zugewiesenen Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Moment, an dem die Web-Seite das Container-Element wieder zum Layout zurückbringt. Wenn diese Aktion stattfindet, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()`-Methode. In diesem Beispiel wird davon ausgegangen, `panoramicViewer` die Viewer-Instanz, `s7viewer` der Name des Platzhalters `DIV`, [!DNL http://s7d1.scene7.com/is/image/] die Bildbereitstellungs-URL und [!DNL Scene7SharedAssets/PanoramicImage-Sample] das Asset ist.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, auf der der Panorama-Viewer mit einer festen Größe eingebettet ist:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**Responsives Design mit unbegrenzter Höhe**

Bei der responsiven Einbettung verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Container-DIVs des Viewers bestimmt. Nehmen wir für die Zwecke dieses Beispiels an, dass die Web-Seite dem Container-DIV des Viewers ermöglicht, 80 % der Fenstergröße des Webbrowsers zu übernehmen, wobei seine Höhe nicht beschränkt wird. Der Web-Seiten-HTML-Code könnte wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt der Einbettung mit fester Größe, mit dem einzigen Unterschied, dass Sie die Viewer-Größe nicht explizit definieren müssen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Definieren des Container-DIV.
1. Viewer erstellen und initialisieren.

Alle oben genannten Schritte sind dieselben wie bei der Einbettung in fester Größe. Container-DIV sollte zum vorhandenen „Inhaber“-DIV hinzugefügt werden. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Seitenverhältnis des Viewers mit dem Asset übereinstimmt.

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

Die folgende Beispielseite veranschaulicht eine praktischere Verwendung der responsiven Designeinbettung mit unbegrenzter Höhe:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demo-Speicherort](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Responsives Design Einbetten mit definierter Breite und Höhe**

Wenn ein responsives Design eingebettet wird und Breite und Höhe definiert sind, ist der Web-Seiten-Stil unterschiedlich. Er stellt dem `DIV` „Halter“ beide Größen zur Verfügung und zentriert ihn im Browser-Fenster. Außerdem legt die Web-Seite die Größe des `HTML`- und `BODY` auf 100 % fest:

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

Die übrigen Einbettungsschritte sind identisch mit responsiven Einbettungen mit unbegrenzter Höhe. Das daraus resultierende Beispiel ist

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**Einbetten mithilfe der Setter-basierten API**

Anstatt die JSON-basierte Initialisierung zu verwenden, ist es möglich, eine Setter-basierte API und einen Nicht-Args-Konstruktor zu verwenden. Mit dieser API übernimmt der Konstruktor keine Parameter und Konfigurationsparameter werden mithilfe von `setContainerId()`-, `setParam()`- und `setAsset()`-API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Einbettung fester Größe mit einer Setter-basierten API:

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
    width: 1024;
    height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
