---
description: Der Interactive Video Viewer ist ein Videoplayer, der Streaming- und Progressiv-Videos im H.264-Format wiedergibt.
seo-description: Der Interactive Video Viewer ist ein Videoplayer, der Streaming- und Progressiv-Videos im H.264-Format wiedergibt.
seo-title: Interaktives Video
solution: Experience Manager
title: Interaktives Video
topic: Dynamic media
uuid: 116c6b40-2490-4f1a-9c76-e06082069cc8
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2243'
ht-degree: 0%

---


# Interaktives Video{#interactive-video}

Der Interactive Video Viewer ist ein Videoplayer, der Streaming- und Progressiv-Videos im H.264-Format wiedergibt.

Der Viewer zeigt auch interaktive Produktfelder neben dem Videoinhalt an. Es werden sowohl einzelne Video- als auch adaptive Videosets unterstützt. Es wurde für die Verwendung mit Desktop- und mobilen Webbrowsern entwickelt, die HTML5-Videos unterstützen. Der Viewer unterstützt optionale Untertitel, die über Videoinhalten, Videokapitelnavigation und Social Sharing-Werkzeugen angezeigt werden. Dieser Viewer soll Ihnen bei der Implementierung eines &quot;Shoppable Video&quot;-Erlebnisses helfen. Das heißt, Benutzer können ein mit einem bestimmten Videozeitbereich verknüpftes Muster auswählen und zu einer Schnellseite oder Produktdetailseite auf der Website des Kunden umgeleitet werden.

Der Viewer-Typ ist 510.

## Demo-URLs {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

und

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## Systemanforderungen {#section-b7270cc4290043399681dc504f043609}

