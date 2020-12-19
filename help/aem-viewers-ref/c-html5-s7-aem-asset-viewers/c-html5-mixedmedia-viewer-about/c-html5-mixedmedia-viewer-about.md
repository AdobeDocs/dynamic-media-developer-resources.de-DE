---
description: Der Viewer für gemischte Medien ist ein Medien-Viewer. Es unterstützt Mediensets, die Bilder, Mustersets, Rotationssets, Videos und adaptive Videosets enthalten.
keywords: responsive
seo-description: Der Viewer für gemischte Medien ist ein Medien-Viewer. Es unterstützt Mediensets, die Bilder, Mustersets, Rotationssets, Videos und adaptive Videosets enthalten.
seo-title: Gemischte Medien
solution: Experience Manager
title: Gemischte Medien
topic: Dynamic media
uuid: b6028c54-7a3c-41eb-89f8-7b86bb0d0deb
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2681'
ht-degree: 0%

---


# Gemischte Medien{#mixed-media}

Der Viewer für gemischte Medien ist ein Medien-Viewer. Es unterstützt Mediensets, die Bilder, Mustersets, Rotationssets, Videos und adaptive Videosets enthalten.

Eine Miniaturansicht am unteren Rand des Viewers stellt jedes Medienset-Element zusammen mit seiner Asset-Typanzeige dar. Wenn ein Musterset-Element ausgewählt ist, wird eine zweite Zeile mit Farbfeldern angezeigt, um die Auswahl der Farbvariation innerhalb des Mustersets zu ermöglichen. Bilder und Musterset-Elemente unterstützen das Zoomen im kontinuierlichen oder inline-Modus. Rotationssets unterstützen sowohl Zoomen als auch Spinnen. Videos und adaptive Videosets unterstützen alle grundlegenden Steuerelemente für die Wiedergabe, solange optionale Untertitel über dem Videoinhalt angezeigt werden. Ein Benutzer kann jederzeit durch Klicken auf die Schaltfläche im Vollbildmodus zum Vollbildmodus wechseln. Der Viewer verfügt über eine optionale Schaltfläche zum Schließen. Es wurde für den Einsatz auf Desktop- und Mobilgeräten entwickelt.

