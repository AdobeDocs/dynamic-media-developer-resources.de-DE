---
title: Gemischte Medien
description: „Viewer für gemischte Medien“ ist ein Medien-Viewer. Sie unterstützt Mediensets, die Bilder, Mustersets, Rotationssets, Videos und adaptive Videosets enthalten.
keywords: Responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2581'
ht-degree: 0%

---

# Gemischte Medien{#mixed-media}

„Viewer für gemischte Medien“ ist ein Medien-Viewer. Sie unterstützt Mediensets, die Bilder, Mustersets, Rotationssets, Videos und adaptive Videosets enthalten.

Eine Miniaturansicht am unteren Rand des Viewers stellt jedes Medienset-Element zusammen mit seiner Asset-Typanzeige dar. Wenn ein Farbfeldset-Element ausgewählt wird, wird eine sekundäre Reihe von Farbfeldern angezeigt, um die Auswahl von Farbvarianten innerhalb des Farbfeldsets zu ermöglichen. Bilder und Farbfeldsatzelemente unterstützen das Zoomen im kontinuierlichen oder Inline-Modus. Rotationssets unterstützen sowohl Zoomen als auch Drehen. Videos und adaptive Videosets unterstützen alle grundlegenden Wiedergabesteuerelemente , solange optionale verdeckte Untertitel über dem Videoinhalt angezeigt werden. Ein Benutzer kann jederzeit zum Vollbildmodus wechseln, indem er auf die Schaltfläche für den Vollbildmodus klickt. Der Viewer verfügt über eine optionale Schaltfläche Schließen . Es wurde für Desktop-PCs und mobile Geräte entwickelt.

