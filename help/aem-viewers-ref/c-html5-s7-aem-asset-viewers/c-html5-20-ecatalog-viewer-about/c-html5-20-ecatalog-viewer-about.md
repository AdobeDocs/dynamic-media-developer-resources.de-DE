---
title: eCatalog
description: eCatalog Viewer ist ein Katalog-Viewer, der elektronische Broschüren auf breiter Basis oder seitenweise anzeigt. Mit dem eCatalog können Benutzer mithilfe zusätzlicher Elemente der Benutzeroberfläche oder des dedizierten Miniaturansichtsmodus durch den Katalog navigieren. Benutzer können auch auf jeder Seite heranzoomen, um mehr Details zu erhalten.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 8e243fa5-e375-41ce-8b49-2571023130c1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '2160'
ht-degree: 0%

---

# eCatalog{#ecatalog}

eCatalog Viewer ist ein Katalog-Viewer, der elektronische Broschüren auf breiter Basis oder seitenweise anzeigt. Mit dem eCatalog können Benutzer mithilfe zusätzlicher Elemente der Benutzeroberfläche oder des dedizierten Miniaturansichtsmodus durch den Katalog navigieren. Benutzer können auch auf jeder Seite heranzoomen, um mehr Details zu erhalten.

>[!NOTE]
>
>Bilder, die Image Rendering (IR) oder benutzergenerierte Inhalte (UGC) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ 507.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Dieser Viewer arbeitet mit E-Katalogen und unterstützt optionale Imagemaps und Tools zur Freigabe in sozialen Netzwerken. Es verfügt über Zoom-Tools, Katalognavigationswerkzeuge, Vollbildunterstützung, Miniaturen und eine optionale Schließen-Schaltfläche. Der Viewer unterstützt auch Social-Sharing-Tools, Drucken, Herunterladen und Favoriten. Es wurde für Desktops und Mobilgeräte entwickelt.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## Verwenden des eCatalog-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der eCatalog-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar (ein einzelnes JavaScript-Include mit allen Viewer-SDK-Komponenten, die von diesem Viewer, Assets und CSS verwendet werden), die vom Viewer zur Laufzeit heruntergeladen wurden.

Sie können den E-Katalog-Viewer im Popup-Modus verwenden, indem Sie eine produktionsbereite HTML-Seite verwenden, die mit IS-Viewern bereitgestellt wird, oder im eingebetteten Modus, auf der er mithilfe der dokumentierten API in die Ziel-Web-Seite integriert wird.

Die Konfiguration und die Skinning-Funktion ähneln denen der anderen Viewer. Alle Skins werden über benutzerdefiniertes CSS erstellt.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem E-Katalog-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der E-Katalog-Viewer unterstützt die folgenden Berührungsgesten, die in anderen Mobile Apps häufig vorkommen.

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
   <td colname="col2"> <p> Wählt neue Miniaturansichten in Farbfeldern aus. </p> </td> 
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
   <td colname="col2"> <p> Scrollt durch die Liste der Katalogseiten, wenn eine Folienframe-Transition verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Wischen oder Klick </p> </td> 
   <td colname="col2"> <p>Wenn das Bild sich im Status "Zurücksetzen"befindet, führt es einen nativen Bildlauf durch. </p> <p>Wenn Miniaturansichten aktiv sind, wird ein Bildlauf in der Liste der Miniaturansichten durchgeführt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Es ist möglich, einen realistischen Animationseffekt für Seitenumbrüche für die Navigation zwischen Katalogseiten zu aktivieren. In solchen Fällen kann ein Benutzer eine Seitenecke halten, ziehen und die Seite spiegeln.

Dieser Viewer unterstützt auch Touch-Eingabe- und Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome-, Internet Explorer 11- und Edge-Webbrowser beschränkt.