Der Viewer für gemischte Medien verwendet HTML5-Streaming-Videowiedergabe im HLS-Format in seiner Standardkonfiguration, wenn das zugrunde liegende System dies unterstützt. Auf Systemen, die kein HTML5-Streaming unterstützen, greift der Viewer auf den progressiven HTML5-Versand zurück.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ 505.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Verwenden des gemischten Media Viewers {#section-f21ac23d3f6449ad9765588d69584772}

Der Viewer für gemischte Medien stellt eine Haupt-JavaScript-Datei und eine Reihe von Hilfedateien dar (ein einzelnes JavaScript enthält alle Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Sie können den Viewer für gemischte Medien im Popup-Modus verwenden, indem Sie eine produktionsfertige HTML-Seite verwenden, die mit IS-Viewern bereitgestellt wird. Oder Sie können den Viewer im eingebetteten Modus verwenden, wo er mithilfe der dokumentierten API in eine Zielgruppe-Webseite integriert ist.

Die Aufgabe, den Viewer zu konfigurieren und Skins zu erstellen, ähnelt der anderer Viewer. Alle Skins werden mithilfe von benutzerdefiniertem CSS erreicht.

Siehe [Befehlsreferenz, die allen Viewern gemein ist - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz, die allen Viewern gemein ist - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaktion mit dem gemischten MedienViewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Der gemischte Media Viewer unterstützt Single-Touch- und Multi-Touch-Gesten, die in anderen Mobilanwendungen häufig vorkommen. Wenn der Viewer die Blättergeste eines Benutzers nicht verarbeiten kann, leitet er das Ereignis an den Webbrowser weiter, um einen nativen Seitenbildlauf durchzuführen. Mit dieser Funktion kann ein Benutzer durch die Seite navigieren, selbst wenn der Viewer den größten Teil des Gerätebildschirms einnimmt.

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
   <td colname="col2"> <p> Aktiviert die Flyout-Ansicht oder Änderungen zwischen dem primären und dem sekundären Zoomgrad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dublette Tippen </p> </td> 
   <td colname="col2"> <p>Wenn der Zoommodus im kontinuierlichen <span class="codeph">-Modus </span> eine Ebene vergrößert wird, bis die maximale Vergrößerung erreicht ist, wird die Geste zum Tippen auf die nächste Dublette auf den Ausgangszustand zurückgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berühren und halten (Touch and hold) </p> </td> 
   <td colname="col2"> <p> Aktiviert im Inline-Zoommodus <span class="codeph"> das gezoomte Bild.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinch </p> </td> 
   <td colname="col2"> <p>Vergrößert oder verkleinert das Bild im kontinuierlichen Zoommodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontale Blättergeste oder Flick </p> </td> 
   <td colname="col2"> <p> Wenn es sich bei dem aktuellen Asset um ein Rotationsset handelt und das Bild sich in einem Reset-Zustand befindet, wird es horizontal durch das Rotationsset gedreht. </p> <p> Wenn das aktuelle Asset ein Rotationsset oder ein Bild ist und das Bild vergrößert wird, wird es horizontal verschoben. Wenn das Bild an die Kante der Ansicht verschoben wird und die Blättergeste weiterhin in dieser Richtung erfolgt, führt die Geste einen nativen Seitenbildlauf durch. </p> <p> Blättert durch die Liste der Farbfelder in der Farbfeldleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Wischen oder Klick </p> </td> 
   <td colname="col2"> <p> Wenn sich das Bild in einem Reset-Zustand befindet, ändert es den Winkel der vertikalen Ansicht, falls ein mehrdimensionales Rotationsset verwendet wird. In einem eindimensionalen Rotationsset oder wenn sich ein mehrdimensionales Rotationsset auf der letzten oder ersten Achse befindet, sodass die vertikale Blättergeste nicht zu einer Änderung des vertikalen Ansicht-Winkels führt, führt die Geste einen nativen Seitenbildlauf durch. </p> <p> Wenn es sich bei dem aktuellen Asset um ein Rotationsset oder ein Bild handelt und das Bild vergrößert wird, wird das Bild vertikal verschoben. Wenn das Bild an den Rand der Ansicht verschoben wird und das Blättern weiterhin in dieser Richtung erfolgt, führt die Geste einen nativen Seitenbildlauf durch. </p> <p> Wenn die Geste innerhalb des Farbfeldbereichs erfolgt, führt sie einen nativen Seitenbildlauf durch. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt auch die Eingabe per Touch- und Mausklick auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf die Webbrowser Chrome, Internet Explorer 11 und Edge beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Barrierefreiheit und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten von gemischten Medien-Viewern {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, über den der Viewer bei einem Klick in einem separaten Browserfenster geöffnet wird. In anderen Fällen ist es erforderlich, den Viewer direkt auf der Hostingseite einzubetten. Im letzteren Fall verfügt die Webseite möglicherweise über ein statisches Seitenlayout oder über ein reaktionsfähiges Design, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung in fester Größe und Einbettung in reaktionsfähiges Design.

## Popup-Modus {#section-77d5aa03b8b94566958a179b1a2cd474}

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Browserfenster-Bereich und passt sich an, falls die Größe des Browsers oder die Ausrichtung des Mobilgeräts geändert wird.

Der Popupmodus ist der häufigste für Mobilgeräte. Die Webseite lädt den Viewer mit dem JavaScript-Aufruf `window.open()`, dem ordnungsgemäß konfigurierten `A` HTML-Element oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. In diesem Fall wird es als [!DNL MixedMediaViewer.html] bezeichnet und befindet sich im Unterordner [!DNL html5/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erzielen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, mit dem der Viewer in einem neuen Fenster geöffnet wird:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Informationen zur Einbettung fester und reaktionsfähiger Designs {#section-ec86b100ba5943d0b16694268520bbde}

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer zusammenhängen. Der Viewer belegt normalerweise nur einen Teil der Immobilie einer Webseite.

Die wichtigsten Anwendungsfälle sind Webseiten, die auf Desktop- oder Tablet-Geräte ausgerichtet sind, sowie reaktionsfähige Designseiten, die das Layout automatisch an den Gerätetyp anpassen.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Dies ist die beste Wahl für Webseiten mit einem statischen Layout.

Bei der responsiven Designeinbettung wird davon ausgegangen, dass die Größe des Viewers zur Laufzeit entsprechend der Größenänderung des Containers `DIV` ggf. angepasst werden muss. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für reaktionsfähiges Design verhält sich der Viewer je nach Größe des Containers `DIV` der Webseite unterschiedlich. Wenn auf der Webseite nur die Breite des Containers `DIV` festgelegt wird und die Höhe nicht eingeschränkt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass es an den Seiten aufgefüllt werden muss. Dieser Anwendungsfall ist der häufigste Fall für Webseiten mit reaktionsfähigen Layoutrahmen wie Bootstrap, Foundation usw.

Andernfalls füllt der Viewer, wenn die Webseite sowohl die Breite als auch die Höhe des Containers des Viewers `DIV` festlegt, nur diesen Bereich und folgt der vom Webseitenlayout bereitgestellten Größe. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung je nach Webbrowser-Fenstergröße angepasst wird.

## Einbettung fester Größe {#section-17d162f76ffa4804b27928f51e7bea1d}

Der Viewer wird wie folgt zu einer Webseite hinzugefügt:

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite
1. Definieren des Containers `DIV`.
1. Einstellen der Viewer-Größe.
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der JavaScript-Datei für den Viewer zur Webseite

   Zum Erstellen eines Viewers müssen Sie im HTML-Kopf ein Skript-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL MixedMediaViewer.js] einschließen. Die Datei [!DNL MixedMediaViewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Scene7-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem Adobe Scene7-Server an, auf dem die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Sie sollten nur auf die JavaScript-Hauptdatei des Viewers `include` auf Ihrer Seite verweisen. Sie sollten keine weiteren JavaScript-Dateien im Webseitencode referenzieren, die möglicherweise von der Logik des Viewers zur Laufzeit heruntergeladen werden. Insbesondere sollten Sie nicht direkt auf die HTML5 SDK `Utils.js`-Bibliothek verweisen, die vom Viewer aus dem Kontextpfad `/s7viewers` geladen wird (so genanntes konsolidiertes SDK `include`). Der Grund dafür ist, dass der Speicherort von `Utils.js`- oder ähnlichen Laufzeit-Viewer-Bibliotheken vollständig durch die Logik des Viewers verwaltet wird und sich der Speicherort zwischen den Viewer-Versionen ändert. Ältere Versionen des sekundären Viewers `includes` werden von der Adobe nicht auf dem Server gespeichert.
>
>
>Infolgedessen wird die Viewer-Funktionalität bei der Bereitstellung einer neuen Produktversion durch die direkte Referenz auf sekundäres JavaScript `include`, das vom Viewer auf der Seite verwendet wird, in Zukunft unterbrochen.

1. Definieren des Container-DIV.

   hinzufügen ein leeres DIV-Element auf die Seite, auf der der Viewer angezeigt werden soll. Die ID des DIV-Elements muss definiert sein, da diese ID später an die Viewer-API übergeben wird. Die DIV-Größe wird durch CSS festgelegt.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h., die CSS-Eigenschaft ist auf `position` oder `relative` eingestellt.`absolute`

   Stellen Sie sicher, dass die Vollbildfunktion in Internet Explorer ordnungsgemäß funktioniert. Vergewissern Sie sich, dass keine anderen Elemente im DOM eine höhere Stapelreihenfolge aufweisen als das Platzhalter-DIV.

   Das folgende Beispiel zeigt ein definiertes Platzhalter-DIV-Element:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Einstellen der Viewer-Größe

   In diesem Viewer werden Miniaturansichten angezeigt, wenn Sie mit Sets mit mehreren Elementen arbeiten. Auf Desktop-Systemen werden Miniaturansichten unterhalb der Hauptversion der Ansicht platziert. Gleichzeitig ermöglicht der Viewer den Austausch des Hauptassets während der Laufzeit mit der API `setAsset()`. Als Entwickler haben Sie die Kontrolle darüber, wie der Viewer den Bereich &quot;Miniaturansichten&quot;unten verwaltet, wenn das neue Asset nur ein Element enthält. Es ist möglich, die Größe des äußeren Viewers beizubehalten und die Haupthöhe der Ansicht zu erhöhen und den Bereich der Miniaturansichten zu belassen. Oder Sie können die Größe der Hauptversion statisch beibehalten und den äußeren Viewer-Bereich reduzieren, damit der Inhalt der Ansicht nach oben verschoben werden kann, und dann die freie Seitenposition verwenden, die von den Miniaturbildern entfernt wird.

   Um die äußeren Viewer-Grenzen intakt zu halten, definieren Sie die Größe der CSS-Klasse der obersten Ebene in absoluten Einheiten. `.s7mixedmediaviewer` Die Größe in CSS kann direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festgelegt werden, die später im Scene7 Publishing System einem Viewer-Vorgabendatensatz zugewiesen oder explizit mit dem Stilbefehl übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Viewers für gemischte Medien](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4).

   Das folgende Beispiel zeigt die Definition der statischen äußeren Viewer-Größe in einer HTML-Seite:

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können das Verhalten mit einem festen äußeren Viewer-Bereich auf der folgenden Beispielseite sehen. Beachten Sie, dass sich die Größe des äußeren Viewers beim Wechseln zwischen den Sets nicht ändert:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   Um die Hauptabmessungen der Ansicht statisch zu machen, definieren Sie die Viewer-Größe in absoluten Maßeinheiten für die innere Komponente `Container` SDK mit dem CSS-Selektor `.s7mixedmediaviewer .s7container` oder mit dem Modifikator `stagesize`.

   Im Folgenden sehen Sie ein Beispiel für die Definition der Viewer-Größe für die innere SDK-Komponente `Container`, sodass der Hauptbereich &quot;Ansicht&quot;beim Wechseln des Assets seine Größe nicht ändert:

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Die folgende Beispielseite zeigt das Viewer-Verhalten mit einer festen Größe für die Haupt-Ansicht. Beachten Sie, dass beim Wechseln zwischen Sets die Hauptinhalt-Ansicht statisch bleibt und der Webseiteninhalt vertikal verschoben wird:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   Sie können den Modifikator `stagesize` entweder im Viewer-Vorgabendatensatz im Scene7 Publishing System festlegen oder ihn explizit mit der `params`-Sammlung an den Viewer-Initialisierungscode übergeben oder als API-Aufruf, wie im Abschnitt &quot;Befehlsreferenz&quot;dieser Hilfe beschrieben, wie im Folgenden dargestellt:

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.MixedMediaViewer`, geben Sie alle Konfigurationsinformationen an den Konstruktor weiter und rufen Sie die Methode `init()` für eine Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID und das verschachtelte `params`-JSON-Objekt mit den vom Viewer unterstützten Konfigurationsparametern enthält. In diesem Fall muss für das `params`-Objekt mindestens die Image Serving-URL als `serverUrl`-Eigenschaft, die Video-Server-URL als `videoserverurl`-Eigenschaft und das erste Asset als `asset`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und Beginn erstellen.

   Es ist wichtig, dass der Viewer-Container dem DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser zögern die Erstellung von DOM bis zum Ende der Webseite. Um eine maximale Kompatibilität zu gewährleisten, rufen Sie die `init()`-Methode direkt vor dem schließenden `BODY`-Tag oder im Body `onload()`-Ereignis auf.

   Gleichzeitig sollte das Container-Element nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mit dem `display:none`-Stil ausgeblendet werden, der ihm zugewiesen wurde. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Zeitpunkt, zu dem die Webseite das Container-Element wieder in das Layout zurückführt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der notwendigen Mindestkonfigurationsoptionen an den Konstruktor und Aufrufen der `init()`-Methode. Das Beispiel geht davon aus, dass `mixedMediaViewer` die Viewer-Instanz ist. `s7viewer` ist der Name des Platzhalters `DIV`; [!DNL http://s7d1.scene7.com/is/image/] ist die Image Serving-URL; [!DNL http://s7d1.scene7.com/is/content/] ist die URL des Videoservers; und [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] ist das Asset:

```
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, die den gemischten MedienViewer mit einer festen Größe einbettet:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Responsive Einbettung mit unbeschränkter Höhe {#section-056cb574713c4d07be6d07cf3c598839}

Bei der Integration reaktionsfähiger Designs verfügt die Webseite normalerweise über ein flexibles Layout, das die Laufzeitgröße des Containers des Viewers `DIV` vorgibt. Im folgenden Beispiel nehmen Sie an, dass die Webseite dem Container des Viewers `DIV` erlaubt, 40 % der Größe des Webbrowser-Fensters zu übernehmen, wobei die Höhe unbegrenzt bleibt. Der HTML-Code der Webseite würde wie folgt aussehen:

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
1. Erstellen und Initialisieren des Viewers.

Alle oben genannten Schritte sind identisch mit denen der Einbettung in fester Größe. hinzufügen Sie den Container DIV an das vorhandene `"holder"` DIV. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn die Größe des Browsers geändert wird, und wie das Viewer-Seitenverhältnis mit dem Asset übereinstimmt.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Die folgende Beispielseite zeigt die aktuelleren Einsatzmöglichkeiten von reaktionsfähigem Design-Einbettung mit uneingeschränkter Höhe:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Einbetten flexibler Größe mit definierter Breite und Höhe {#section-0a329016f9414d199039776645c693de}

Bei Einbettung in flexibler Größe mit definierter Breite und Höhe ist der Webseitenstil anders. Es stellt beide Größen für das DIV `"holder"` bereit und zentriert es im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und `BODY` auf 100 Prozent.

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

Die übrigen Einbettungsschritte sind identisch mit den Schritten, die für die Einbettung von reaktionsfähigem Design mit uneingeschränkter Höhe verwendet werden. Das resultierende Beispiel lautet:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Einbetten mit Setter-basierter API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Anstatt JSON-basierte Initialisierung zu verwenden, ist es möglich, set-basierte API- und no-args-Konstruktoren zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` und mit separaten JavaScript-Aufrufen angegeben.

Im folgenden Beispiel wird die Einbettung in feste Größe mit setter-basierter API veranschaulicht:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```

