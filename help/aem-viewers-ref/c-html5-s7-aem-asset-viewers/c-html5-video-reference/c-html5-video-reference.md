---
title: Video
description: Der Video-Viewer ist ein Video-Player, der im H.264-Format kodierte Streaming- und progressive Videos abspielt. Es wird von Dynamic Media Classic oder Adobe Experience Manager mit Dynamic Media bereitgestellt.
keywords: Responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2333'
ht-degree: 0%

---

# Video{#video}

Der Video-Viewer ist ein Video-Player, der im H.264-Format kodierte Streaming- und progressive Videos abspielt. Es wird von Dynamic Media Classic oder Experience Manager mit Dynamic Media bereitgestellt.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Es werden sowohl einzelne als auch adaptive Videosets unterstützt. Außerdem unterstützt der Viewer das Arbeiten mit progressiven Video- und HLS-Streams, die an externen Speicherorten gehostet werden. Es wurde für Desktop- und mobile Webbrowser entwickelt, die HTML5-Videos unterstützen. Dieser Viewer unterstützt auch optionale Untertitel, die über Videoinhalten, der Videokapitelnavigation und Tools zur Freigabe in Social Media angezeigt werden.

Der Video-Viewer verwendet HTML5-Streaming-Videowiedergabe im HLS-Format in der Standardkonfiguration, wenn das zugrunde liegende System dies unterstützt. Auf Systemen, die HTML5-Streaming nicht unterstützen, wird der Viewer auf die progressive HTML5-Videobereitstellung zurückgesetzt.

