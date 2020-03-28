---
description: Der Viewer für die E-Katalog-Suche ist ein Katalog-Viewer, der elektronische Prospekte auf Druckbogen oder Seite nach Seite anzeigt. Der E-Katalog ermöglicht Benutzern das Navigieren durch den Katalog mithilfe zusätzlicher Elemente der Benutzeroberfläche oder des speziellen Miniaturansichtsmodus. Benutzer können auch auf jeder Seite heranzoomen, um mehr Details zu erhalten.
keywords: responsive
seo-description: Der Viewer für die E-Katalog-Suche ist ein Katalog-Viewer, der elektronische Prospekte auf Druckbogen oder Seite nach Seite anzeigt. Der E-Katalog ermöglicht Benutzern das Navigieren durch den Katalog mithilfe zusätzlicher Elemente der Benutzeroberfläche oder des speziellen Miniaturansichtsmodus. Benutzer können auch auf jeder Seite heranzoomen, um mehr Details zu erhalten.
seo-title: E-Katalog-Suche
solution: Experience Manager
title: E-Katalog-Suche
topic: Dynamic media
uuid: f5ec33bf-e827-4709-9780-6f17096bf306
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# E-Katalog-Suche{#ecatalog-search}

Der Viewer für die E-Katalog-Suche ist ein Katalog-Viewer, der elektronische Prospekte auf Druckbogen oder Seite nach Seite anzeigt. Der E-Katalog ermöglicht Benutzern das Navigieren durch den Katalog mithilfe zusätzlicher Elemente der Benutzeroberfläche oder des speziellen Miniaturansichtsmodus. Benutzer können auch auf jeder Seite heranzoomen, um mehr Details zu erhalten.

Dieser Viewer funktioniert mit Katalogen und unterstützt optionale Imagemaps und Werkzeuge zum Weitergeben in sozialen Netzwerken. Es verfügt über Zoomwerkzeuge, Katalognavigationstools, Vollbildunterstützung, Miniaturansichten und eine optionale Schließen-Schaltfläche. Der Viewer unterstützt außerdem Werkzeuge zum Weitergeben in sozialen Netzwerken, Drucken, Herunterladen und Favoriten. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.

Der Benutzer kann auch eine suchbegriffsbasierte oder auf Wortfolgen basierende Suche über den Kataloginhalt durchführen.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ 513.

Siehe [Systemanforderungen und -voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/)

## Verwenden des E-Katalog-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der E-Katalog-Search Viewer stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar (ein einzelnes JavaScript enthält alle Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden

Sie können den E-Katalog-Search-Viewer im Popupmodus verwenden, indem Sie eine produktionsfertige HTML-Seite verwenden, die mit IS-Viewern bereitgestellt wird, oder im eingebetteten Modus, wo er mithilfe der dokumentierten API in die Zielgruppe-Webseite integriert wird.

Konfigurationen und Skins ähneln denen anderer Viewer. Alle Skins werden mithilfe von benutzerdefiniertem CSS erreicht.

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem E-Katalog-Search-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der E-Katalog-Search-Viewer unterstützt die folgenden Berührungsgesten, die in anderen Mobilanwendungen häufig vorkommen.

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
   <td colname="col2"> <p> Wählt neue Miniaturansichten in Farbfeldern aus. </p> </td> 
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
   <td colname="col2"> <p>Führt einen Bildlauf durch die Liste von Katalogseiten durch, wenn eine Transition mit einem Diashow-Rahmen verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Wischen oder Klick </p> </td> 
   <td colname="col2"> <p>Wenn sich das Bild in einem Reset-Status befindet, führt es einen nativen Seitenbildlauf durch. </p> <p>Wenn Miniaturansichten aktiv sind, wird die Liste der Miniaturansichten durchlaufen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Es ist möglich, einen realistischen Animationseffekt für Seitenumbrüche zu aktivieren, um zwischen Katalogseiten zu navigieren. In solchen Fällen kann ein Benutzer eine Seitenecke halten und ziehen und die Seite spiegeln.

Dieser Viewer unterstützt auch die Eingabe per Touch- und Mausklick auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.

## Social-Media-Freigabe-Tools mit dem E-Katalog-Search-Viewer {#section-eb575084a99647c3a9591f439f40b412}

