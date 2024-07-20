---
title: Panoramabilder
description: HTML5 Panorama-Viewer ist ein Bild-Viewer, der ein Panoramabild anzeigt. Der Zweck dieses Betrachters besteht darin, ein kugelförmiges Panorama anzuzeigen, das auch als Panorama bezeichnet wird. Es unterstützt das automatische Schwenken und Schwenken durch gyroskopische Bewegung. Es wurde für Desktops und Mobilgeräte entwickelt. Der Virtual-Reality-Anzeigemodus ist auf Mobilgeräten verfügbar.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1924'
ht-degree: 0%

---

# Panorama{#panoramic}

HTML5 Panorama-Viewer ist ein Bild-Viewer, der ein Panoramabild anzeigt. Der Zweck dieses Betrachters besteht darin, ein kugelförmiges Panorama anzuzeigen, das auch als Panorama bezeichnet wird. Es unterstützt das automatische Schwenken und Schwenken durch gyroskopische Bewegung. Es wurde für Desktops und Mobilgeräte entwickelt. Der Virtual-Reality-Anzeigemodus ist auf Mobilgeräten verfügbar.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Viewer-Typ 514.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Verwenden des Panorama-Viewers {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panorama Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar, die vom Viewer zur Laufzeit heruntergeladen wurden. Der Satz von Hilfsdateien ist ein JavaScript-Include mit allen HTML5 Viewer SDK-Komponenten, die von diesem Viewer, Assets und CSS verwendet werden.
HTML5 Panorama-Viewer können sowohl im Popup-Modus mithilfe einer produktionsbereiten HTML-Seite, die mit IS-Viewern bereitgestellt wird, als auch im eingebetteten Modus verwendet werden, wo sie mithilfe der dokumentierten API in die Ziel-Web-Seite integriert wird.
Die Konfiguration und das Skinning ähneln der anderen HTML5-Viewer. Alle Skins können über benutzerdefiniertes CSS erstellt werden.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem HTML5-Panorama-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 Panorama Viewer unterstützt automatisches Schwenken und Navigieren durch Ziehen oder Gyroskopie.

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
   <td colname="col2"> <p>Auto-Schwenken und Ziehen zum Navigieren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Touch-Gerät </p> </td> 
   <td colname="col2"> <p>Standardmäßig können Sie durch Verschieben und Ziehen navigieren. Navigieren Sie im VR-Rendermodus durch gyroskopische Bewegung (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt sowohl die Touch-Eingabe als auch die Mauseingabe auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome-, Internet Explorer 11- und Edge-Webbrowser beschränkt.
Der Panorama-Viewer kann Panoramabilder im VR-Modus (Virtual Reality) rendern, indem er den Viewer angibt. Wenn &quot;vrrender&quot;aktiviert ist, wird ein Panoramabild in geteilten Bildschirmen angezeigt. Ein gängiges Nutzungsszenario wäre, das Bild in einem Mobiltelefon zu bedienen, das in einem Virtual-Reality-Headset montiert ist, und für jedes Auge separate Bilder bereitzustellen. Der Viewer reagiert auf die gyroskopische Bewegung des Kopfes und navigiert durch das Bild.

## Einbetten von HTML 5 Panorama-Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit. Wenn Sie diesen Link auswählen, wird der Viewer in einem separaten Browser-Fenster geöffnet. In anderen Fällen kann es erforderlich sein, den Viewer in die Hosting-Seite einzubetten. In letzterem Fall kann die Webseite ein statisches Layout aufweisen oder &quot;responsiv&quot;sein und auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt werden. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei Hauptbetriebsmodi: Popup, Einbettung fester Größe und responsives Einbetten.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Bereich des Browser-Fensters und passt sich an, falls die Größe des Browsers geändert oder die Geräteausrichtung geändert wird.

Dieser Modus wird am häufigsten für Mobilgeräte verwendet. Die Webseite lädt den Viewer mit dem JavaScript-Aufruf `window.open()`, der ordnungsgemäß konfigurierten HTML-Komponente oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Es heißt [!DNL PanoramicViewer.html] und befindet sich im Unterordner [!DNL html5/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

Die visuelle Anpassung kann durch Anwendung von benutzerdefiniertem CSS erreicht werden.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer im neuen Fenster öffnet:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Über Einbettungsmodus mit fester Größe und responsiven Einbettungsmodus**

Im eingebetteten Modus wird der Viewer der vorhandenen Web-Seite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Website-Immobilien.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Web-Seiten, auf denen das Layout automatisch an den Gerätetyp angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Methode eignet sich am besten für Webseiten mit statischem Layout.

Responsives Einbetten setzt voraus, dass die Größe des Viewers zur Laufzeit angepasst werden muss, wenn die Größe des Containers DIV geändert wird. Der häufigste Anwendungsfall ist das Hinzufügen des Viewers zu einer Webseite, die ein flexibles Layout verwendet.

Im responsiven Modus verhält sich der Viewer unterschiedlich, je nachdem, wie die Web-Seite die Größe des Container-DIVs ändert. Wenn die Web-Seite nur die Breite des Container-DIV festlegt und die Höhe nicht eingeschränkt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Methode stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten aufgefüllt werden. Dieser Anwendungsfall ist am häufigsten für Webseiten mit responsiven Layout-Frameworks wie Bootstrap, Foundation und so weiter.

Wenn die Web-Seite andernfalls sowohl die Breite als auch die Höhe für das Container-DIV des Viewers festlegt, füllt der Viewer diesen Bereich und folgt der Größe, die durch das Web-Seiten-Layout angegeben wird. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

**Einbettung fester Größe**

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie Folgendes ausführen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Containers `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL PanoramicViewer.js] einbeziehen. Die Datei [!DNL PanoramicViewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf dem die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Referenzieren Sie nur die JavaScript `include` -Hauptdatei des Viewers auf Ihrer Seite. Referenzieren Sie keine zusätzlichen JavaScript-Dateien im Webseitencode, die möglicherweise von der Viewer-Logik zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die vom Viewer aus dem Kontextpfad `/s7viewers` geladene HTML5 SDK `Utils.js`-Bibliothek (das so genannte konsolidierte SDK `include`). Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig durch die Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Adobe hält ältere Versionen des sekundären Viewers `includes` nicht auf dem Server.
>
>
>Infolgedessen wird die Viewer-Funktion bei der Bereitstellung einer neuen Produktversion durch direkte Referenzierung auf alle sekundären JavaScript `include`, die vom Viewer auf der Seite verwendet werden, in Zukunft beeinträchtigt.

1. Definieren des Container-DIV.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres DIV-Element hinzu. Die ID des DIV-Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird über CSS angegeben.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. die CSS-Eigenschaft `position` ist auf `relative` oder `absolute` festgelegt.


   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-DIV-Element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für die CSS-Klasse der obersten Ebene in absoluten Einheiten deklarieren oder den Modifikator `stagesize` verwenden.`.s7panoramicviewer`

   Die Größe in CSS kann direkt auf der HTML-Seite oder in der benutzerdefinierten Viewer-CSS-Datei festgelegt werden, die später einem Viewer-Vorgabendatensatz in AOD zugewiesen oder explizit mithilfe des Stilbefehls übergeben wird. Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter Anpassen des Viewers . Nachfolgend finden Sie ein Beispiel für die Definition der statischen Viewer-Größe auf der HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` -Modifikator kann explizit mit dem Viewer-Initialisierungscode mit der Parametersammlung oder als API-Aufruf übergeben werden, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben:

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   CSS-basierter Ansatz wird empfohlen und in diesem Beispiel verwendet.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.PanoramicViewer`, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode `init(`) auf einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld containerId verfügen, das den Namen der Viewer-Container-ID und das verschachtelte JSON-Objekt params mit Konfigurationsparametern enthält, die vom Viewer unterstützt werden. In diesem Fall muss für das params-Objekt mindestens die Image Serving-URL als `serverUrl`-Eigenschaft und das erste Asset als Asset-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder das body `onload()` -Ereignis auf.

   Gleichzeitig sollte das Containerelement nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit dem ihm zugewiesenen `display:none` -Stil ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Wenn diese Aktion auftritt, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. In diesem Beispiel wird davon ausgegangen, dass `panoramicViewer` die Viewer-Instanz, `s7viewer` der Name des Platzhalters `DIV`, [!DNL http://s7d1.scene7.com/is/image/] die Image Serving-URL und [!DNL Scene7SharedAssets/PanoramicImage-Sample] das Asset ist.

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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Panorama-Viewer mit einer festen Größe einbettet:

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

**Responsives Design, eingebettet in unbeschränkte Höhe**

Mit der responsiven Einbettung verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Container-DIV des Viewers bestimmt. Für die Zwecke dieses Beispiels nehmen wir an, dass die Web-Seite es dem Container-DIV des Viewers ermöglicht, 80 % der Fenstergröße des Webbrowsers zu erreichen, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite könnte wie folgt aussehen:

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

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Das Container-DIV sollte zum bestehenden DIV &quot;Inhaber&quot;hinzugefügt werden. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

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

Die folgende Beispielseite veranschaulicht die reale Verwendung responsiver Designs, die mit unbegrenzter Höhe eingebettet werden:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demostandort](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Responsives Design, das mit definierter Breite und Höhe eingebettet wird**

Wenn ein responsives Design mit definierter Breite und Höhe eingebettet ist, unterscheidet sich der Webseitenstil. Er stellt dem Inhaber `DIV` beide Größen bereit und zentriert sie im Browserfenster. Außerdem setzt die Webseite die Größe der Elemente `HTML` und `BODY` auf 100 %:

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

Die übrigen Einbettungsschritte sind mit der responsiven Einbettung mit uneingeschränkter Höhe identisch. Das resultierende Beispiel lautet

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

**Einbetten mit Setter-basierter API**

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Mit dieser API akzeptiert der Konstruktor keine Parameter und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Einbettung fester Größe in eine setter-basierte API:

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
