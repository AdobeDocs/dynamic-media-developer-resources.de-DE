---
description: Der Video-Viewer ist ein Videoplayer, der Streaming- und Progressiv-Videos im H.264-Format wiedergibt. Es wird vom Scene7 Publishing System oder von AEM Dynamic Media bereitgestellt.
keywords: responsive
seo-description: Der Video-Viewer ist ein Videoplayer, der Streaming- und Progressiv-Videos im H.264-Format wiedergibt. Es wird vom Scene7 Publishing System oder von AEM Dynamic Media bereitgestellt.
seo-title: Video
solution: Experience Manager
title: Video
topic: Dynamic media
uuid: 961a9b99-5892-4ee3-a2df-13e299f5d086
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video{#video}

Der Video-Viewer ist ein Videoplayer, der Streaming- und Progressiv-Videos im H.264-Format wiedergibt. Es wird vom Scene7 Publishing System oder von AEM Dynamic Media bereitgestellt.

Siehe [Systemanforderungen und -voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Es werden sowohl einzelne Video- als auch adaptive Videosets unterstützt. Darüber hinaus unterstützt der Viewer das Arbeiten mit progressiven Video- und HLS-Streams, die auf externen Speicherorten gehostet werden. Es wurde für die Verwendung mit Desktop- und mobilen Webbrowsern entwickelt, die HTML5-Videos unterstützen. Dieser Viewer unterstützt auch optionale Untertitel, die über Videoinhalten, Videokapitelnavigation und Social Media-Sharing-Werkzeugen angezeigt werden.

Der Video-Viewer verwendet die HTML5-Streaming-Videowiedergabe im HLS-Format in seiner Standardkonfiguration, wenn das zugrunde liegende System sie unterstützt. Auf Systemen, die kein HTML5-Streaming unterstützen, greift der Viewer auf den progressiven HTML5-Versand zurück.

Viewer-Typ 506.

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Verwenden des Video-Viewers {#section-f21ac23d3f6449ad9765588d69584772}

Der Video-Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar. Eine einzige JavaScript-Datei enthält alle Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets und CSS, die vom Viewer zur Laufzeit heruntergeladen werden.

Sie können den Video-Viewer im Popup-Modus verwenden, indem Sie eine produktionsfertige HTML-Seite verwenden, die mit IS-Viewern bereitgestellt wird. Oder Sie können den Viewer im eingebetteten Modus verwenden, wo er mithilfe der dokumentierten API in eine Zielgruppe-Webseite integriert ist.

Die Aufgabe, den Viewer zu konfigurieren und Skins zu erstellen, ähnelt der anderer Viewer. Alle Skins werden mithilfe von benutzerdefiniertem CSS erreicht.

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem Video-Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Der Video-Viewer bietet eine Reihe standardmäßiger Steuerelemente der Benutzeroberfläche für die Videowiedergabe, wie z. B. eine Wiedergabe-/Pause-Schaltfläche, Video-Scrubbing-Videozeitblase, Wiedergabedauer/Gesamtzeit-Indikator, Lautstärkeregelung, Vollbildschaltfläche und Umschalter für Bildunterschriften. Alle diese Steuerelemente werden in einer Steuerleiste am unteren Rand der Viewer-Benutzeroberfläche gruppiert.

Auf Touch-Geräten wird die Lautstärkeregelung in der Benutzeroberfläche ausgeblendet, da die Lautstärke nur über die Hardwaretasten gesteuert werden kann.

Wenn der Viewer im Popupmodus ausgeführt wird, ist die Schaltfläche für den Vollbildmodus nicht in der Benutzeroberfläche verfügbar.

Es ist möglich, schnell durch den Inhalt eines Videos zu navigieren, wenn das Videochaptern aktiviert ist. Videokapitel werden als Markierungen in der Videomaterial-Navigationsleiste angezeigt und zeigen den Kapiteltitel und die zugehörige Beschreibung bei einem Mausklick über oder mit einem einzigen Tippen auf Touchsysteme an. Benutzer können nach einem bestimmten Kapitel suchen, indem sie auf eine Kapitelmarke klicken oder auf die Kapitelbeschreibung tippen.

Der Viewer unterstützt sowohl Berührungseingaben als auch Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Barrierefreiheit und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)über die Tastatur.

## Werkzeuge zum Freigeben von sozialen Medien mit dem Video-Viewer {#section-907d316fe1da4b87abb9775f02464704}

Der Video-Viewer unterstützt Werkzeuge zum Freigeben von sozialen Medien. Sie stehen als einzelne Schaltfläche in der Benutzeroberfläche zur Verfügung, die sich durch Klicken oder Tippen auf eine Freigabebeschaltfläche in eine Freigabebeschaltfläche umwandelt.

Die Freigabe-Symbolleiste enthält ein Symbol für jeden unterstützten Freigabetyp, z. B. Facebook, Twitter, E-Mail-Freigabe, Einbettungscode-Freigabe und Linkfreigabe. Wenn die Tools für die Freigabe per E-Mail, die Einbettung von Teilen oder die Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Dateneingabeformular an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer über einen Social Media-Dienst zu einem Standardfreigabedialogfeld um. Auch wenn ein Freigabe-Tool aktiviert ist, wird die Videowiedergabe automatisch angehalten.

Die Freigabe von Werkzeugen ist aufgrund der Sicherheitsbeschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

## Einbetten des Video-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, über den der Viewer bei einem Klick in einem separaten Browserfenster geöffnet wird. In anderen Fällen ist es erforderlich, den Viewer direkt auf der Hostingseite einzubetten. Im letzteren Fall verfügt die Webseite möglicherweise über ein statisches Seitenlayout oder über ein reaktionsfähiges Design, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung in fester Größe und Einbettung in reaktionsfähiges Design.

Das Einbetten mehrerer Videos auf derselben Seite wird auf Tablets und Mobilgeräten unterstützt. In den meisten Fällen kann jeweils nur ein Video abgespielt werden. Wenn ein Beginn ein Video abspielt und dann versucht, ein weiteres Video abzuspielen, wird das erste Video automatisch angehalten. Das automatisch angehaltene Video speichert seine aktuelle Wiedergabezeit, sodass der Benutzer jederzeit darauf zurückgreifen und die Wiedergabe fortsetzen kann. Die einzige Ausnahme für diese Regel ist der Chrome-Browser auf Android 4.x-Geräten, die Videos parallel abspielen können.

**Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Browserfenster-Bereich und passt sich an, falls die Größe des Browsers oder die Geräteausrichtung geändert wird.

Dieser Modus ist der am häufigsten verwendete für Mobilgeräte. Die Webseite lädt den Viewer mit dem `window.open()` JavaScript-Aufruf, dem ordnungsgemäß konfigurierten `A` HTML-Element oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. Es wird aufgerufen [!DNL VideoViewer.html] und befindet sich im [!DNL html5/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erzielen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, mit dem der Viewer in einem neuen Fenster geöffnet wird:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Informationen zum Einbettungsmodus mit fester Größe und zum responsiven Einbettungsmodus**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer zusammenhängen. Der Viewer belegt normalerweise nur einen Teil der Immobilie der Webseite.

Der primäre Anwendungsfall sind Webseiten, die auf Desktop- oder Tablet-Geräte ausgerichtet sind, sowie reaktionsfähige Designseiten, die das Layout automatisch an den Gerätetyp anpassen.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Diese Option eignet sich am besten für Webseiten mit einem statischen Seitenlayout.

Bei der responsiven Design-Einbettung wird davon ausgegangen, dass die Größe des Viewers in der Laufzeit je nach Größenänderung des Containers möglicherweise angepasst werden muss `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen des Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für reaktionsfähiges Design verhält sich der Viewer je nach Größe des Containers der Webseite unterschiedlich `DIV`. Wenn die Webseite nur die Breite des Containers festlegt `DIV`und dabei die Höhe unbegrenzt bleibt, wählt der Viewer die Höhe automatisch entsprechend dem Seitenverhältnis des verwendeten Assets aus. Auf diese Weise wird sichergestellt, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten aufgefüllt werden müssen. Dieser Anwendungsfall ist der häufigste Fall für Webseiten, die ein reaktionsfähiges Layout-Framework wie Bootstrap, Foundation usw. verwenden.

Andernfalls füllt der Viewer, wenn die Webseite sowohl die Breite als auch die Höhe des Containers des Viewers festlegt `DIV`, nur diesen Bereich und folgt der vom Webseitenlayout bereitgestellten Größe. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung der Größe des Webbrowser-Fensters entspricht.

**Einbettung fester Größe**

Der Viewer wird wie folgt zu einer Webseite hinzugefügt:

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Containers `DIV`.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite

   Zum Erstellen eines Viewers müssen Sie im HTML-Kopf ein Skript-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL FlyoutViewer.js]dies berücksichtigen. Die [!DNL FlyoutViewer.js] Datei befindet sich im [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Relativer Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Sie sollten nur auf die JavaScript- `include` Hauptdatei des Viewers auf Ihrer Seite verweisen. Sie sollten keine weiteren JavaScript-Dateien im Webseitencode referenzieren, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Verweisen Sie insbesondere nicht direkt auf die vom Viewer aus dem `Utils.js` Kontextpfad (so genanntes konsolidiertes SDK) geladene HTML5 SDK- `/s7viewers` Bibliothek `include`. Der Grund dafür ist, dass der Speicherort von `Utils.js` oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig durch die Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Ältere Versionen des sekundären Viewers werden von Adobe nicht `includes` auf dem Server gespeichert.
>
>
>Infolgedessen wird die Viewer-Funktion bei der Bereitstellung einer neuen Produktversion durch direkte Verweise auf sekundäres JavaScript, das vom Viewer auf der Seite `include` verwendet wird, in Zukunft unterbrochen.

1. Definieren des Container-DIV.

   Hinzufügen ein leeres DIV-Element auf die Seite, auf der der Viewer angezeigt werden soll. Die ID des DIV-Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird durch CSS festgelegt.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute`eingestellt.

   Stellen Sie sicher, dass die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert. Vergewissern Sie sich, dass keine anderen Elemente im DOM eine höhere Stapelreihenfolge aufweisen als das Platzhalter-DIV.

   Das folgende Beispiel zeigt ein definiertes Platzhalter-DIV-Element:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Einstellen der Viewer-Größe

   Sie können die statische Größe des Viewers festlegen, indem Sie ihn entweder für die CSS-Klasse der `.s7videoviewer` obersten Ebene in absoluten Einheiten deklarieren oder den Modifikator verwenden `stagesize`.

   Die Größe in CSS kann auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei korrekt festgelegt werden, die später im Scene7 Publishing System einem Viewer-Vorgabendatensatz zugewiesen oder explizit mit einem Stilbefehl übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Video-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) .

   Im Folgenden finden Sie ein Beispiel zum Definieren einer statischen Viewer-Größe in einer HTML-Seite:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können den `stagesize` Modifikator entweder im Viewer-Vorgabendatensatz im Scene7 Publishing System festlegen oder ihn explizit mit dem Viewer-Initialisierungscode mit der `params` Sammlung oder als API-Aufruf, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben, übergeben, wie im Folgenden dargestellt:

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der `s7viewers.VideoViewer` Klasse, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode für eine Viewer-Instanz auf `init()` . Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über ein `containerId` Feld verfügen, das den Namen der Viewer-Container-ID und das verschachtelte `params` JSON-Objekt mit vom Viewer unterstützten Konfigurationsparametern enthält. In diesem Fall muss für das `params` Objekt mindestens die Image Serving-URL als `serverUrl` -Eigenschaft übergeben, die Video-Server-URL als `videoserverurl` -Eigenschaft und das ursprüngliche Asset als `asset` -Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und mit einem Beginn versehen.

   Es ist wichtig, dass der Viewer-Container dem DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser zögern die Erstellung von DOM bis zum Ende der Webseite. Um eine maximale Kompatibilität zu gewährleisten, rufen Sie die `init()` Methode direkt vor dem schließenden `BODY` Tag oder im Body- `onload()` Ereignis auf.

   Gleichzeitig sollte das Container-Element nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mithilfe des ihr zugewiesenen `display:none` Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der notwendigen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` Methode. In diesem Beispiel wird davon ausgegangen, dass `videoViewer` es sich um die Viewer-Instanz, `s7viewer` den Namen des Platzhalters `DIV`und [!DNL http://s7d1.scene7.com/is/image/] die Image Serving-URL handelt, [!DNL http://s7d1.scene7.com/is/content/] die Video-Server-URL und [!DNL Scene7SharedAssets/Glacier_Climber_MP4] das Asset.

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

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, die den Video-Viewer mit einer festen Größe einbettet:

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

**Responsive Design-Einbettung mit unbeschränkter Höhe**

Bei der Einbettung reaktionsfähiger Designs verfügt die Webseite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers vorgibt `DIV`. Für dieses Beispiel nehmen Sie an, dass der Container des Viewers auf der Webseite 40 % der Fenstergröße des Webbrowsers `DIV` annehmen kann, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ist der Einbettung in fester Größe sehr ähnlich. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers

Alle oben genannten Schritte sind identisch mit denen der Einbettung in fester Größe. Hinzufügen Container `DIV` zum bestehenden Inhaber `DIV`. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

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

Die folgende Beispielseite zeigt eine aktuellere Verwendung von reaktionsfähigem Design-Einbettungen mit uneingeschränkter Höhe:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**Responsive Design-Einbettung mit definierter Breite und Höhe**

Bei responsiver Designeinbettung mit definierter Breite und Höhe ist der Webseitenstil anders. Es bietet beide Größen für den &quot;Inhaber&quot; `DIV` und zentriert ihn im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und des `BODY` Elements auf 100 %:

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

Die verbleibenden Einbettungsschritte sind identisch mit der Einbettung von reaktionsfähigem Design mit uneingeschränkter Höhe. Das resultierende Beispiel lautet:

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

**Einbetten mithilfe der Setter-basierten API**

Anstatt JSON-basierte Initialisierung zu verwenden, ist es möglich, set-basierte API- und no-args-Konstruktoren zu verwenden. Mit dieser API akzeptiert der Konstruktor keine Parameter und Konfigurationsparameter werden mit `setContainerId()`, `setParam()`und `setAsset()` API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Im folgenden Beispiel wird die Einbettung fester Größe in Setter-basierte API veranschaulicht:

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