Der E-Katalog-Search-Viewer unterstützt Social Sharing-Tools. Sie stehen als Schaltfläche in der Hauptsteuerungsleiste zur Verfügung. Diese wird zu einer Freigabewerkzeugleiste erweitert, wenn ein Benutzer darauf klickt oder darauf tippt.

Die Symbolleiste für die Freigabe enthält Symbole für jeden unterstützten Typ von freigegebenen Kanälen, einschließlich Facebook, Twitter, E-Mail-Freigabe, Einbettungscode-Freigabe und Linkfreigabe. Wenn die Tools für die Freigabe per E-Mail, die Einbettung von Teilen oder die Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Dateneingabeformular an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer zu einem standardmäßigen Freigabedialogfeld von einem Social-Dienst weiter. Die Freigabe von Werkzeugen ist aufgrund der Sicherheitsbeschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

Die Suchfunktion des Viewers ist als gläsernes Symbol in der Hauptsymbolleiste verfügbar. Durch Klicken oder Tippen auf das Symbol wird der Suchbereich mit einem Eingabefeld aktiviert. Nachdem Sie einen Suchbegriff oder eine Wortgruppe eingegeben und die Eingabetaste gedrückt haben, rendert der Viewer die Suchergebnisse im Bedienfeld und markiert die gefundenen Wörter in der Haupt-Ansicht.

## Einbetten des E-Katalog-Such-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, über den der Viewer bei einem Klick in einem separaten Browserfenster geöffnet wird. In anderen Fällen ist es erforderlich, den Viewer direkt auf der Hostingseite einzubetten. Im letzteren Fall verfügt die Webseite möglicherweise über ein statisches Seitenlayout oder über ein reaktionsfähiges Design, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung in fester Größe und Einbettung in reaktionsfähiges Design.

**Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Browserfenster-Bereich und passt sich an, falls die Größe des Browsers oder die Ausrichtung des Mobilgeräts geändert wird.