Auf diesen Viewer kann wie unter [Tastaturzugriff und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Tools zur Freigabe in Social Media mit dem E-Katalog-Viewer {#section-eb575084a99647c3a9591f439f40b412}

Der E-Katalog-Viewer unterstützt Tools zur Freigabe in sozialen Netzwerken. Sie sind als Schaltfläche in der Hauptsteuerungsleiste verfügbar, die sich zu einer Freigabe-Symbolleiste erweitert, wenn ein Benutzer darauf klickt oder tippt.

Die Freigabe-Symbolleiste enthält Symbole für jeden unterstützten Freigabekanaltyp, darunter Facebook, Twitter, E-Mail-Freigabe, Einbettungscode-Freigabe und Linkfreigabe. Wenn die Tools für die Freigabe von E-Mails, die Einbettung von Freigabe oder die Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Formular für die Dateneingabe an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer von einem Social-Dienst zu einem standardmäßigen Dialogfeld für die Freigabe um. Die Freigabe-Tools sind aufgrund der Sicherheitseinschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

## Einbetten des E-Katalog-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, der, wenn ausgewählt, den Viewer in einem separaten Browserfenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt in die Hosting-Seite einzubetten. In letzterem Fall kann die Webseite ein statisches Seitenlayout aufweisen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung fester Größe und Einbettung responsiver Designs.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Bereich des Browser-Fensters und passt sich an, falls die Größe des Browsers geändert wird oder die Ausrichtung eines Mobilgeräts geändert wird.

Der Pop-up-Modus ist der häufigste für Mobilgeräte. Die Webseite lädt den Viewer mit `window.open()` JavaScript-Aufruf, ordnungsgemäß konfiguriert `A` HTML-Element oder eine andere geeignete Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. In diesem Fall wird sie [!DNL eCatalogViewer.html] und sich innerhalb der [!DNL html5/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erreichen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```
<a href="https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**Über den Einbettungsmodus mit fester Größe und den Einbettungsmodus für responsives Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Seiten, auf denen das Layout automatisch an den Gerätetyp angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Methode eignet sich am besten für Webseiten mit statischem Layout.

Responsives Design-Einbetten setzt voraus, dass die Größe des Viewers zur Laufzeit geändert werden muss, wenn die Größe des Containers geändert wird `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für responsives Design verhält sich der Viewer unterschiedlich, je nachdem, wie die Web-Seite den Container dimensioniert `DIV`. Wenn die Webseite nur die Breite des Containers festlegt `DIV`Wenn die Höhe nicht eingeschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten einen Abstand aufweisen. Dieser Anwendungsfall ist der häufigste bei Webseiten, die responsive Layout-Frameworks wie Bootstrap und Foundation verwenden.

Andernfalls, wenn die Webseite sowohl die Breite als auch die Höhe für den Container des Viewers festlegt `DIV`, füllt der Viewer nur diesen Bereich und folgt der Größe, die das Layout der Webseite bietet. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

**Einbettung fester Größe**

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie wie folgt vorgehen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Container-DIV.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL eCatalogViewer.js]. Die [!DNL eCatalogViewer.js] befindet sich unter der [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf dem die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
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

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für `.s7ecatalogviewer` CSS-Klasse der obersten Ebene in absoluten Einheiten oder durch Verwendung von `stagesize` -Modifikator.

   Sie können die Größenanpassung in CSS direkt auf die HTML-Seite setzen. Oder fügen Sie die Größe in eine benutzerdefinierte Viewer-CSS-Datei ein, die später in Dynamic Media Classic einem Viewer-Vorgabendatensatz zugewiesen oder explizit mithilfe eines Stilbefehls übergeben wird.

   Siehe [Anpassen des E-Katalog-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) Weitere Informationen zum Formatieren des Viewers mit CSS.

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf der HTML-Seite:

   ```
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können die `stagesize` -Modifikator im Viewer-Vorgabendatensatz in Dynamic Media Classic. Oder Sie können sie explizit mit dem Viewer-Initialisierungscode mit `params` -Sammlung oder als API-Aufruf, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben, wie folgt:

   ```
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz von `s7viewers.eCatalogViewer` -Klasse, übergeben Sie alle Konfigurationsinformationen an ihren Konstruktor und rufen Sie `init()` -Methode in einer Viewer-Instanz verwenden. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt hat mindestens die `containerId` -Feld, das den Namen der Viewer-Container-ID und verschachtelt enthält `params` JSON-Objekt mit Konfigurationsparametern, die vom Viewer unterstützt werden. In diesem Fall wird die `params` -Objekt muss mindestens über die Image Serving-URL verfügen, die als `serverUrl` -Eigenschaft und das erste Asset als `asset` Parameter. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Um die maximale Kompatibilität sicherzustellen, rufen Sie jedoch die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder im Hauptteil `onload()` -Ereignis.

   Gleichzeitig sollte das Containerelement nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit `display:none` Stil zugewiesen. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Wenn diese Aktion auftritt, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. Das Beispiel geht von `eCatalogViewer` ist die Viewer-Instanz; `s7viewer` ist der Name des Platzhalters `DIV`; `https://s7d1.scene7.com/is/image/` ist die Image Serving-URL und `Viewers/Pluralist` ist das Asset:

   ```
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den E-Katalog-Viewer mit einer festen Größe einbettet:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsives Design mit uneingeschränkter Höhe**

Mit responsiver Designeinbettung verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers bestimmt `DIV`. Für die Zwecke dieses Beispiels nehmen Sie an, dass die Webseite den Container des Viewers zulässt `DIV` , um 40 % der Fenstergröße des Webbrowsers zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der resultierende HTML-Code der Webseite sieht wie folgt aus:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt der Einbettung in feste Größe, wobei der einzige Unterschied darin besteht, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Container hinzufügen `DIV` an den bestehenden &quot;Inhaber&quot; `DIV`. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Die folgende Beispielseite zeigt reale Anwendungsfälle responsiven Designs, die mit unbegrenzter Höhe eingebettet werden:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Flexible Größeneinbettung mit definierter Breite und Höhe**

Bei der Einbettung in flexibler Größe mit definierter Breite und Höhe unterscheidet sich der Webseitenstil. Das heißt, es stellt dem Inhaber beide Größen zur Verfügung. `DIV` und zentriert sie im Browserfenster. Außerdem legt die Webseite die Größe der `HTML` und `BODY` -Element auf 100 %:

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

Die restlichen Einbettungsschritte sind mit dem responsiven Design identisch, das mit uneingeschränkter Höhe eingebettet wird. Das folgende Beispiel zeigt:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Einbetten mit Setter-basierter API**

Statt die JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Mit diesem API-Konstruktor nehmen keine Parameter auf und Konfigurationsparameter werden mit `setContainerId()`, `setParam()`und `setAsset()` API-Methoden mit separaten JavaScript-Aufrufen.

Das folgende Beispiel zeigt die Einbettung von fester Größe in eine setter-basierte API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogViewer = new s7viewers.eCatalogViewer(); 
eCatalogViewer.setContainerId("s7viewer"); 
eCatalogViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```
