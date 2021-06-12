---
description: Der Video-Viewer ist ein Videoplayer, der Streaming- und progressive Videos wiedergibt, die im H.264-Format kodiert sind. Es wird von Dynamic Media Classic oder AEM Dynamic Media bereitgestellt.
keywords: responsiv
solution: Experience Manager
title: Video
feature: Dynamic Media Classic,Viewer,SDK/API,Video
role: Developer,Business Practitioner
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '2388'
ht-degree: 0%

---

# Video{#video}

Der Video-Viewer ist ein Videoplayer, der Streaming- und progressive Videos wiedergibt, die im H.264-Format kodiert sind. Es wird von Dynamic Media Classic oder AEM Dynamic Media bereitgestellt.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Es werden sowohl einzelne Video- als auch adaptive Videosets unterstützt. Darüber hinaus unterstützt der Viewer die Arbeit mit progressiven Video- und HLS-Streams, die auf externen Standorten gehostet werden. Es wurde für Desktop- und mobile Webbrowser entwickelt, die HTML5-Videos unterstützen. Dieser Viewer unterstützt auch optionale Untertitel, die über Videoinhalten, Videokapitelnavigation und Tools zur Freigabe in sozialen Medien angezeigt werden.

Der Video-Viewer verwendet die HTML5-Streaming-Videowiedergabe im HLS-Format in seiner Standardkonfiguration, wenn das zugrunde liegende System dies unterstützt. Auf Systemen, die HTML5-Streaming nicht unterstützen, greift der Viewer auf die progressive HTML5-Videobereitstellung zurück.