Der Popupmodus ist der häufigste für Mobilgeräte. Die Webseite lädt den Viewer mit dem `window.open()` JavaScript-Aufruf, dem ordnungsgemäß konfigurierten `A` HTML-Element oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. In diesem Fall wird es aufgerufen [!DNL eCatalogSearchViewer.html] und befindet sich im [!DNL html5/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erzielen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, mit dem der Viewer in einem neuen Fenster geöffnet wird:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**Einbettungsmodus mit fester Größe und Einbettungsmodus für reaktionsfähiges Design**

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer zusammenhängen. Der Viewer belegt normalerweise nur einen Teil der Immobilie einer Webseite.

Die wichtigsten Anwendungsfälle sind Webseiten, die auf Desktop- oder Tablet-Geräte ausgerichtet sind, sowie reaktionsfähige Seiten, die das Layout automatisch an den Gerätetyp anpassen.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Dies ist die beste Wahl für Webseiten mit einem statischen Layout.

Bei der responsiven Design-Einbettung wird davon ausgegangen, dass der Viewer die Größe zur Laufzeit ändern muss, je nach Größenänderung des Containers `DIV`. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für reaktionsfähiges Design verhält sich der Viewer je nach Größe des Containers der Webseite unterschiedlich `DIV`. Wenn die Webseite nur die Breite des Containers festlegt `DIV`und dabei die Höhe unbegrenzt bleibt, wählt der Viewer die Höhe automatisch entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass es an den Seiten aufgefüllt werden muss. Dieser Anwendungsfall ist der häufigste Fall für Webseiten mit reaktionsfähigen Layout-Frameworks wie Bootstrap, Foundation usw.

Andernfalls füllt der Viewer, wenn die Webseite sowohl die Breite als auch die Höhe des Containers des Viewers festlegt `DIV`, nur diesen Bereich aus und entspricht der Größe des Webseitenlayouts. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung je nach Webbrowser-Fenstergröße angepasst wird.

**Einbettung fester Größe**

Der Viewer wird wie folgt zu einer Webseite hinzugefügt:

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Container-DIV.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite

   Zum Erstellen eines Viewers müssen Sie im HTML-Kopf ein Skript-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL eCatalogSearchViewer.js]dies berücksichtigen. Die [!DNL eCatalogSearchViewer.js] Datei befindet sich im [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Scene7-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Scene7-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. Definieren des Container-DIV.

   Hinzufügen ein leeres DIV-Element auf die Seite, auf der der Viewer angezeigt werden soll. Die ID des DIV-Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute`eingestellt.

   Das folgende Beispiel zeigt ein definiertes Platzhalter-DIV-Element:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Einstellen der Viewer-Größe

   Sie können die statische Größe des Viewers festlegen, indem Sie ihn entweder für die CSS-Klasse der `.s7ecatalogsearchviewer` obersten Ebene in absoluten Einheiten deklarieren oder einen `stagesize` Modifikator verwenden.

   Sie können die Größe in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festlegen, die später im Scene7 Publishing System einem Viewer-Vorgabendatensatz zugewiesen oder explizit mit einem Stilbefehl übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des E-Katalog-Viewers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf einer HTML-Seite:

   ```
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können den `stagesize` Modifikator entweder im Viewer-Vorgabendatensatz im Scene7 Publishing System festlegen oder ihn explizit mit dem Viewer-Initialisierungscode mit der `params` Sammlung oder als API-Aufruf, wie im Abschnitt &quot;Befehlsreferenz&quot;beschrieben, übergeben. Beispiel:

   ```
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. Initialisieren des Viewers

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der `s7viewers.eCatalogSearchViewer` Klasse, geben Sie alle Konfigurationsinformationen an den Konstruktor weiter und rufen Sie `init()` die Methode für eine Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt hat mindestens das `containerId` Feld, das den Namen der Viewer-Container-ID und das verschachtelte `params` JSON-Objekt mit vom Viewer unterstützten Konfigurationsparametern enthält. In diesem Fall muss für das `params` Objekt mindestens die Image Serving-URL als `serverUrl` -Eigenschaft und das ursprüngliche Asset als `asset` -Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und Beginn erstellen.

   Es ist wichtig, dass der Viewer-Container dem DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser zögern die Erstellung von DOM bis zum Ende der Webseite. Um eine maximale Kompatibilität zu gewährleisten, rufen Sie die `init()` Methode jedoch direkt vor dem schließenden `BODY` Tag oder im Body- `onload()` Ereignis auf.

   Gleichzeitig sollte das Container-Element nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mithilfe des ihr zugewiesenen `display:none` Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der notwendigen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()` Methode. Im Beispiel wird davon ausgegangen, dass `eCatalogSearchViewer` es sich um die Viewer-Instanz handelt. der Name `s7viewer` des Platzhalters `DIV`; ist `http://s7d1.scene7.com/is/image/` die Image Serving-URL und `Viewers/Pluralist` das Asset:

   ```
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, die den E-Katalog-Search Viewer mit einer festen Größe einbettet:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "searchserverurl":"http://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsive Design-Einbettung mit unbeschränkter Höhe**

Bei der Integration reaktionsfähiger Designs verfügt die Webseite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers vorgibt `DIV`. Für dieses Beispiel nehmen Sie an, dass der Container des Viewers auf der Webseite 40 % der Fenstergröße des Webbrowsers `DIV` annehmen kann, wobei die Höhe unbegrenzt bleibt. Der resultierende HTML-Code der Webseite sieht wie folgt aus:

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

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Container-DIV.
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind identisch mit denen der Einbettung in fester Größe. Hinzufügen den Container `DIV` zum bestehenden Inhaber `DIV`. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Die folgende Beispielseite zeigt die aktuelleren Anwendungsfälle für reaktionsfähiges Design-Einbetten mit uneingeschränkter Höhe:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**Einbettung flexibler Größe mit definierter Breite und Höhe**

Bei Einbettung in flexibler Größe mit definierter Breite und Höhe ist der Webseitenstil anders. Das heißt, es bietet dem Inhaber beide Größen `DIV` und zentriert ihn im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und des `BODY` Elements auf 100 %:

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Einbetten mithilfe der Setter-basierten API**

Anstatt JSON-basierte Initialisierung zu verwenden, ist es möglich, set-basierte API- und no-args-Konstruktoren zu verwenden. Mit diesem API-Konstruktor werden keine Parameter verwendet und Konfigurationsparameter werden mit `setContainerId()`, `setParam()`und `setAsset()` API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt Einbettung in feste Größe mit setter-basierter API:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "http://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```

