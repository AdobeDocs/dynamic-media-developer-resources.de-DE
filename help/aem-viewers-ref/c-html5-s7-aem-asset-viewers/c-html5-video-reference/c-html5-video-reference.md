---
title: Video
description: Der Video-Viewer ist ein Videoplayer, der Streaming- und progressive Videos wiedergibt, die im H.264-Format kodiert sind. Es wird aus Dynamic Media Classic oder Adobe Experience Manager mit Dynamic Media bereitgestellt.
keywords: responsive
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

Der Video-Viewer ist ein Videoplayer, der Streaming- und progressive Videos wiedergibt, die im H.264-Format kodiert sind. Es wird aus Dynamic Media Classic oder Experience Manager mit Dynamic Media bereitgestellt.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Es werden sowohl einzelne Video- als auch adaptive Videosets unterstützt. Außerdem unterstützt der Viewer die Arbeit mit progressiven Video- und HLS-Streams, die auf externen Standorten gehostet werden. Es wurde für Desktop- und mobile Webbrowser entwickelt, die HTML5-Videos unterstützen. Dieser Viewer unterstützt auch optionale Untertitel, die über Videoinhalten, Videokapitelnavigation und Tools zur Freigabe in sozialen Medien angezeigt werden.

Der Video-Viewer verwendet die HTML5-Streaming-Videowiedergabe im HLS-Format in seiner Standardkonfiguration, wenn das zugrunde liegende System dies unterstützt. Auf Systemen, die HTML5-Streaming nicht unterstützen, greift der Viewer auf die progressive HTML5-Videowiedergabe zurück.

