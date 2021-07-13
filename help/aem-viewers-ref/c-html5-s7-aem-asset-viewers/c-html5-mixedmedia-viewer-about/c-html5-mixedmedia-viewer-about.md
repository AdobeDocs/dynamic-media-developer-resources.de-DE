---
description: Der Viewer für gemischte Medien ist ein Medien-Viewer. Es unterstützt Mediensets, die Bilder, Mustersets, Rotationssets, Videos und adaptive Videosets enthalten.
keywords: responsiv
solution: Experience Manager
title: Gemischte Medien
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2662'
ht-degree: 0%

---

# Gemischte Medien{#mixed-media}

Der Viewer für gemischte Medien ist ein Medien-Viewer. Es unterstützt Mediensets, die Bilder, Mustersets, Rotationssets, Videos und adaptive Videosets enthalten.

Eine Miniaturansicht am unteren Rand des Viewers stellt jedes Medienset-Element zusammen mit seiner Asset-Typ-Anzeige dar. Wenn ein Musterset-Element ausgewählt ist, wird eine sekundäre Zeile von Farbmustern angezeigt, um die Auswahl von Farbvarianten innerhalb des Mustersets zu ermöglichen. Bilder und Musterset-Elemente unterstützen das Zoomen im kontinuierlichen oder Inline-Modus. Rotationssets unterstützen sowohl Zoomen als auch Spinnen. Videos und adaptive Videosets unterstützen alle grundlegenden Wiedergabesteuerelemente, solange optionale Untertitel über dem Videoinhalt angezeigt werden. Benutzer können jederzeit zum Vollbildmodus wechseln, indem sie auf die Schaltfläche für den Vollbildmodus klicken. Der Viewer verfügt über eine optionale Schaltfläche zum Schließen. Es wurde für Desktops und Mobilgeräte entwickelt.