Viewer-Typ 506.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Verwenden des Video-Viewers {#section-f21ac23d3f6449ad9765588d69584772}

Der Video-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar - ein einzelnes JavaScript-Include mit allen Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, sowie Assets und CSS, die vom Viewer zur Laufzeit heruntergeladen werden.

Sie können den Video-Viewer im Popup-Modus verwenden, indem Sie eine produktionsbereite HTML-Seite verwenden, die mit IS-Viewern bereitgestellt wird. Alternativ können Sie den Viewer im eingebetteten Modus verwenden, wo er mithilfe der dokumentierten API in eine Ziel-Web-Seite integriert wird.

Die Aufgabe, den Viewer zu konfigurieren und zu skizzieren, ähnelt anderen Viewern. Die gesamte Skinning-Funktion wird über benutzerdefiniertes CSS erreicht.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem Video-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Der Video-Viewer bietet eine Reihe von standardmäßigen Steuerelementen der Benutzeroberfläche für die Videowiedergabe, wie z. B. eine Wiedergabe-/Pausenschaltfläche, Video-Scrubber-Videozeitblase, Anzeige der Wiedergabezeit/Gesamtdauer, Lautstärkeregler, Schaltfläche im Vollbildmodus und Umschalter für Untertitel. Alle diese Steuerelemente sind in einer Steuerleiste am unteren Rand der Viewer-Benutzeroberfläche gruppiert.

Auf Touch-Geräten ist die Lautstärkeregelung in der Benutzeroberfläche ausgeblendet, da die Lautstärke nur über die Hardwaretasten gesteuert werden kann.

Wenn der Viewer im Popup-Modus ausgeführt wird, ist die Schaltfläche für den Vollbildmodus nicht in der Benutzeroberfläche verfügbar.

Es ist möglich, schnell im Inhalt eines Videos zu navigieren, wenn das Video-Chaptering aktiviert ist. Videokapitel werden als Markierungen in der Video-Scrubber-Spur angezeigt und zeigen den Kapiteltitel und die zugehörige Beschreibung bei einem Mausklick über oder mit einem einzigen Tippen auf Touch-Systeme an. Benutzer können nach einem bestimmten Kapitel suchen, indem sie auf eine Kapitelmarke klicken oder auf die Kapitelbeschreibungsblase tippen.

Der Viewer unterstützt sowohl die Touch-Eingabe als auch die Mauseingabe auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome-, Internet Explorer 11- und Edge-Webbrowser beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Barrierefreiheit und Navigation über die Tastatur](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Tools zur Freigabe in Social Media mit dem Video-Viewer {#section-907d316fe1da4b87abb9775f02464704}

Der Video-Viewer unterstützt Tools zur Freigabe in Social Media. Diese sind als einzelne Schaltfläche in der Benutzeroberfläche verfügbar, die sich durch Klicken oder Tippen auf eine Freigabe-Symbolleiste in eine Freigabe-Symbolleiste einblendet.

Die Freigabesymbolleiste enthält ein Symbol für jeden unterstützten Freigabekanaltyp wie Facebook, Twitter, E-Mail-Freigabe, Einbettungscode-Freigabe und Linkfreigabe. Wenn die Tools für die Freigabe von E-Mails, die Einbettung von Freigabe oder die Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Formular für die Dateneingabe an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer von einem Social-Media-Dienst zu einem standardmäßigen Dialogfeld für die Freigabe um. Auch wenn ein Freigabe-Tool aktiviert ist, wird die Videowiedergabe automatisch angehalten.

Die Freigabe-Tools sind aufgrund der Sicherheitseinschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

## Einbetten des Video-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, der den Viewer beim Klicken in einem separaten Browser-Fenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt auf der Hosting-Seite einzubetten. In letzterem Fall kann die Webseite ein statisches Seitenlayout aufweisen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung in feste Größe und Einbettung in responsives Design.

Das Einbetten mehrerer Videos auf derselben Seite wird auf Tablets und Mobilgeräten unterstützt. In den meisten Fällen kann jeweils nur ein Video abgespielt werden. Wenn ein Benutzer mit der Wiedergabe eines Videos beginnt und dann versucht, ein weiteres Video abzuspielen, wird das erste Video automatisch angehalten. Das automatisch angehaltene Video speichert die aktuelle Wiedergabedauer, sodass der Benutzer jederzeit darauf zugreifen und die Wiedergabe fortsetzen kann. Die einzige Ausnahme ist der Chrome-Browser auf Android 4.x-Geräten, die Videos parallel wiedergeben können.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Bereich des Browser-Fensters und passt sich an, falls die Größe des Browsers geändert oder die Geräteausrichtung geändert wird.

Dieser Modus wird am häufigsten für Mobilgeräte verwendet. Die Webseite lädt den Viewer mit dem JavaScript-Aufruf `window.open()`, dem ordnungsgemäß konfigurierten HTML-Element `A` oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Es heißt [!DNL VideoViewer.html] und befindet sich im Unterordner [!DNL html5/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erreichen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Über Einbettungsmodus mit fester Größe und responsiven Einbettungsmodus**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien der Web-Seite.

Das primäre Anwendungsbeispiel sind Web-Seiten, die für Desktops oder Tablet-Geräte ausgerichtet sind, sowie responsive Design-Seiten, die das Layout automatisch an den Gerätetyp anpassen.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Auswahl ist am besten für Webseiten mit statischem Seitenlayout.

Responsives Einbetten von Design setzt voraus, dass die Größe des Viewers zur Laufzeit entsprechend der Größenänderung des Containers `DIV` ggf. angepasst werden muss. Der häufigste Anwendungsfall besteht darin, den Viewer zu einer Webseite hinzuzufügen, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für responsives Design verhält sich der Viewer je nach Größe des Containers `DIV` unterschiedlich. Wenn die Web-Seite nur die Breite des Containers `DIV` festlegt und dabei die Höhe unbegrenzt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Methode stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten aufgefüllt werden. Dieser Anwendungsfall ist der häufigste bei Webseiten, die ein responsives Design-Layout-Framework wie Bootstrap, Foundation usw. verwenden.

Wenn die Webseite andernfalls die Breite und Höhe für den Container des Viewers `DIV` festlegt, füllt der Viewer nur diesen Bereich und folgt der Größe, die durch das Layout der Webseite angegeben wird. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Größe des Webbrowserfensters skaliert wird.

**Einbettung fester Größe**

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie Folgendes ausführen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Containers `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL FlyoutViewer.js] angeben. Die Datei [!DNL FlyoutViewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Sie sollten nur auf die JavaScript-Hauptdatei für den Viewer `include` auf Ihrer Seite verweisen. Sie sollten keine zusätzlichen JavaScript-Dateien im Webseitencode referenzieren, die möglicherweise von der Viewer-Logik zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die HTML5-SDK-Bibliothek `Utils.js` , die vom Viewer aus dem Kontextpfad `/s7viewers` geladen wird (so genanntes konsolidiertes SDK `include`). Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig von der Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Adobe behält ältere Versionen des sekundären Viewers `includes` nicht auf dem Server bei.
>
>
>Infolgedessen wird die Viewer-Funktion bei der Bereitstellung einer neuen Produktversion zukünftig beeinträchtigt, wenn ein direkter Verweis auf ein sekundäres JavaScript `include` gesetzt wird, das vom Viewer auf der Seite verwendet wird.

1. Definieren des Container-DIV.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres DIV-Element hinzu. Die ID des DIV-Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird über CSS angegeben.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. die CSS-Eigenschaft `position` ist auf `relative` oder `absolute` festgelegt.

   Stellen Sie sicher, dass die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert. Vergewissern Sie sich, dass keine anderen Elemente im DOM vorhanden sind, die eine höhere Stapelreihenfolge aufweisen als Ihr Platzhalter-DIV.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-DIV-Element:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für die CSS-Klasse der obersten Ebene `.s7videoviewer` in absoluten Einheiten deklarieren oder den Modifikator `stagesize` verwenden.

   Die Größe in CSS kann direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festgelegt werden, die später einem Viewer-Vorgabendatensatz in Dynamic Media Classic zugewiesen oder explizit mithilfe eines Stilbefehls übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Video-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) .

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe in einer HTML-Seite:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können den Modifikator `stagesize` entweder im Viewer-Vorgabendatensatz in Dynamic Media Classic festlegen oder ihn explizit mit der Viewer-Initialisierungscode-Sammlung `params` oder als API-Aufruf übergeben, wie im Abschnitt Befehlsreferenz beschrieben:

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.VideoViewer`, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode `init()` in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID enthält und das verschachtelte `params` JSON-Objekt mit Konfigurationsparametern enthält, die vom Viewer unterstützt werden. In diesem Fall muss für das `params`-Objekt mindestens die Image Serving-URL als `serverUrl`-Eigenschaft übergeben werden, die Video-Server-URL als `videoserverurl`-Eigenschaft übergeben werden und das erste Asset als `asset`-Parameter. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()`-Methode direkt vor dem schließenden `BODY`-Tag oder das `onload()`-Ereignis im Hauptteil auf.

   Gleichzeitig sollte das Containerelement nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mit dem `display:none`-Stil ausgeblendet werden, der ihm zugewiesen ist. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()`-Methode. In diesem Beispiel wird angenommen, dass `videoViewer` die Viewer-Instanz ist, `s7viewer` der Name des Platzhalters `DIV`, [!DNL http://s7d1.scene7.com/is/image/] die Image Serving-URL, [!DNL http://s7d1.scene7.com/is/content/] die Video-Server-URL und [!DNL Scene7SharedAssets/Glacier_Climber_MP4] das Asset ist.

   ```
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Video-Viewer mit einer festen Größe einbettet:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Responsives Design mit uneingeschränkter Höhe**

Mit der Einbettung des responsiven Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers `DIV` vorgibt. Für dieses Beispiel nehmen Sie an, dass die Web-Seite es dem Container des Viewers `DIV` ermöglicht, 40 % der Fenstergröße des Webbrowsers zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt der Einbettung mit fester Größe sehr. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Fügen Sie den Container `DIV` zum vorhandenen &quot;Inhaber&quot; `DIV` hinzu. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

Die folgende Beispielseite veranschaulicht die reale Verwendung responsiver Designs, die mit unbegrenzter Höhe eingebettet werden:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demostandort](https://experienceleague.adobe.com/tools/vlist/vlist.html)

**Responsives Design, eingebettet in definierte Breite und Höhe**

Bei responsiven Designs, die mit definierter Breite und Höhe eingebettet werden, unterscheidet sich der Webseitenstil. Es stellt beide Größen für den &quot;Inhaber&quot; `DIV` bereit und zentriert ihn im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und `BODY` auf 100 %:

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Einbetten mit der Setter-basierten API**

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Mit dieser API akzeptiert der Konstruktor keine Parameter und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Einbettung fester Größe in eine setter-basierte API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```
