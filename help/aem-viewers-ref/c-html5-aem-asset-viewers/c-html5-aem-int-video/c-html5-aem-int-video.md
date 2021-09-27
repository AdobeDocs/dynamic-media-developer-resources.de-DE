---
title: Interaktives Video
description: Der Viewer für interaktive Videos ist ein Videoplayer, der Streaming- und progressive Videos wiedergibt, die im H.264-Format kodiert sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '2211'
ht-degree: 0%

---

# Interaktives Video{#interactive-video}

Der Viewer für interaktive Videos ist ein Videoplayer, der Streaming- und progressive Videos wiedergibt, die im H.264-Format kodiert sind.

Der Viewer zeigt außerdem interaktive Produktmuster neben dem Videoinhalt an. Es werden sowohl einzelne Video- als auch adaptive Videosets unterstützt. Es wurde für Desktop- und mobile Webbrowser entwickelt, die HTML5-Videos unterstützen. Der Viewer unterstützt optionale Untertitel, die über Videoinhalten, Videokapitelnavigation und Tools zur Freigabe in sozialen Netzwerken angezeigt werden. Dieser Viewer soll Ihnen bei der Implementierung eines Videos mit Shopping-Funktion helfen. Das heißt, Benutzer können ein mit einer bestimmten Videozeitregion verknüpftes Muster auswählen und zu einer Schnellansicht oder Produktdetailseite auf der Website des Kunden weitergeleitet werden.

Der Viewer-Typ ist 510.

## Demo-URLs {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

Und

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## Systemanforderungen {#section-b7270cc4290043399681dc504f043609}