Der Viewer für gemischte Medien verwendet die HTML5-Streaming-Videowiedergabe im HLS-Format in der Standardkonfiguration, wenn das zugrunde liegende System dies unterstützt. Auf Systemen, die HTML5-Streaming nicht unterstützen, greift der Viewer auf die progressive HTML5-Videobereitstellung zurück.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ 505.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Verwenden des Viewer für gemischte Medien {#section-f21ac23d3f6449ad9765588d69584772}

Der Viewer für gemischte Medien stellt eine JavaScript-Hauptdatei und eine Reihe von Hilfedateien dar (ein einzelnes JavaScript-Include mit allen Viewer-SDK-Komponenten, die von diesem Viewer verwendet werden, Assets, CSS), die vom Viewer zur Laufzeit heruntergeladen werden.

Sie können den Viewer für gemischte Medien im Popup-Modus verwenden, indem Sie eine produktionsbereite HTML-Seite verwenden, die mit IS-Viewern bereitgestellt wird. Alternativ können Sie den Viewer im eingebetteten Modus verwenden, wo er mithilfe der dokumentierten API in eine Ziel-Web-Seite integriert wird.

Die Aufgabe, den Viewer zu konfigurieren und zu skizzieren, ähnelt anderen Viewern. Die gesamte Skinning-Funktion wird über benutzerdefiniertes CSS erreicht.

Siehe [Befehlsreferenz für alle Viewer - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Befehlsreferenz für alle Viewer - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit Viewer für gemischte Medien {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Der Viewer für gemischte Medien unterstützt Einkontaktgesten und Multi-Touch-Gesten, die in anderen Mobile Apps gängig sind. Wenn der Viewer die Wischgeste eines Benutzers nicht verarbeiten kann, leitet er das Ereignis an den Webbrowser weiter, um einen nativen Seitenbildlauf durchzuführen. Mit dieser Funktion kann ein Benutzer durch die Seite navigieren, selbst wenn der Viewer den größten Teil des Gerätebildschirms einnimmt.

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
   <td colname="col2"> <p> Aktiviert die Flyout-Ansicht oder Änderungen zwischen dem primären und dem sekundären Zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doppeltippen </p> </td> 
   <td colname="col2"> <p>Wenn im Zoommodus <span class="codeph"> (fortlaufend </span>) eine Ebene vergrößert wird, bis die maximale Vergrößerung erreicht ist, wird die nächste doppelte Tickgeste wieder in den Anfangszustand zurückgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berühren und halten (Touch and hold) </p> </td> 
   <td colname="col2"> <p> Aktiviert im Inline-Modus <span class="codeph"> </span> den Zoommodus das gezoomte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pinch </p> </td> 
   <td colname="col2"> <p>Zoomt das Bild im kontinuierlichen Zoommodus ein- oder aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontales Wischen oder Klick </p> </td> 
   <td colname="col2"> <p> Wenn es sich bei dem aktuellen Asset um ein Rotationsset handelt und sich das Bild in einem Zurücksetzungsstatus befindet, wird es horizontal durch das Rotationsset gedreht. </p> <p> Wenn es sich bei dem aktuellen Asset um ein Rotationsset oder ein Bild handelt und das Bild vergrößert wird, wird das Bild horizontal verschoben. Wenn das Bild an die Ansichtskante verschoben wird und das Wischen weiterhin in diese Richtung erfolgt, führt die Geste einen nativen Seitenbildlauf durch. </p> <p> Scrollt durch die Liste der Farbfelder in der Farbfeldleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Wischen oder Klick </p> </td> 
   <td colname="col2"> <p> Wenn sich das Bild in einem Zurücksetzungsstatus befindet, ändert es den vertikalen Blickwinkel, falls ein mehrdimensionales Rotationsset verwendet wird. In einem eindimensionalen Rotationsset oder wenn sich ein mehrdimensionales Rotationsset auf der letzten oder ersten Achse befindet, sodass das vertikale Wischen nicht zu einer Änderung des vertikalen Blickwinkels führt, führt die Geste einen nativen Seitenbildlauf durch. </p> <p> Wenn es sich bei dem aktuellen Asset um ein Rotationsset oder ein Bild handelt und das Bild vergrößert wird, wird das Bild vertikal verschoben. Wenn das Bild an die Ansichtskante verschoben wird und das Wischen weiterhin in diese Richtung erfolgt, führt die Geste einen nativen Bildlauf durch. </p> <p> Wenn die Geste innerhalb des Farbfeldbereichs ausgeführt wird, führt sie einen nativen Bildlauf durch. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt auch Touch-Eingabe- und Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome-, Internet Explorer 11- und Edge-Webbrowser beschränkt.

Auf diesen Viewer kann vollständig über die Tastatur zugegriffen werden.

Siehe [Barrierefreiheit und Navigation über die Tastatur](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten von Viewer für gemischte Medien {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Webseiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal stellt eine Webseite einen Link bereit, der den Viewer beim Klicken in einem separaten Browser-Fenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt in die Hosting-Seite einzubetten. In letzterem Fall kann die Webseite ein statisches Seitenlayout aufweisen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diese Anforderungen zu erfüllen, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung fester Größe und Einbettung responsiver Designs.

## Über den Popup-Modus {#section-77d5aa03b8b94566958a179b1a2cd474}

Im Popup-Modus wird der Viewer in einem separaten Webbrowser-Fenster oder einer separaten Registerkarte geöffnet. Es nimmt den gesamten Bereich des Browser-Fensters und passt sich an, falls die Größe des Browsers geändert wird oder die Ausrichtung eines Mobilgeräts geändert wird.

Der Pop-up-Modus ist der häufigste für Mobilgeräte. Die Webseite lädt den Viewer mit dem JavaScript-Aufruf `window.open()`, dem ordnungsgemäß konfigurierten HTML-Element `A` oder einer anderen geeigneten Methode.

Es wird empfohlen, eine vordefinierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. In diesem Fall wird sie [!DNL MixedMediaViewer.html] genannt und befindet sich im Unterordner [!DNL html5/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Sie können visuelle Anpassungen durch Anwendung von benutzerdefiniertem CSS erreichen.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Über die Einbettung von fester Größe und responsivem Design {#section-ec86b100ba5943d0b16694268520bbde}

Im eingebetteten Modus wird der Viewer der vorhandenen Webseite hinzugefügt, die möglicherweise bereits über Kundeninhalte verfügt, die nicht mit dem Viewer in Verbindung stehen. Der Viewer belegt normalerweise nur einen Teil der Immobilien einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die auf Desktops oder Tablets ausgerichtet sind, sowie responsive Design-Seiten, auf denen das Layout automatisch an den Gerätetyp angepasst wird.

Die Einbettung fester Größe wird verwendet, wenn die Größe des Viewers nach dem ersten Laden nicht geändert wird. Dies ist die beste Wahl für Webseiten mit statischem Layout.

Responsive Designeinbettung setzt voraus, dass der Viewer die Größe möglicherweise zur Laufzeit ändert, wenn die Größe des Containers `DIV` geändert wird. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Webseite, die ein flexibles Seitenlayout verwendet.

Im Einbettungsmodus für responsive Designs verhält sich der Viewer unterschiedlich, je nachdem, wie die Größe der Web-Seite für den Container `DIV` angepasst wird. Wenn die Web-Seite nur die Breite des Containers `DIV` festlegt und dabei die Höhe unbegrenzt bleibt, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass die Seiten einen Abstand aufweisen. Dieser Anwendungsfall ist der häufigste bei Webseiten, die responsive Design-Layout-Frameworks wie Bootstrap, Foundation usw. verwenden.

Andernfalls füllt der Viewer, wenn die Web-Seite die Breite und Höhe für den Container des Viewers `DIV` festlegt, nur diesen Bereich und folgt der Größe, die das Layout der Web-Seite bietet. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Überlagerung entsprechend der Fenstergröße des Webbrowsers skaliert wird.

## Einbetten fester Größe {#section-17d162f76ffa4804b27928f51e7bea1d}

Sie fügen den Viewer zu einer Web-Seite hinzu, indem Sie Folgendes ausführen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.
1. Definieren des Containers `DIV`.
1. Festlegen der Viewer-Größe
1. Erstellen und Initialisieren des Viewers.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Webseite.

   Zum Erstellen eines Viewers müssen Sie ein Skript-Tag im HTML-Kopf hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL MixedMediaViewer.js] angeben. Die Datei [!DNL MixedMediaViewer.js] befindet sich im Unterordner [!DNL html5/js/] Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und von derselben Domäne aus bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
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
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Viewer-Größe festlegen

   Dieser Viewer zeigt Miniaturansichten bei der Arbeit mit Sets für mehrere Elemente an. Auf Desktop-Systemen werden Miniaturansichten unter der Hauptansicht platziert. Gleichzeitig ermöglicht der Viewer den Austausch des Haupt-Assets während der Laufzeit mithilfe der `setAsset()`-API. Als Entwickler haben Sie die Kontrolle darüber, wie der Viewer den Bereich &quot;Miniaturansichten&quot;am unteren Rand verwaltet, wenn das neue Asset nur ein Element enthält. Es ist möglich, die Größe des äußeren Viewers intakt zu halten und die Größe der Hauptansicht zu erhöhen und den Bereich der Miniaturansichten zu belassen. Alternativ können Sie die Größe der Hauptansicht statisch halten und den äußeren Viewer-Bereich reduzieren, den Webseiteninhalt nach oben verschieben und dann die freie Seiteneigenschaft verwenden, die von den Miniaturansichten weg gelassen wird.

   Um die äußeren Viewer-Grenzen intakt zu halten, definieren Sie die Größe für die CSS-Klasse der obersten Ebene `.s7mixedmediaviewer` in absoluten Einheiten. Die Größe in CSS kann direkt auf der HTML-Seite oder in einer benutzerdefinierten Viewer-CSS-Datei festgelegt werden, die später in Dynamic Media Classic einem Viewer-Vorgabendatensatz zugewiesen oder explizit mithilfe des Stilbefehls übergeben wird.

   Weitere Informationen zum Formatieren des Viewers mit CSS finden Sie unter [Anpassen des Viewers für gemischte Medien](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) .

   Im Folgenden finden Sie ein Beispiel für die Definition der statischen äußeren Viewer-Größe in einer HTML-Seite:

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können das Verhalten mit einem festen äußeren Viewer-Bereich auf der folgenden Beispielseite sehen. Beachten Sie, dass sich die äußere Viewer-Größe beim Wechsel zwischen Sets nicht ändert:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html)

   Um die Hauptansichtsdimensionen statisch zu machen, definieren Sie die Viewer-Größe in absoluten Einheiten für die innere SDK-Komponente `Container` mit dem CSS-Selektor `.s7mixedmediaviewer .s7container` oder mit dem Modifikator `stagesize` .

   Im Folgenden finden Sie ein Beispiel für die Definition der Viewer-Größe für die innere SDK-Komponente `Container`, sodass der Hauptansichtsbereich beim Wechseln des Assets seine Größe nicht ändert:

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Die folgende Beispielseite zeigt das Viewer-Verhalten mit einer festen Hauptansichtsgröße. Beachten Sie, dass beim Wechseln zwischen Sets die Hauptansicht statisch bleibt und der Webseiteninhalt vertikal verschoben wird:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html)

   Sie können den Modifikator `stagesize` entweder im Viewer-Vorgabendatensatz in Dynamic Media Classic festlegen oder explizit mit der Viewer-Initialisierungscode-Sammlung `params` oder als API-Aufruf übergeben, wie im Abschnitt Befehlsreferenz dieser Hilfe beschrieben:

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Es wird ein CSS-basierter Ansatz empfohlen, der in diesem Beispiel verwendet wird.

1. Erstellen und Initialisieren des Viewers.

   Wenn Sie die oben genannten Schritte ausgeführt haben, erstellen Sie eine Instanz der Klasse `s7viewers.MixedMediaViewer`, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen die Methode `init()` in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID enthält und das verschachtelte `params` JSON-Objekt mit Konfigurationsparametern enthält, die vom Viewer unterstützt werden. In diesem Fall muss für das `params`-Objekt mindestens die Image Serving-URL als `serverUrl`-Eigenschaft übergeben werden, die Video-Server-URL als `videoserverurl`-Eigenschaft und das erste Asset als `asset`-Parameter. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzelnen Codezeile erstellen und starten.

   Der Viewer-Container muss dem DOM hinzugefügt werden, damit der Viewer-Code das Container-Element anhand seiner Kennung finden kann. Einige Browser verzögern das Erstellen von DOM bis zum Ende der Webseite. Rufen Sie für maximale Kompatibilität die `init()`-Methode direkt vor dem schließenden `BODY`-Tag oder das `onload()`-Ereignis im Hauptteil auf.

   Gleichzeitig sollte das Containerelement nicht unbedingt erst noch Teil des Webseitenlayouts sein. Sie kann beispielsweise mit dem `display:none`-Stil ausgeblendet werden, der ihm zugewiesen ist. In diesem Fall verzögert der Viewer den Initialisierungsprozess so lange, bis die Webseite das Containerelement wieder in das Layout bringt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()`-Methode. Das Beispiel geht davon aus, dass `mixedMediaViewer` die Viewer-Instanz ist. `s7viewer` ist der Name des Platzhalters `DIV`; [!DNL http://s7d1.scene7.com/is/image/] ist die Image Serving-URL; [!DNL http://s7d1.scene7.com/is/content/] ist die Videoserver-URL; und [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] das Asset ist:

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

Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den Viewer für gemischte Medien mit einer festen Größe einbettet:

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

## Responsives Einbetten mit unbeschränkter Höhe {#section-056cb574713c4d07be6d07cf3c598839}

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

Die folgende Beispielseite zeigt die reale Nutzung responsiver Designs, die mit unbegrenzter Höhe eingebettet werden:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demostandort](https://experienceleague.adobe.com/tools/vlist/vlist.html)

## Flexible Größeneinbettung mit definierter Breite und Höhe {#section-0a329016f9414d199039776645c693de}

Bei der Einbettung in flexibler Größe mit definierter Breite und Höhe unterscheidet sich der Webseitenstil. Es stellt beide Größen für den DIV `"holder"` bereit und zentriert ihn im Browserfenster. Außerdem setzt die Webseite die Größe des Elements `HTML` und `BODY` auf 100 Prozent.

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

Die übrigen Schritte zum Einbetten sind mit den Schritten für responsives Design identisch, das mit uneingeschränkter Höhe eingebettet wird. Das folgende Beispiel zeigt:

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

## Einbetten mit der Setter-basierten API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Statt eine JSON-basierte Initialisierung zu verwenden, ist es möglich, setter-basierte API und den no-args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors werden keine Parameter verwendet und Konfigurationsparameter werden mit den API-Methoden `setContainerId()`, `setParam()` und `setAsset()` mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Verwendung der Einbettung fester Größe in eine setter-basierte API:

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