Viewer-Typ 506.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Video-Viewer verwenden {#section-f21ac23d3f6449ad9765588d69584772}

Der Video-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar. Eine einzelne JavaScript-Include-Datei enthält alle Viewer-SDK-Komponenten, die von diesem bestimmten Viewer verwendet werden, Assets und CSS, die vom Viewer zur Laufzeit heruntergeladen werden.

Sie können den Video-Viewer im Popup-Modus verwenden, indem Sie die produktionsbereite HTML-Seite verwenden, die mit IS-Viewern bereitgestellt wird. Alternativ können Sie den Viewer im eingebetteten Modus verwenden, wo er mithilfe der dokumentierten API in eine Ziel-Web-Seite integriert wird.

Die Aufgabe, den Viewer zu konfigurieren und zu skizzieren, ähnelt anderen Viewern. Die gesamte Skinning-Funktion wird über benutzerdefiniertes CSS erreicht.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem Video-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Der Video-Viewer bietet eine Reihe von standardmäßigen Steuerelementen für die Benutzeroberfläche für die Videowiedergabe, wie z. B. eine Wiedergabe-/Pausenschaltfläche, Video-Scrubber-Videozeitblase, Anzeige der Wiedergabezeit/Gesamtdauer, Lautstärkeregler, Schaltfläche im Vollbildmodus und Umschalter für Untertitel. Alle diese Steuerelemente sind in einer Steuerleiste am unteren Rand der Viewer-Benutzeroberfläche gruppiert.

Auf Touch-Geräten ist die Lautstärkeregelung in der Benutzeroberfläche ausgeblendet, da die Lautstärke nur über die Hardwaretasten gesteuert werden kann.

Wenn der Viewer im Popup-Modus ausgeführt wird, ist die Schaltfläche im Vollbildmodus nicht in der Benutzeroberfläche verfügbar.

Es ist möglich, schnell im Inhalt eines Videos zu navigieren, wenn das Videokapitel aktiviert ist. Videokapitel werden als Markierungen in der Video-Scrubber-Spur angezeigt und zeigen den Kapiteltitel und die zugehörige Beschreibung bei einem Mausrollover oder mit einem einzigen Tippen auf Touch-Systeme an. Benutzer können nach einem bestimmten Kapitel suchen, indem sie eine Kapitelmarke auswählen oder die Blase der Kapitelbeschreibung auswählen.

Der Viewer unterstützt sowohl die Touch-Eingabe als auch die Mauseingabe auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome-, Internet Explorer 11- und Edge-Webbrowser beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Barrierefreiheit und Navigation auf der Tastatur](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Tools zur Freigabe in Social Media mit dem Video-Viewer {#section-907d316fe1da4b87abb9775f02464704}

Der Video-Viewer unterstützt Tools zur Freigabe in sozialen Medien. Sie sind als einzelne Schaltfläche in der Benutzeroberfläche verfügbar, die sich zu einer Freigabesymbolleiste erweitert, wenn der Benutzer darauf klickt oder tippt.

Die Freigabesymbolleiste enthält ein Symbol für jeden unterstützten Freigabekanaltyp wie Facebook, Twitter, E-Mail-Freigabe, Einbettungscode-Freigabe und Linkfreigabe. Wenn die Tools für die Freigabe von E-Mails, die Einbettung von Freigabe oder die Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Dateneingabeformular an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer von einem Social-Media-Dienst zu einem standardmäßigen Dialogfeld für die Freigabe um. Auch wenn ein Freigabe-Tool aktiviert ist, wird die Videowiedergabe automatisch angehalten.

Die Freigabe-Tools sind aufgrund der Sicherheitseinschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

## Einbetten des Video-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, der, wenn ausgewählt, den Viewer in einem separaten Browserfenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt auf der Hosting-Seite einzubetten. In letzterem Fall kann die Webseite ein statisches Seitenlayout aufweisen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei Hauptbetriebsmodi: Popup, Einbettung fester Größe und Einbettung responsiver Designs.

Das Einbetten mehrerer Videos auf derselben Seite wird auf Tablets und Mobilgeräten unterstützt. Normalerweise kann nur ein Video gleichzeitig wiedergegeben werden. Wenn ein Benutzer mit der Wiedergabe eines Videos beginnt und dann versucht, ein weiteres Video abzuspielen, wird das erste Video automatisch angehalten. Das automatisch angehaltene Video speichert die aktuelle Wiedergabedauer, sodass der Benutzer jederzeit darauf zugreifen und die Wiedergabe fortsetzen kann. Die einzige Ausnahme bildet der Chrome-Browser auf Geräten mit Android™ 4.x, die Videos parallel wiedergeben können.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Bereich des Browser-Fensters und passt sich an, falls die Größe des Browsers geändert oder die Geräteausrichtung geändert wird.

Dieser Modus wird am häufigsten für Mobilgeräte verwendet. Die Webseite lädt den Viewer mit dem Aufruf `window.open()` JavaScript , dem ordnungsgemäß konfigurierten Element `A` HTML oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Es heißt [!DNL VideoViewer.html] und befindet sich im Unterordner [!DNL html5/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erreichen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Über Einbettungsmodus mit fester Größe und responsiven Einbettungsmodus**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien der Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Design-Seiten, auf denen das Layout automatisch an den Gerätetyp angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Auswahl ist am besten für Webseiten mit statischem Seitenlayout.

Responsive Designeinbettung setzt voraus, dass die Größe des Viewers zur Laufzeit angepasst werden muss, wenn die Größe des Containers geändert wird `DIV`. Der häufigste Anwendungsfall besteht darin, den Viewer zu einer Webseite hinzuzufügen, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für responsive Designs verhält sich der Viewer je nach Größe des Containers `DIV` unterschiedlich. Wenn die Webseite nur die Breite des Containers &quot;`DIV`&quot; festlegt und die Höhe nicht eingeschränkt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Methode stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten aufgefüllt werden. Dieser Anwendungsfall ist am häufigsten für Webseiten, die ein responsives Design-Layout-Framework wie Bootstrap oder Foundation verwenden.

Wenn die Web-Seite andernfalls die Breite und Höhe für den Container des Viewers `DIV` festlegt, füllt der Viewer nur diesen Bereich und folgt der Größe, die durch das Layout der Web-Seite angegeben wird. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Größe des Webbrowserfensters skaliert wird.

**Einbettung fester Größe**

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie Folgendes ausführen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Containers `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL FlyoutViewer.js] einbeziehen. Die Datei [!DNL FlyoutViewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf dem die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
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

   Stellen Sie sicher, dass die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert. Vergewissern Sie sich, dass keine anderen Elemente im DOM vorhanden sind, die eine höhere Stapelreihenfolge aufweisen als Ihr Platzhalter-DIV.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-DIV-Element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Viewer-Größe festlegen

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für die CSS-Klasse der obersten Ebene in absoluten Einheiten deklarieren oder den Modifikator `stagesize` verwenden.`.s7videoviewer`

   Sie können die Größe in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festlegen. Sie wird später einem Viewer-Vorgabendatensatz in Dynamic Media Classic zugewiesen oder explizit mithilfe eines Stilbefehls übergeben.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Video-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) .

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf einer HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können den Modifikator `stagesize` entweder im Viewer-Vorgabendatensatz in Dynamic Media Classic festlegen oder ihn explizit mit dem Viewer-Initialisierungscode mit der Sammlung `params` übergeben. Oder als API-Aufruf, wie im Abschnitt Befehlsreferenz beschrieben:

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.VideoViewer`, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode `init()` in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID und das verschachtelte JSON-Objekt `params` mit Konfigurationsparametern enthält, die vom Viewer unterstützt werden. In diesem Fall muss für das Objekt `params` mindestens die Image Serving-URL als `serverUrl`-Eigenschaft, die Video-Server-URL als `videoserverurl`-Eigenschaft und das erste Asset als `asset`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()` -Methode direkt vor dem schließenden `BODY` -Tag oder das body `onload()` -Ereignis auf.

   Gleichzeitig sollte das Containerelement nicht unbedingt Teil des Web-Seiten-Layouts sein. Sie kann beispielsweise mit dem ihm zugewiesenen `display:none` -Stil ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. Wenn diese Aktion auftritt, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` -Methode. In diesem Beispiel wird angenommen, dass `videoViewer` die Viewer-Instanz ist, `s7viewer` der Name des Platzhalters `DIV`, [!DNL http://s7d1.scene7.com/is/image/] die Image Serving-URL, [!DNL http://s7d1.scene7.com/is/content/] die Video-Server-URL und [!DNL Scene7SharedAssets/Glacier_Climber_MP4] das Asset ist.

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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Video-Viewer mit einer festen Größe einbettet:

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

**Responsives Design, eingebettet in unbeschränkte Höhe**

Mit der Einbettung des responsiven Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers `DIV` vorgibt. Für dieses Beispiel nehmen Sie an, dass die Web-Seite es dem Container `DIV` des Viewers ermöglicht, 40 % der Fenstergröße des Webbrowsers zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt der Einbettung mit fester Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind mit der Einbettung fester Größe identisch. Fügen Sie dem vorhandenen &quot;Inhaber&quot; `DIV` den Container `DIV` hinzu. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

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

Die restlichen Einbettungsschritte sind mit dem responsiven Design identisch, das mit uneingeschränkter Höhe eingebettet wird. Das folgende Beispiel zeigt:

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

**Einbetten mit Setter-basierter API**

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Mit dieser API akzeptiert der Konstruktor keine Parameter und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Einbettung fester Größe in eine setter-basierte API:

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