Siehe [Systemanforderungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Verwenden des interaktiven Video-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der interaktive Video-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar (ein einzelnes JavaScript enthält alle Viewer-SDK-Komponenten, die von diesem bestimmten Viewer verwendet werden, Assets und CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Der interaktive Video-Viewer kann im Popup-Modus verwendet werden, indem eine produktionsfertige HTML-Seite mit Image Serving Viewern verwendet wird. Es kann auch im eingebetteten Modus verwendet werden, wo es mithilfe der dokumentierten API in die zielgerichtete Webseite integriert wird.

Konfiguration und Skin ähneln denen der anderen in diesem Handbuch beschriebenen Viewer. Alle Skins werden mithilfe von CSS (Custom Cascading Style Sheets) realisiert.

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem interaktiven Video-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der interaktive Video-Viewer bietet eine Reihe standardmäßiger Steuerelemente der Benutzeroberfläche für die Videowiedergabe, wie z. B. die Schaltflächen &quot;Abspielen/Anhalten&quot;, &quot;Video-Navigationsleisten&quot;, &quot;Video-Zeitblase&quot;, &quot;Wiedergabedauer/Gesamtzeit-Indikator&quot;, &quot;Lautstärkeregler&quot;, &quot;Vollbildschaltfläche&quot;und &quot;Bildunterschrift&quot;. Alle diese Steuerelemente werden in einer Steuerleiste direkt unter der Haupt-Ansicht gruppiert.

Beachten Sie, dass auf Touch-Geräten die Lautstärkeregelung in der Benutzeroberfläche ausgeblendet ist, da die Lautstärke nur über die Hardwareschaltflächen des Geräts gesteuert werden kann.

Wenn der Viewer im Popupmodus ausgeführt wird, ist in der Benutzeroberfläche keine Vollbildschaltfläche verfügbar.

Der Viewer zeigt ein Bedienfeld mit interaktiven Farbfeldern rechts neben dem Videoanzeigebereich an. Die Liste der Farbfelder wird bei der Videowiedergabe automatisch angepasst, sodass die dem aktuellen Videobereich entsprechenden Farbfelder angezeigt werden. Durch Klicken oder Tippen auf ein Farbfeld wird eine Aktion ausgelöst, die während der Autorenzeit mit diesem Farbfeld verknüpft wurde. Je nachdem, wie Sie ihn einrichten, kann der Auslöser zu einer anderen Seite der Website umleiten oder Produktinformationen an die Webseitenlogik weiterleiten, was wiederum das Öffnen einer Schnellseite auslösen kann, die den zugehörigen Produktinhalt anzeigt.

Es ist möglich, schnell durch den Videoinhalt zu navigieren, wenn das Videochaptern aktiviert ist. Videokapitel werden als Markierungen in der Videobildschirmspur angezeigt und zeigen den Kapiteltitel und die Beschreibung beim Rollover (oder bei einem einzigen Tippen auf Touch-Systemen) an. Der Kunde kann zu einem bestimmten Kapitel &quot;suchen&quot;, indem er auf eine Kapitelmarke klickt oder auf eine Kapitelbeschreibungsblase tippt.

Der Viewer unterstützt außerdem eine Reihe von Social Media-Sharing-Werkzeugen. Sie stehen als eine einzige Schaltfläche in der Benutzeroberfläche zur Verfügung, die durch Klicken oder Tippen auf eine Freigabebeschaltfläche in eine Freigabebeschaltfläche umgewandelt wird. Die Freigabe-Symbolleiste enthält ein Symbol für jeden unterstützten Freigabetyp, z. B. Facebook, Twitter, E-Mail-Freigabe, Einbettungscode-Freigabe und Linkfreigabe. Wenn die Tools für die Freigabe per E-Mail, die Einbettung von Teilen oder die Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Dateneingabeformular an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer über einen Social Media-Dienst zu einem Standardfreigabedialogfeld um. Wenn ein Freigabe-Tool aktiviert ist, wird die Videowiedergabe automatisch angehalten. Die Freigabe von Werkzeugen ist im Vollbildmodus aufgrund von Webbrowser-Sicherheitsbeschränkungen nicht verfügbar.

Der Viewer kann vollständig über die Tastatur aufgerufen werden. Siehe [Barrierefreiheit und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)über die Tastatur.

## Einbetten des interaktiven Video-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Der interaktive Video-Viewer ist so konzipiert, dass er in die Hostingseite eingebettet wird. Eine solche Webseite kann ein statisches Layout haben oder &quot;reaktionsfähig&quot;sein und auf verschiedenen Geräten oder für verschiedene Fenstergrößen des Browsers unterschiedlich angezeigt werden.

Um diese Anforderungen zu erfüllen, unterstützt der Viewer zwei primäre Betriebsmodi: Einbettung in fester Größe und Einbettung in responsiv.

**Einbettungsmodus mit fester Größe und Einbettungsmodus für reaktionsfähiges Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer zusammenhängen. Der Viewer belegt normalerweise nur einen Teil der Immobilie einer Webseite.

Die wichtigsten Anwendungsfälle sind Webseiten, die auf Desktop- oder Tablet-Geräte ausgerichtet sind, sowie reaktionsfähige Seiten, die das Layout automatisch an den Gerätetyp anpassen.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Dies ist die beste Wahl für Webseiten mit einem statischen Layout.

Bei der responsiven Design-Einbettung wird davon ausgegangen, dass der Viewer die Größe zur Laufzeit ändern muss, je nach Größenänderung des Containers `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für reaktionsfähiges Design verhält sich der Viewer je nach Größe des Containers der Webseite unterschiedlich `DIV`. Wenn die Webseite nur die Breite des Containers festlegt `DIV`und dabei die Höhe unbegrenzt bleibt, wählt der Viewer die Höhe automatisch entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass es an den Seiten aufgefüllt werden muss. Dieser Anwendungsfall ist der häufigste Fall für Webseiten mit reaktionsfähigen Webdesign-Layoutrahmen wie Bootstrap, Foundation usw.

Andernfalls füllt der Viewer, wenn die Webseite sowohl die Breite als auch die Höhe des Containers des Viewers festlegt `DIV`, nur diesen Bereich aus und entspricht der Größe des Webseitenlayouts. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung je nach Webbrowser-Fenstergröße angepasst wird.

**Einbettung fester Größe**

Der Viewer wird wie folgt zu einer Webseite hinzugefügt:

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Containers `DIV`.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite

   Zum Erstellen eines Viewers müssen Sie im HTML-Kopf ein Skript-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL InterativeVideoViewer.js]dies berücksichtigen. Die [!DNL InteractiveVideoViewer.js] Datei befindet sich im [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Sie sollten nur auf die JavaScript- `include` Hauptdatei des Viewers auf Ihrer Seite verweisen. Sie sollten keine weiteren JavaScript-Dateien im Webseitencode referenzieren, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die vom Viewer aus dem `Utils.js` Kontextpfad (so genanntes konsolidiertes SDK) geladene HTML5 SDK- `/s7viewers` Bibliothek `include`. Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig durch die Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Ältere Versionen des sekundären Viewers werden von Adobe nicht `includes` auf dem Server gespeichert.
>
>
>Infolgedessen wird die Viewer-Funktion bei der Bereitstellung einer neuen Produktversion durch direkte Verweise auf sekundäres JavaScript, das vom Viewer auf der Seite `include` verwendet wird, in Zukunft unterbrochen.

1. Definieren des Containers `DIV`.

   Hinzufügen Sie ein leeres `DIV` Element auf der Seite, auf der der Viewer angezeigt werden soll. Die ID des `DIV` Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird durch CSS festgelegt.

   Der Platzhalter `DIV` ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute`eingestellt.

   Damit die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert, müssen Sie sicherstellen, dass keine anderen Elemente im DOM eine höhere Stapelreihenfolge aufweisen als Ihr Platzhalter `DIV`.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalterelement `DIV` :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Einstellen der Viewer-Größe

   Sie können die statische Größe des Viewers festlegen, indem Sie ihn entweder für die CSS-Klasse der `.s7interactivevideoviewer` obersten Ebene in absoluten Einheiten deklarieren oder einen `stagesize` Modifikator verwenden.

   Sie können die Größe in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festlegen, die später einem Viewer-Vorgabendatensatz in AEM Assets zugewiesen wird - On-Demand oder explizit mit `style` einem Befehl weitergegeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des interaktiven Video-Viewers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Im Folgenden finden Sie ein Beispiel zum Definieren einer statischen Viewer-Größe auf der HTML-Seite:

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Sie können den `stagesize` Modifikator im Viewer-Vorgabendatensatz in AEM Assets einstellen - On-Demand. Sie können sie auch explizit mit dem Viewer-Initialisierungscode mit `params` Collection oder als API-Aufruf, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben, übergeben. Beispiel:

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der `s7viewers.InteractiveVideoViewer` Klasse, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode für eine Viewer-Instanz auf `init()` . Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über ein `containerId` Feld verfügen, das den Namen der Viewer-Container-ID und das verschachtelte `params` JSON-Objekt mit vom Viewer unterstützten Konfigurationsparametern enthält.

   In diesem Fall muss für das `params` Objekt mindestens die Image Serving-URL als `serverUrl` -Eigenschaft und das ursprüngliche Asset als `asset` -Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile, einer Videoserver-URL, die als `videoserverurl` Eigenschaft übergeben wird, einem anfänglichen Asset als `asset` Parameter und interaktiven Daten als `interactivedata` -Eigenschaft erstellen und Beginn erstellen. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und Beginn erstellen.

   Es ist wichtig, dass der Viewer-Container dem DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser zögern die Erstellung von DOM bis zum Ende der Webseite. Um eine maximale Kompatibilität zu gewährleisten, rufen Sie die `init()` Methode direkt vor dem schließenden `BODY` Tag oder im Body- `onload()` Ereignis auf.

   Gleichzeitig sollte das Container-Element nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mithilfe des ihr zugewiesenen `display:none` Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. Dadurch wird der Ladevorgang des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel zum Erstellen einer Viewer-Instanz, bei der die notwendigen Mindestkonfigurationsoptionen an den Konstruktor übergeben und die `init()` Methode aufgerufen werden. Das Beispiel geht von Folgendem aus:

   * Die Viewer-Instanz ist `interactiveVideoViewer`vorhanden.
   * Der Name des Platzhalters `DIV` lautet `s7viewer`.
   * Die Image Serving-URL lautet `https://aodmarketingna.assetsadobe.com/is/image/`.
   * Die URL des Videoservers lautet `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * Die Inhalts-URL lautet `https://aodmarketingna.assetsadobe.com/`.
   * Das Asset ist `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * Die interaktiven Daten werden `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`angezeigt.

   ```
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, die den interaktiven Video-Viewer mit einer festen Größe einbettet:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsive Design-Einbettung mit unbeschränkter Höhe**

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten zum Einbetten in feste Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers

Alle oben genannten Schritte sind identisch mit denen der Einbettung in fester Größe. Hinzufügen den Container DIV an das bestehende `"holder"` DIV. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Die folgende Beispielseite zeigt die aktuelleren Einsatzmöglichkeiten von reaktionsfähigem Design-Einbettung mit uneingeschränkter Höhe:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- OLD DEMO LOCATION-KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Responsive Einbettung mit definierter Breite und Höhe**

Bei responsiver Einbettung mit definierter Breite und Höhe ist der Webseitenstil anders. Es bietet beide Größen für das `"holder"` DIV und zentriert es im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und des `BODY` Elements auf 100 Prozent.

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

Die übrigen Einbettungsschritte sind identisch mit den Schritten, die für eine reaktionsfähige Einbettung mit uneingeschränkter Höhe verwendet werden. Das resultierende Beispiel lautet:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Einbetten mithilfe der Setter-basierten API**

Anstatt JSON-basierte Initialisierung zu verwenden, ist es möglich, set-basierte API- und no-args-Konstruktoren zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit `setContainerId()`-, `setParam()`- und `setAsset()` -API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Im folgenden Beispiel wird die Einbettung in feste Größe mit der setter-basierten API veranschaulicht:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```