Der Viewer für gemischte Medien verwendet HTML5-Streaming-Videowiedergabe im HLS-Format in der Standardkonfiguration, wenn das zugrunde liegende System dies unterstützt. Auf Systemen, die HTML5-Streaming nicht unterstützen, wird der Viewer auf die progressive HTML5-Videobereitstellung zurückgesetzt.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ 505.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Verwenden des Viewers für gemischte Medien {#section-f21ac23d3f6449ad9765588d69584772}

Der Viewer für gemischte Medien stellt eine JavaScript-Hauptdatei und einen Satz Hilfsdateien (ein einzelnes JavaScript-Include mit allen Viewer-SDK-Komponenten, die von diesem bestimmten Viewer verwendet werden, Assets, CSS) dar, die vom Viewer zur Laufzeit heruntergeladen wurden.

Sie können den Viewer für gemischte Medien im Popup-Modus verwenden, indem Sie die produktionsbereite HTML-Seite verwenden, die mit IS-Viewers bereitgestellt wird. Sie können den Viewer auch im eingebetteten Modus verwenden, in dem er mithilfe der dokumentierten API in eine Ziel-Web-Seite integriert wird.

Die Aufgabe der Konfiguration und Skin-Verwaltung des Viewers ist ähnlich wie bei anderen Viewern. Die gesamte Skin-Verwaltung erfolgt über benutzerdefiniertes CSS.

Siehe [Für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Für alle Viewer gemeinsame Befehlsreferenz - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem Viewer für gemischte Medien {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Der gemischte Medien-Viewer unterstützt Single-Touch- und Multi-Touch-Gesten, die in anderen Mobile Apps üblich sind. Wenn der Viewer die Wischgeste eines Benutzers nicht verarbeiten kann, leitet er das Ereignis an den Webbrowser weiter, um einen nativen Seitenscroll durchzuführen. Mit dieser Funktion kann ein Benutzer durch die Seite navigieren, auch wenn der Viewer den größten Teil des Gerätebildbereichs einnimmt.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geste </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Einfaches Tippen </p> </td> 
   <td colname="col2"> <p> Aktiviert die Flyout-Ansicht oder wechselt zwischen primärer und sekundärer Zoom-Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doppeltippen </p> </td> 
   <td colname="col2"> <p>Wenn Sie <span class="codeph"> kontinuierlichen </span>-Zoom-Modus in einer Ebene zoomen, bis die maximale Vergrößerung erreicht ist, wird die nächste Doppeltipp-Geste auf den Anfangsstatus zurückgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Berühren und halten (Touch and hold) </p> </td> 
   <td colname="col2"> <p> Im Inline<span class="codeph"></span>Zoom-Modus wird das gezoomte Bild aktiviert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zwicker </p> </td> 
   <td colname="col2"> <p>Im kontinuierlichen Zoom-Modus zoomt das Bild ein oder aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontales Wischen oder Schnipsen </p> </td> 
   <td colname="col2"> <p> Wenn es sich bei dem aktuellen Asset um ein Rotationsset handelt und sich das Bild im zurückgesetzten Zustand befindet, wird es horizontal durch das Rotationsset rotiert. </p> <p> Wenn es sich bei dem aktuellen Asset um ein Rotationsset oder Bild handelt und das Bild vergrößert ist, wird das Bild horizontal verschoben. Wenn das Bild an den Ansichtsrand verschoben und weiterhin in diese Richtung gewischt wird, führt die Geste einen nativen Seitenscroll durch. </p> <p> Scrollt durch die Liste der Farbfelder in der Farbfeldleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Streichen oder Ziehen </p> </td> 
   <td colname="col2"> <p> Wenn sich das Bild im zurückgesetzten Zustand befindet, ändert es den vertikalen Ansichtswinkel, falls ein mehrdimensionales Rotationsset verwendet wird. In einem eindimensionalen Rotationsset oder wenn sich ein mehrdimensionales Rotationsset auf der letzten oder ersten Achse befindet, sodass das vertikale Wischen nicht zu einer Änderung des vertikalen Ansichtswinkels führt, führt die Geste einen nativen Seitenscroll durch. </p> <p> Wenn es sich bei dem aktuellen Asset um ein Rotationsset oder Bild handelt und das Bild vergrößert ist, wird das Bild vertikal verschoben. Wenn das Bild an den Ansichtsrand verschoben und weiterhin in diese Richtung gewischt wird, führt die Geste einen nativen Seitenscroll durch. </p> <p> Wenn die Geste innerhalb des Farbfeldbereichs ausgeführt wird, wird ein nativer Seitenscroll durchgeführt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Viewer unterstützt auch Touch-Eingabe und Mauseingabe auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.

Dieser Viewer ist vollständig mit der Tastatur zugänglich.

Siehe [Tastaturzugriff und Navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Einbetten des Viewers für gemischte Medien {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Web-Seiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal enthält eine Web-Seite einen Link, der bei Auswahl den Viewer in einem separaten Browser-Fenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt in die Hosting-Seite einzubetten. Im letzteren Fall kann die Web-Seite über ein statisches Seiten-Layout verfügen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diesen Anforderungen gerecht zu werden, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung mit fester Größe und Einbetten von responsivem Design.

## Über den Popup-Modus {#section-77d5aa03b8b94566958a179b1a2cd474}

Im Popup-Modus wird der Viewer in einem separaten Fenster oder einer separaten Registerkarte des Webbrowsers geöffnet. Sie nimmt den gesamten Browser-Fensterbereich und passt sich an, falls die Größe des Browsers geändert oder die Ausrichtung eines Mobilgeräts geändert wird.

Der Popup-Modus ist der gängigste für Mobilgeräte. Die Web-Seite lädt den Viewer mithilfe `window.open()` JavaScript-Aufrufs, eines ordnungsgemäß konfigurierten HTML-Elements `A` einer anderen geeigneten Methode.

Es wird empfohlen, eine vorkonfigurierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. In diesem Fall wird sie als [!DNL MixedMediaViewer.html] bezeichnet und befindet sich im [!DNL html5/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Sie können die visuelle Anpassung erreichen, indem Sie benutzerdefiniertes CSS anwenden.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Über die Einbettung in festes Format und responsives Design {#section-ec86b100ba5943d0b16694268520bbde}

Im eingebetteten Modus wird der Viewer zur vorhandenen Web-Seite hinzugefügt, die möglicherweise bereits einige Kundeninhalte enthält, die nicht mit dem Viewer verknüpft sind. Der Viewer belegt normalerweise nur einen Teil des Grundbesitzes einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die für Desktops oder Tablet-Geräte ausgerichtet sind, sowie responsive Design-Seiten, deren Layout automatisch an den Gerätetyp angepasst wird.

Einbetten in fester Größe wird verwendet, wenn der Viewer seine Größe nach dem ersten Laden nicht ändert. Diese Aktion ist die beste Wahl für Web-Seiten mit statischem Layout.

Beim Einbetten eines responsiven Designs wird davon ausgegangen, dass die Größe des Viewers zur Laufzeit entsprechend der Größenänderung seiner Container-`DIV` geändert werden muss. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Web-Seite, die ein flexibles Seiten-Layout verwendet.

Im responsiven Design-Einbettungsmodus verhält sich der Viewer unterschiedlich, je nachdem, wie die Größe der Web-Seite seinen Container-`DIV` bestimmt. Wenn die Web-Seite nur die Breite des Container-`DIV` festlegt und seine Höhe nicht eingeschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass an den Seiten ein Abstand vorhanden ist. Dieser Anwendungsfall ist der häufigste bei Web-Seiten, die responsive Design-Layout-Frameworks wie Bootstrap oder Foundation verwenden.

Wenn die Web-Seite jedoch sowohl die Breite als auch die Höhe für die Container-`DIV` des Viewers festlegt, füllt der Viewer nur diesen Bereich aus und folgt der Größe, die das Web-Seiten-Layout bereitstellt. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung an die Fenstergröße des Webbrowsers angepasst ist.

## Einbettung mit fester Größe {#section-17d162f76ffa4804b27928f51e7bea1d}

Sie können den Viewer wie folgt zu einer Web-Seite hinzufügen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Container-`DIV` definieren.
1. Festlegen der Viewer-Größe.
1. Viewer erstellen und initialisieren.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.

   Zum Erstellen eines Viewers müssen Sie dem HTML-Head ein Script-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL MixedMediaViewer.js] einbeziehen. Die [!DNL MixedMediaViewer.js]-Datei befindet sich im [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewers-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe Dynamic Media Classic-Server bereitgestellt wird und er von derselben Domain bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe Dynamic Media Classic-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
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
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Festlegen der Viewer-Größe

   Dieser Viewer zeigt Miniaturen bei der Arbeit mit Sets mit mehreren Elementen an. Auf Desktop-Systemen werden Miniaturansichten unter der Hauptansicht platziert. Gleichzeitig ermöglicht der Viewer den Austausch des Haupt-Assets während der Laufzeit mithilfe `setAsset()` API. Als Entwickler haben Sie die Kontrolle darüber, wie der Viewer den Bereich Miniaturen unten verwaltet, wenn das neue Asset nur ein Element enthält. Es ist möglich, die äußere Viewer-Größe intakt zu halten und die Hauptansicht ihre Höhe erhöhen und den Bereich für Miniaturen belegen zu lassen. Sie können auch die Größe der Hauptansicht unverändert lassen und den äußeren Viewer-Bereich reduzieren, sodass der Webseiteninhalt nach oben verschoben wird. Verwenden Sie dann die kostenlose Immobilienseite, die von den Miniaturansichten übrig bleibt.

   Um die äußeren Viewer-Grenzen intakt zu halten, definieren Sie die Größe für `.s7mixedmediaviewer` CSS-Klasse der obersten Ebene in absoluten Einheiten. Die Größe in CSS kann direkt auf der HTML-Seite oder in einer benutzerdefinierten CSS-Viewer-Datei festgelegt und später einem Viewer-Vorgabeneintrag in Dynamic Media Classic zugewiesen oder explizit mit dem Stilbefehl übergeben werden.

   Weitere [ zum Formatieren des Viewers mit CSS finden Sie unter „Anpassen ](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) Viewers für gemischte Medien“.

   Im Folgenden finden Sie ein Beispiel für die Definition der statischen äußeren Viewer-Größe auf einer HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können das Verhalten mit einem festen äußeren Viewer-Bereich auf der folgenden Beispielseite sehen. Beachten Sie, dass sich beim Wechseln zwischen Sets die Größe des äußeren Viewers nicht ändert:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=de](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=de)

   Um die Hauptansichtsdimensionen statisch zu machen, definieren Sie die Viewer-Größe in absoluten Einheiten für die SDK-Komponente des inneren `Container` mithilfe `.s7mixedmediaviewer .s7container` CSS-Selektors oder mithilfe `stagesize` Modifikators.

   Im Folgenden finden Sie ein Beispiel dafür, wie Sie die Viewer-Größe für die SDK-Komponente des inneren `Container` definieren, sodass der Hauptansichtsbereich beim Wechseln des Assets seine Größe nicht ändert:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Die folgende Beispielseite zeigt das Viewer-Verhalten mit einer festen Hauptansichtsgröße. Beachten Sie, dass beim Wechseln zwischen Sets die Hauptansicht statisch bleibt und der Webseiteninhalt vertikal verschoben wird:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=de](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=de)

   Sie können den `stagesize`-Modifikator entweder im Viewer-Vorgabeneintrag in Dynamic Media Classic festlegen oder ihn explizit mit dem Viewer-Initialisierungs-Code mit `params` Sammlung übergeben. Oder rufen Sie als API-Aufruf wie im Abschnitt Befehlsreferenz dieser Hilfe beschrieben auf, wie in der folgenden Abbildung dargestellt:

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Ein CSS-basierter Ansatz wird empfohlen und wird in diesem Beispiel verwendet.

1. Viewer erstellen und initialisieren.

   Wenn Sie die obigen Schritte ausgeführt haben, erstellen Sie eine Instanz `s7viewers.MixedMediaViewer` Klasse, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen `init()` Methode in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt sollte mindestens über das Feld `containerId` verfügen, das den Namen der Viewer-Container-ID enthält und `params` JSON-Objekt mit Konfigurationsparametern verschachtelt ist, die der Viewer unterstützt. In diesem Fall muss für das `params`-Objekt mindestens die Bildbereitstellungs-URL als `serverUrl`-Eigenschaft, die Videoserver-URL als `videoserverurl`-Eigenschaft und das anfängliche Asset als `asset`-Parameter übergeben werden. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzigen Codezeile erstellen und starten.

   Es ist wichtig, dass der Viewer-Container zum DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser verzögern die Erstellung von DOM bis zum Ende der Web-Seite. Um maximale Kompatibilität zu erzielen, rufen Sie die `init()`-Methode unmittelbar vor dem schließenden `BODY`-Tag oder im body-`onload()` auf.

   Gleichzeitig sollte das Container-Element noch nicht unbedingt Teil des Web-Seiten-Layouts sein. Beispielsweise kann sie mithilfe `display:none` ihr zugewiesenen Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Moment, an dem die Web-Seite das Container-Element wieder zum Layout zurückbringt. Wenn diese Aktion stattfindet, wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()`-Methode. Im Beispiel wird davon ausgegangen, `mixedMediaViewer` die Viewer-Instanz ist; `s7viewer` der Name des Platzhalters `DIV` ist; [!DNL http://s7d1.scene7.com/is/image/] die Bildbereitstellungs-URL ist; [!DNL http://s7d1.scene7.com/is/content/] die Videoserver-URL ist; und [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] das Asset ist:

```html {.line-numbers}
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

Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, auf der der Viewer für gemischte Medien mit einer festen Größe eingebettet ist:

```html {.line-numbers}
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

## Responsives Einbetten mit unbegrenzter Höhe {#section-056cb574713c4d07be6d07cf3c598839}

Beim Einbetten eines responsiven Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße der Container-`DIV` des Viewers bestimmt. Nehmen wir für das folgende Beispiel an, dass die Web-Seite dem Container-`DIV` des Viewers ermöglicht, 40 % der Fenstergröße des Webbrowsers zu verwenden, wobei seine Höhe nicht beschränkt wird. Der Web-Seiten-HTML-Code würde wie folgt aussehen:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt den Schritten für Einbetten in fester Größe. Der einzige Unterschied besteht darin, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Definieren des Container-DIV.
1. Viewer erstellen und initialisieren.

Alle oben genannten Schritte sind dieselben wie bei der Einbettung in fester Größe. Fügen Sie das Container-DIV zum vorhandenen `"holder"`-DIV hinzu. Der folgende Code ist ein vollständiges Beispiel. Beachten Sie, wie sich die Viewer-Größe ändert, wenn der Browser skaliert wird, und wie das Seitenverhältnis des Viewers mit dem Asset übereinstimmt.

```html {.line-numbers}
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

Die folgende Beispielseite zeigt weitere reale Verwendungen der responsiven Designeinbettung mit unbegrenzter Höhe:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Alternativer Demo-Speicherort](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=de)

## Flexible Einbettungsgröße mit definierter Breite und Höhe {#section-0a329016f9414d199039776645c693de}

Wenn es Einbettungen in flexibler Größe gibt, bei denen Breite und Höhe definiert sind, ist der Web-Seiten-Stil anders. Es stellt dem `"holder"`-DIV beide Größen zur Verfügung und zentriert ihn im Browser-Fenster. Außerdem legt die Web-Seite die Größe des `HTML`- und `BODY` auf 100 Prozent fest.

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

Die restlichen Einbettungsschritte sind identisch mit den Schritten für responsive Designeinbettung mit unbegrenzter Höhe. Das daraus resultierende Beispiel lautet:

```html {.line-numbers}
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

## Einbetten mithilfe der Setter-basierten API {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Anstatt die JSON-basierte Initialisierung zu verwenden, ist es möglich, eine Setter-basierte API und einen Nicht-Args-Konstruktor zu verwenden. Bei Verwendung dieses API-Konstruktors sind keine Parameter erforderlich und Konfigurationsparameter werden mithilfe von `setContainerId()`-, `setParam()`- und `setAsset()`-API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel veranschaulicht die Verwendung der Einbettung fester Größe mit einer Setter-basierten API:

```html {.line-numbers}
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