Viewer-Typ 506.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Verwenden des Video-Viewer {#section-f21ac23d3f6449ad9765588d69584772}

Der Video-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfsdateien dar - eine einzige JavaScript, die mit allen Viewer-SDK-Komponenten enthalten ist, die von diesem bestimmten Viewer verwendet werden, sowie Assets und CSS, die der Viewer zur Laufzeit heruntergeladen hat.

Sie können den Video-Viewer im Popup-Modus mit der produktionsbereiten HTML-Seite verwenden, die mit IS-Viewers bereitgestellt wird. Sie können den Viewer auch im eingebetteten Modus verwenden, in dem er mithilfe der dokumentierten API in eine Ziel-Web-Seite integriert wird.

Die Aufgabe der Konfiguration und Skin-Verwaltung des Viewers ist ähnlich wie bei anderen Viewern. Die gesamte Skin-Verwaltung erfolgt über benutzerdefiniertes CSS.

Siehe [Für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Für alle Viewer gemeinsame Befehlsreferenz - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem Video-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Video Viewer bietet eine Reihe von Standardsteuerelementen der Benutzeroberfläche für die Videowiedergabe, z. B. eine Wiedergabe-/Pausenschaltfläche, Video-Scrubber-Video-Zeitblase, Anzeige der wiedergegebenen Zeit/Gesamtzeit, Lautstärkeregelung, Vollbildschaltfläche und Umschalten der Untertitel. Alle diese Steuerelemente werden in einer Steuerleiste am unteren Rand der Viewer-Benutzeroberfläche gruppiert.

Auf Touch-Geräten ist die Lautstärkeregelung auf der Benutzeroberfläche ausgeblendet, da die Lautstärkeregelung nur über die Hardwaretasten gesteuert werden kann.

Wenn der Viewer im Popup-Modus ausgeführt wird, ist die Vollbildschaltfläche in der Benutzeroberfläche nicht verfügbar.

Es ist möglich, schnell durch den Inhalt eines Videos zu navigieren, wenn das Videokapitel aktiviert ist. Videokapitel werden als Markierungen in der Video-Scrubber-Spur angezeigt und zeigen den Kapiteltitel und die zugehörige Beschreibung bei einem Mausrollover oder mit einem einzigen Tippen auf Touch-Systeme an. Benutzer können nach einem bestimmten Kapitel suchen, indem sie eine Kapitelmarkierung oder die Kapitelbeschreibungsblase auswählen.

Der Viewer unterstützt sowohl Touch-Eingabe als auch Mauseingabe auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.

Dieser Viewer ist vollständig mit der Tastatur zugänglich.

Siehe [Tastaturzugriff und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Tools zur Freigabe in Social Media mit Video Viewer {#section-907d316fe1da4b87abb9775f02464704}

Der Video-Viewer unterstützt Tools zur Freigabe in Social Media. Sie sind in der Benutzeroberfläche als einzelne Schaltfläche verfügbar, die in eine Freigabesymbolleiste erweitert wird, wenn Benutzende darauf klicken oder tippen.

Die Freigabesymbolleiste enthält ein Symbol für jeden unterstützten Freigabekanaltyp wie Facebook, Twitter, E-Mail-Freigabe, Einbettungs-Code-Freigabe und Link-Freigabe. Wenn die Tools E-Mail-Freigabe, Einbettungsfreigabe oder Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Dateneingabeformular an. Wenn Facebook oder Twitter aufgerufen werden, leitet der Viewer den Benutzer von einem Social-Media-Service zu einem Standarddialogfeld für die Freigabe um. Auch wenn ein Freigabetool aktiviert ist, wird die Videowiedergabe automatisch angehalten.

Freigabetools sind aufgrund von Sicherheitsbeschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

## Einbetten des Video-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Web-Seiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal enthält eine Web-Seite einen Link, der bei Auswahl den Viewer in einem separaten Browser-Fenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt auf der Hosting-Seite einzubetten. Im letzteren Fall kann die Web-Seite über ein statisches Seiten-Layout verfügen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diesen Anforderungen gerecht zu werden, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung mit fester Größe und Einbetten von responsivem Design.

Das Einbetten mehrerer Videos auf derselben Seite wird auf Tablets und Mobilgeräten unterstützt. Normalerweise kann immer nur ein Video wiedergegeben werden. Wenn ein(e) Benutzende(r) beginnt, ein Video abzuspielen und dann versucht, ein anderes Video abzuspielen, wird das erste Video automatisch angehalten. Das automatisch angehaltene Video speichert die aktuelle Wiedergabezeit, sodass der/die Benutzende immer darauf zurückgreifen und die Wiedergabe fortsetzen kann. Die einzige Ausnahme von dieser Regel ist der Chrome-Browser auf Android™ 4.x-Geräten, auf dem Videos parallel wiedergegeben werden können.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Fenster oder einer separaten Registerkarte des Webbrowsers geöffnet. Sie nimmt den gesamten Browser-Fensterbereich und passt sich an, falls die Größe des Browsers geändert oder die Ausrichtung des Geräts geändert wird.

Dieser Modus ist bei Mobilgeräten am häufigsten. Die Web-Seite lädt den Viewer mithilfe `window.open()` JavaScript-Aufrufs, eines ordnungsgemäß konfigurierten HTML-Elements `A` einer anderen geeigneten Methode.

Es wird empfohlen, eine vorkonfigurierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Sie wird als [!DNL VideoViewer.html] bezeichnet und befindet sich im [!DNL html5/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Sie können die visuelle Anpassung erreichen, indem Sie benutzerdefiniertes CSS anwenden.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Über den Einbettungsmodus mit fester Größe und den responsiven Einbettungsmodus**

Im eingebetteten Modus wird der Viewer zur vorhandenen Web-Seite hinzugefügt, die möglicherweise bereits einige Kundeninhalte enthält, die nicht mit dem Viewer verknüpft sind. Der Viewer belegt normalerweise nur einen Teil des Grundbesitzes der Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die für Desktops oder Tablet-Geräte ausgerichtet sind, sowie responsive Design-Seiten, deren Layout automatisch an den Gerätetyp angepasst wird.

Einbetten in fester Größe wird verwendet, wenn der Viewer nach dem ersten Laden seine Größe nicht ändert. Diese Option eignet sich am besten für Web-Seiten mit statischem Seiten-Layout.

Beim Einbetten eines responsiven Designs wird davon ausgegangen, dass die Größe des Viewers zur Laufzeit entsprechend der Größenänderung seiner Container-`DIV` geändert werden muss. Der häufigste Anwendungsfall besteht darin, den Viewer zu einer Web-Seite hinzuzufügen, die ein flexibles Seiten-Layout verwendet.

Im responsiven Design-Einbettungsmodus verhält sich der Viewer unterschiedlich, je nachdem, wie die Web-Seite die Größe ihres Container-`DIV` bestimmt. Wenn die Web-Seite nur die Breite des Container-`DIV` festlegt und seine Höhe nicht eingeschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Auf diese Weise wird sichergestellt, dass das Asset perfekt in die Ansicht passt, ohne dass an den Seiten ein Abstand vorhanden ist. Dieser Anwendungsfall ist der häufigste für Web-Seiten, die ein responsives Design-Layout-Framework wie Bootstrap oder Foundation verwenden.

Wenn die Web-Seite jedoch sowohl die Breite als auch die Höhe für die Container-`DIV` des Viewers festlegt, füllt der Viewer nur diesen Bereich aus und folgt der vom Web-Seiten-Layout bereitgestellten Größe. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung an die Größe des Webbrowser-Fensters angepasst ist.

**Einbetten in fester Größe**

Sie können den Viewer wie folgt zu einer Web-Seite hinzufügen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Container-`DIV` definieren.
1. Festlegen der Viewer-Größe.
1. Viewer erstellen und initialisieren.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.

   Zum Erstellen eines Viewers müssen Sie dem HTML-Head ein Script-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL FlyoutViewer.js] einbeziehen. Die [!DNL FlyoutViewer.js]-Datei befindet sich im [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewers-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und er von derselben Domain bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Verweisen Sie auf Ihrer Seite nur auf die JavaScript-`include`-Datei des Haupt-Viewers. Verweisen Sie nicht auf zusätzliche JavaScript-Dateien im Web-Seiten-Code, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die vom Viewer aus `/s7viewers` Kontextpfad geladene HTML5 SDK `Utils.js`-Bibliothek (so genannte konsolidierte SDK-`include`). Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Runtime-Viewer-Bibliotheken vollständig von der Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Adobe speichert ältere Versionen der sekundären Viewer-`includes` nicht auf dem Server.
>
>
>Wenn Sie also auf der Seite einen direkten Verweis auf eine sekundäre JavaScript-`include` einfügen, die vom Viewer verwendet wird, wird die Viewer-Funktionalität in Zukunft unterbrochen, wenn eine neue Produktversion bereitgestellt wird.

1. Definieren des Container-DIV.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres DIV-Element hinzu. Für das DIV-Element muss eine ID definiert sein, da diese ID später an die Viewer-API übergeben wird. Die Größe des DIV wird durch CSS angegeben.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute` festgelegt.

   Stellen Sie sicher, dass die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert. Stellen Sie sicher, dass das DOM keine anderen Elemente enthält, die eine höhere Stapelreihenfolge als der Platzhalter-DIV aufweisen.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-DIV-Element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Festlegen der Viewer-Größe

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für `.s7videoviewer` CSS-Klasse der obersten Ebene in absoluten Einheiten deklarieren oder den Modifikator `stagesize` verwenden.

   Sie können die Größenanpassung in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten CSS-Viewer-Datei festlegen. Sie wird später einem Viewer-Vorgabeneintrag in Dynamic Media Classic zugewiesen oder explizit mit einem Stilbefehl übergeben.

   Weitere [ zum Formatieren des Viewers mit CSS finden ](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) unter „Anpassen des Video-Viewers“ .

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf einer HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können `stagesize` Modifikator entweder im Viewer-Vorgabeneintrag in Dynamic Media Classic festlegen oder ihn explizit mit dem Viewer-Initialisierungs-Code mit `params` Sammlung übergeben. Oder als API-Aufruf, wie im Abschnitt Befehlsreferenz beschrieben, wie im Folgenden beschrieben:

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   Ein CSS-basierter Ansatz wird empfohlen und wird in diesem Beispiel verwendet.

1. Viewer erstellen und initialisieren.

   Wenn Sie die obigen Schritte ausgeführt haben, erstellen Sie eine Instanz `s7viewers.VideoViewer` Klasse, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen `init()` Methode in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über `containerId` Feld verfügen, das den Namen der Viewer-Container-ID enthält und `params` JSON-Objekt mit Konfigurationsparametern verschachtelt ist, die vom Viewer unterstützt werden. In diesem Fall muss `params` -Objekt mindestens die Bildbereitstellungs-URL als `serverUrl`-Eigenschaft, die Videoserver-URL als `videoserverurl`-Eigenschaft und das anfängliche Asset als `asset`-Parameter übergeben haben. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzigen Codezeile erstellen und starten.

   Es ist wichtig, dass der Viewer-Container zum DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser verzögern die Erstellung von DOM bis zum Ende der Web-Seite. Um maximale Kompatibilität zu erzielen, rufen Sie die `init()`-Methode unmittelbar vor dem schließenden `BODY`-Tag oder im body-`onload()` auf.

   Gleichzeitig sollte das Container-Element noch nicht unbedingt Teil des Web-Seiten-Layouts sein. Beispielsweise kann sie mithilfe `display:none` ihr zugewiesenen Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Moment, an dem die Web-Seite das Container-Element wieder zum Layout zurückbringt. Wenn diese Aktion stattfindet, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()`-Methode. In diesem Beispiel wird davon ausgegangen, `videoViewer` die Viewer-Instanz ist, `s7viewer` der Name des Platzhalters `DIV` ist, [!DNL http://s7d1.scene7.com/is/image/] die Bildbereitstellungs-URL ist, [!DNL http://s7d1.scene7.com/is/content/] die Videoserver-URL ist und [!DNL Scene7SharedAssets/Glacier_Climber_MP4] das Asset ist.

   ```html {.line-numbers}
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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, bei der der Video-Viewer mit einer festen Größe eingebettet wird:

   ```html {.line-numbers}
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

**Responsives Design mit unbegrenzter Höhe**

Durch das Einbetten des responsiven Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße der Container-`DIV` des Viewers bestimmt. Nehmen wir für die Zwecke dieses Beispiels an, dass die Web-Seite dem Container-`DIV` des Viewers ermöglicht, 40 % der Fenstergröße des Webbrowsers zu verwenden, wobei seine Höhe nicht beschränkt wird. Der Web-Seiten-HTML-Code würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt der Einbettung in fester Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Definieren des Container-DIV.
1. Viewer erstellen und initialisieren.

Alle oben genannten Schritte sind dieselben wie bei der Einbettung in fester Größe. Fügen Sie Container-`DIV` zum vorhandenen `DIV` „Inhaber“ hinzu. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn der Browser skaliert wird, und wie das Seitenverhältnis des Viewers mit dem Asset übereinstimmt.

```html {.line-numbers}
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

Die folgende Beispielseite veranschaulicht eine praktischere Verwendung der responsiven Designeinbettung mit unbegrenzter Höhe:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demo-Speicherort](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=de)

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

Die restlichen Einbettungsschritte sind identisch mit der responsiven Designeinbettung mit unbegrenzter Höhe. Das daraus resultierende Beispiel lautet:

```html {.line-numbers}
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

**Einbetten mithilfe der Setter-basierten API**

Anstatt die JSON-basierte Initialisierung zu verwenden, ist es möglich, eine Setter-basierte API und einen Nicht-Args-Konstruktor zu verwenden. Mit dieser API übernimmt der Konstruktor keine Parameter und Konfigurationsparameter werden mithilfe von `setContainerId()`-, `setParam()`- und `setAsset()`-API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Einbettung fester Größe mit einer Setter-basierten API:

```html {.line-numbers}
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