Siehe [Systemanforderungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Verwenden des interaktiven Video-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der Viewer für interaktive Videos stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar, die vom Viewer zur Laufzeit heruntergeladen wurden. In allen Viewer-SDK-Komponenten, die von diesem Viewer, diesen Assets und CSS verwendet werden, ist ein einzelnes JavaScript enthalten.

Der interaktive Video-Viewer kann im Popup-Modus verwendet werden, indem eine produktionsbereite HTML-Seite mit Image Serving Viewers verwendet wird. Sie kann auch im eingebetteten Modus verwendet werden, wo sie mithilfe der dokumentierten API in die Targeting-Webseite integriert wird.

Die Konfiguration und das Skinning ähneln denen der anderen in diesem Handbuch beschriebenen Viewer. Die gesamte Skinnerung erfolgt über benutzerdefinierte CSS-Stylesheets (Cascading Style Sheets).

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem interaktiven Video-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der interaktive Video-Viewer bietet eine Reihe standardmäßiger Steuerelemente für die Videowiedergabe, z. B. eine Wiedergabe/Pause-Schaltfläche, einen Video-Scrubber, eine Videozeitblase, eine Anzeige für die Wiedergabe/Gesamtdauer, eine Lautstärkeregelung, eine Schaltfläche für den Vollbildmodus und einen Umschalter für Untertitel. Alle diese Steuerelemente werden in einer Steuerleiste direkt unter der Hauptansicht gruppiert.

Auf Touch-Geräten ist die Lautstärkeregelung in der Benutzeroberfläche ausgeblendet, da es nur möglich ist, die Lautstärke mithilfe der Hardwaretasten des Geräts zu steuern.

Wenn der Viewer im Popup-Modus ausgeführt wird, ist in der Benutzeroberfläche keine Vollbildschaltfläche verfügbar.

Der Viewer zeigt ein Bedienfeld mit interaktiven Farbfeldern rechts neben dem Videoanzeigebereich an. Die Liste der Farbfelder wird bei der Videowiedergabe automatisch weitergeleitet, sodass Farbfelder angezeigt werden, die dem aktuellen Videobereich entsprechen. Durch Klicken oder Tippen auf ein Muster wird eine Aktion Trigger, die während der Autorenzeit mit diesem Muster verknüpft war. Je nachdem, wie Sie es einrichten, kann der Trigger zu einer anderen Seite der Website umleiten. Alternativ kann es Produktinformationen zurück an die Webseitenlogik übergeben, was wiederum das Öffnen einer Schnellansicht Trigger, die zugehörige Produktinhalte anzeigt.

Es ist möglich, schnell durch den Videoinhalt zu navigieren, wenn das Videokapitel aktiviert ist. Videokapitel werden als Markierungen in der Video-Scrubber-Spur angezeigt und zeigen den Kapiteltitel und die Beschreibung beim Rollover (oder bei einem einzelnen Tippen auf Touch-Systeme) an. Der Kunde kann ein bestimmtes Kapitel &quot;suchen&quot;, indem er auf eine Kapitelmarke klickt oder auf eine Kapitelbeschreibungsblase tippt.

Der Viewer unterstützt auch verschiedene Tools zur Freigabe in Social Media. Sie sind als einzelne Schaltfläche in der Benutzeroberfläche verfügbar, die sich zu einer Freigabesymbolleiste erweitert, wenn der Benutzer darauf klickt oder tippt. Die Freigabesymbolleiste enthält ein Symbol für jeden unterstützten Freigabekanaltyp wie Facebook, Twitter, E-Mail-Freigabe, Einbettungscode-Freigabe und Linkfreigabe. Wenn die Tools für die Freigabe von E-Mails, die Einbettung von Freigabe oder die Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Formular für die Dateneingabe an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer von einem Social-Media-Dienst zu einem standardmäßigen Dialogfeld für die Freigabe um. Außerdem wird die Videowiedergabe automatisch angehalten, wenn ein Freigabe-Tool aktiviert wird. Die Freigabe-Tools sind aufgrund der Sicherheitseinschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

Auf den Viewer kann vollständig über die Tastatur zugegriffen werden. Siehe [Barrierefreiheit und Navigation über die Tastatur](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des interaktiven Video-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Der interaktive Video-Viewer ist in die Hosting-Seite eingebettet. Eine solche Webseite kann ein statisches Layout aufweisen oder &quot;responsiv&quot;sein und auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt werden.

Um diese Anforderungen zu erfüllen, unterstützt der Viewer zwei primäre Betriebsmodi: Einbetten in feste Größe und responsives Einbetten.

**Über den Einbettungsmodus mit fester Größe und den Einbettungsmodus für responsives Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Seiten, auf denen das Layout automatisch an den Gerätetyp angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Funktion eignet sich am besten für Webseiten mit statischem Layout.

Responsive Designeinbettung setzt voraus, dass die Größe des Viewers zur Laufzeit geändert werden muss, wenn die Größe des Containers geändert wird `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für responsive Designs verhält sich der Viewer unterschiedlich, je nachdem, wie die Größe der Web-Seite für den Container `DIV` angepasst wird. Wenn die Web-Seite nur die Breite des Containers `DIV` festlegt und dabei die Höhe unbegrenzt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten einen Abstand aufweisen. Dieser Anwendungsfall ist der häufigste bei Webseiten, die responsive Webdesign-Layoutrahmen wie Bootstrap und Foundation verwenden.

Andernfalls füllt der Viewer, wenn die Web-Seite die Breite und Höhe für den Container des Viewers `DIV` festlegt, nur diesen Bereich und folgt der Größe, die das Layout der Web-Seite bietet. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

**Einbettung fester Größe**

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie Folgendes ausführen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Containers `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL InterativeVideoViewer.js] angeben. Die Datei [!DNL InteractiveVideoViewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Verweisen Sie auf der Seite nur auf die JavaScript-Datei `include` des Haupt-Viewers. Referenzieren Sie keine zusätzlichen JavaScript-Dateien im Webseitencode, die möglicherweise von der Viewer-Logik zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die HTML5-SDK-Bibliothek `Utils.js` , die vom Viewer aus dem Kontextpfad `/s7viewers` geladen wird (so genanntes konsolidiertes SDK `include`). Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig von der Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Adobe behält ältere Versionen des sekundären Viewers `includes` nicht auf dem Server bei.
>
>
>Infolgedessen wird die Viewer-Funktion bei der Bereitstellung einer neuen Produktversion zukünftig beeinträchtigt, wenn ein direkter Verweis auf ein sekundäres JavaScript `include` gesetzt wird, das vom Viewer auf der Seite verwendet wird.

1. Definieren des Containers `DIV`.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres `DIV` -Element hinzu. Die Kennung des Elements `DIV` muss definiert sein, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird über CSS angegeben.

   Der Platzhalter `DIV` ist ein positioniertes Element, d. h. die CSS-Eigenschaft `position` ist auf `relative` oder `absolute` festgelegt.

   Damit die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert, dürfen keine anderen Elemente im DOM vorhanden sein, die eine höhere Stapelreihenfolge aufweisen als Ihr Platzhalter `DIV`.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalterelement `DIV` :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für die CSS-Klasse der obersten Ebene `.s7interactivevideoviewer` in absoluten Einheiten deklarieren oder den Modifikator `stagesize` verwenden.

   Sie können die Größe in CSS direkt auf die HTML-Seite setzen. Alternativ können Sie sie in eine benutzerdefinierte Viewer-CSS-Datei einfügen, die später in Adobe Experience Manager Assets On-Demand einem Viewer-Vorgabendatensatz zugewiesen oder explizit mit dem Befehl `style` übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des interaktiven Video-Viewers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf der HTML-Seite:

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Sie können den Modifikator `stagesize` im Viewer-Vorgabeneintrag in Experience Manager Assets - On-Demand festlegen. Oder Sie können sie explizit mit dem Viewer-Initialisierungscode mit der Sammlung `params` oder als API-Aufruf übergeben, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben:

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.InteractiveVideoViewer`, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode `init()` in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID enthält und das verschachtelte `params` JSON-Objekt mit Konfigurationsparametern enthält, die vom Viewer unterstützt werden.

   In diesem Fall muss für das `params`-Objekt mindestens die Image-Serving-URL als `serverUrl`-Eigenschaft und das erste Asset als `asset`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile, einer Videoserver-URL, die als Eigenschaft `videoserverurl` übergeben wird, einem anfänglichen Asset als Parameter `asset` und interaktiven Daten als Eigenschaft `interactivedata` erstellen und starten. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()`-Methode direkt vor dem schließenden `BODY`-Tag oder das `onload()`-Ereignis im Hauptteil auf.

   Gleichzeitig ist das Containerelement noch nicht unbedingt Teil des Webseitenlayouts. Sie kann beispielsweise mit dem `display:none`-Stil ausgeblendet werden, der ihm zugewiesen ist. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Dadurch wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()`-Methode. Im Beispiel wird von Folgendem ausgegangen:

   * Die Viewer-Instanz ist `interactiveVideoViewer`.
   * Der Name des Platzhalters `DIV` ist `s7viewer`.
   * Die Image Serving-URL ist `https://aodmarketingna.assetsadobe.com/is/image/`.
   * Die Videoserver-URL lautet `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * Die Inhalts-URL lautet `https://aodmarketingna.assetsadobe.com/`.
   * Das Asset ist `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * Die interaktiven Daten sind `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den interaktiven Video-Viewer mit einer festen Größe einbettet:

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

**Responsives Design mit uneingeschränkter Höhe**

Bei der Einbettung responsiver Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers `DIV` vorgibt. Für das folgende Beispiel nehmen Sie an, dass die Web-Seite es dem Container des Viewers `DIV` ermöglicht, 40 % der Fenstergröße des Webbrowsers zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten zum Einbetten fester Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Fügen Sie das Container-DIV zum vorhandenen DIV `"holder"` hinzu. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

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

Die folgende Beispielseite zeigt die reale Nutzung responsiver Designs, die mit unbegrenzter Höhe eingebettet werden:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demostandort](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Responsive Einbettung mit definierter Breite und Höhe**

Wenn eine responsive Einbettung mit definierter Breite und Höhe erfolgt, unterscheidet sich der Webseitenstil. Es bietet beide Größen für den DIV `"holder"` und zentriert ihn im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und `BODY` auf 100 Prozent.

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

Die übrigen Schritte zum Einbetten sind mit den Schritten identisch, die für das responsive Einbetten mit uneingeschränkter Höhe verwendet werden. Das folgende Beispiel zeigt:

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

**Einbetten mit Setter-basierter API**

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Die Verwendung dieses API-Konstruktors akzeptiert keine Parameter und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Verwendung der Einbettung mit fester Größe in die setter-basierte API:

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
