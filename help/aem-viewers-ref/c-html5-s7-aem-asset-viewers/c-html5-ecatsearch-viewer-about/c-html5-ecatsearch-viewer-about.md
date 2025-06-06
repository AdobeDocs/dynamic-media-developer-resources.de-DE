---
description: eCatalog Search Viewer ist ein Katalog-Viewer, der elektronische Broschüren in einer Spread by Spread oder Seite für Seite anzeigt. Mit eCatalog können Benutzer mithilfe zusätzlicher Elemente der Benutzeroberfläche oder des dedizierten Miniaturbildmodus durch den Katalog navigieren. Benutzer können auch auf jede Seite zoomen, um mehr Details zu erhalten.
keywords: Responsiv
solution: Experience Manager
title: E-Katalog-Suche
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2078'
ht-degree: 0%

---

# E-Katalog-Suche{#ecatalog-search}

eCatalog Search Viewer ist ein Katalog-Viewer, der elektronische Broschüren in einer Spread by Spread oder Seite für Seite anzeigt. Mit eCatalog können Benutzer mithilfe zusätzlicher Elemente der Benutzeroberfläche oder des dedizierten Miniaturbildmodus durch den Katalog navigieren. Benutzer können auch auf jede Seite zoomen, um mehr Details zu erhalten.

Dieser Viewer arbeitet mit E-Katalogen und unterstützt optionale Imagemaps und Tools für die Freigabe in sozialen Netzwerken. Es verfügt über Zoom-Tools, Katalog-Navigations-Tools, Vollbildunterstützung, Miniaturansichten und eine optionale Schaltfläche zum Schließen. Der Viewer unterstützt auch Tools zur gemeinsamen Nutzung in sozialen Netzwerken sowie die Optionen Drucken, Herunterladen und Favoriten. Es wurde für Desktop-PCs und mobile Geräte entwickelt.

Der Benutzer kann auch eine schlüsselwort- oder textpasswortbasierte Suche über die Kataloginhalte durchführen.

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

Viewer-Typ 513.

Siehe [Systemanforderungen und Voraussetzungen](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo-URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/)

## Verwenden des E-Katalog-Viewers {#section-e6c68406ecdc4de781df182bbd8088b4}

Der eCatalog Search Viewer stellt eine JavaScript-Hauptdatei und einen Satz Hilfsdateien (ein einziges JavaScript Include mit allen Viewer-SDK-Komponenten, die von diesem bestimmten Viewer verwendet werden, Assets, CSS) dar, die vom Viewer zur Laufzeit heruntergeladen wurden

Sie können den eCatalog Search Viewer im Popup-Modus mit einer produktionsbereiten HTML-Seite verwenden, die mit IS-Viewers bereitgestellt wird, oder im eingebetteten Modus, wo er mithilfe der dokumentierten API in die Ziel-Web-Seite integriert wird.

Konfiguration und Skinning sind mit denen der anderen Viewer vergleichbar. Die gesamte Skin-Verwaltung erfolgt über benutzerdefiniertes CSS.

Siehe [Für alle Viewer gemeinsame Befehlsreferenz - Konfigurationsattribute](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) und [Für alle Viewer gemeinsame Befehlsreferenz - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interagieren mit dem E-Katalog-Such-Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

Der E-Katalog-Such-Viewer unterstützt die folgenden Touch-Gesten, die in anderen Mobile Apps üblich sind.

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
   <td colname="col2"> <p> Wählt neue Miniaturen in Farbfeldern aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doppeltippen </p> </td> 
   <td colname="col2"> <p> Zoomt in eine Ebene, bis die maximale Vergrößerung erreicht ist. Mit der nächsten Doppeltipp-Geste wird der Viewer auf den anfänglichen Anzeigestatus zurückgesetzt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zwicker </p> </td> 
   <td colname="col2"> <p>Zoomt ein oder aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Horizontales Wischen oder Schnipsen </p> </td> 
   <td colname="col2"> <p>Scrollt durch die Liste der Katalogseiten, wenn ein Folienrahmenübergang verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vertikales Streichen oder Ziehen </p> </td> 
   <td colname="col2"> <p>Wenn sich das Bild im zurückgesetzten Zustand befindet, wird ein nativer Seitenscroll durchgeführt. </p> <p>Wenn Miniaturen aktiv sind, wird die Liste der Miniaturen gescrollt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Es ist möglich, einen realistischen Animationseffekt zum Spiegeln der Seite für die Navigation zwischen Katalogseiten zu aktivieren. In solchen Fällen kann ein Benutzer die Ecke einer Seite gedrückt halten und ziehen und die Seite umdrehen.

Dieser Viewer unterstützt auch Touch-Eingaben und Mauseingaben auf Windows-Geräten mit Touchscreen und Maus. Diese Unterstützung ist jedoch auf Chrome, Internet Explorer 11 und Edge-Webbrowser beschränkt.

## Tools zur Freigabe in Social Media mit dem E-Katalog-Such-Viewer {#section-eb575084a99647c3a9591f439f40b412}

Der E-Katalog-Such-Viewer unterstützt Tools zur gemeinsamen Nutzung in sozialen Netzwerken. Sie sind als Schaltfläche in der Hauptsteuerleiste verfügbar, die sich zu einer Freigabesymbolleiste erweitert, wenn Benutzende darauf klicken oder tippen.

Die Freigabesymbolleiste enthält Symbole für jeden unterstützten Freigabekanaltyp, einschließlich Facebook, Twitter, E-Mail-Freigabe, Einbettungs-Code-Freigabe und Link-Freigabe. Wenn die Tools E-Mail-Freigabe, Einbettungsfreigabe oder Linkfreigabe aktiviert sind, zeigt der Viewer ein modales Dialogfeld mit einem entsprechenden Dateneingabeformular an. Wenn Facebook oder Twitter aufgerufen wird, leitet der Viewer den Benutzer von einem Social-Media-Service zu einem Standarddialogfeld für die Freigabe um. Freigabetools sind aufgrund von Sicherheitsbeschränkungen des Webbrowsers nicht im Vollbildmodus verfügbar.

Die Suchfunktion des Viewers ist als Lookglass-Symbol in der Hauptsymbolleiste verfügbar. Durch Klicken oder Tippen auf das Symbol wird das Suchfeld mit einem Eingabefeld aktiviert. Nach Eingabe eines Keywords oder einer Phrase und Drücken der Eingabetaste rendert der Viewer Suchergebnisse im Bedienfeld und markiert gefundene Wörter in der Hauptansicht.

## Einbetten des E-Katalog-Such-Viewers {#section-6bb5d3c502544ad18a58eafe12a13435}

Verschiedene Web-Seiten haben unterschiedliche Anforderungen an das Viewer-Verhalten. Manchmal enthält eine Web-Seite einen Link, der bei Auswahl den Viewer in einem separaten Browser-Fenster öffnet. In anderen Fällen ist es erforderlich, den Viewer direkt in die Hosting-Seite einzubetten. Im letzteren Fall kann die Web-Seite über ein statisches Seiten-Layout verfügen oder ein responsives Design verwenden, das auf verschiedenen Geräten oder für verschiedene Browser-Fenstergrößen unterschiedlich angezeigt wird. Um diesen Anforderungen gerecht zu werden, unterstützt der Viewer drei primäre Betriebsmodi: Popup, Einbettung mit fester Größe und Einbetten von responsivem Design.

**Über den Popup-Modus**

Im Popup-Modus wird der Viewer in einem separaten Fenster oder einer separaten Registerkarte des Webbrowsers geöffnet. Sie nimmt den gesamten Browser-Fensterbereich und passt sich an, falls die Größe des Browsers geändert oder die Ausrichtung eines Mobilgeräts geändert wird.

Der Popup-Modus ist der gängigste für Mobilgeräte. Die Web-Seite lädt den Viewer mithilfe `window.open()` JavaScript-Aufrufs, eines ordnungsgemäß konfigurierten HTML-Elements `A` einer anderen geeigneten Methode.

Es wird empfohlen, eine vorkonfigurierte HTML-Seite für den Popup-Betriebsmodus zu verwenden. In diesem Fall wird sie als [!DNL eCatalogSearchViewer.html] bezeichnet und befindet sich im [!DNL html5/] Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

Sie können die visuelle Anpassung erreichen, indem Sie benutzerdefiniertes CSS anwenden.

Im Folgenden finden Sie ein Beispiel für HTML-Code, der den Viewer in einem neuen Fenster öffnet:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**Über den Einbettungsmodus für feste Größe und den Einbettungsmodus für responsives Design**

Im eingebetteten Modus wird der Viewer zur vorhandenen Web-Seite hinzugefügt, die möglicherweise bereits einige Kundeninhalte enthält, die nicht mit dem Viewer verknüpft sind. Der Viewer belegt normalerweise nur einen Teil des Grundbesitzes einer Web-Seite.

Die wichtigsten Anwendungsfälle sind Web-Seiten, die für Desktops oder Tablet-Geräte ausgerichtet sind, sowie responsive Design-Seiten, deren Layout automatisch an den Gerätetyp angepasst wird.

Einbetten in fester Größe wird verwendet, wenn der Viewer seine Größe nach dem ersten Laden nicht ändert. Dies ist die beste Wahl für Web-Seiten mit statischem Layout.

Beim Einbetten des responsiven Designs wird davon ausgegangen, dass der Viewer zur Laufzeit je nach Größenänderung seiner Container-`DIV` möglicherweise die Größe ändern muss. Der häufigste Anwendungsfall ist das Hinzufügen eines Viewers zu einer Web-Seite, die ein flexibles Seiten-Layout verwendet.

Im responsiven Design-Einbettungsmodus verhält sich der Viewer unterschiedlich, je nachdem, wie die Größe der Web-Seite seinen Container-`DIV` bestimmt. Wenn die Web-Seite nur die Breite des Container-`DIV` festlegt und seine Höhe nicht eingeschränkt wird, wählt der Viewer automatisch seine Höhe entsprechend dem Seitenverhältnis des verwendeten Assets aus. Diese Funktion stellt sicher, dass das Asset perfekt in die Ansicht passt, ohne dass an den Seiten ein Abstand vorhanden ist. Dieser Anwendungsfall ist der häufigste bei Web-Seiten, die responsive Layout-Frameworks wie Bootstrap, Foundation usw. verwenden.

Wenn die Web-Seite jedoch sowohl die Breite als auch die Höhe für die Container-`DIV` des Viewers festlegt, füllt der Viewer nur diesen Bereich aus und folgt der Größe, die das Web-Seiten-Layout bereitstellt. Ein gutes Beispiel ist das Einbetten des Viewers in eine modale Überlagerung, bei der die Größe der Überlagerung an die Fenstergröße des Webbrowsers angepasst ist.

**Einbetten in fester Größe**

Sie können den Viewer wie folgt zu einer Web-Seite hinzufügen:

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Definieren des Container-DIV.
1. Festlegen der Viewer-Größe.
1. Viewer erstellen und initialisieren.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.

   Zum Erstellen eines Viewers müssen Sie dem HTML-Head ein Script-Tag hinzufügen. Bevor Sie die Viewer-API verwenden können, stellen Sie sicher, dass Sie [!DNL eCatalogSearchViewer.js] einbeziehen. Die [!DNL eCatalogSearchViewer.js]-Datei befindet sich im [!DNL html5/js/] Unterordner Ihrer standardmäßigen IS-Viewers-Bereitstellung:

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

Sie können einen relativen Pfad verwenden, wenn der Viewer auf einem der Adobe-Dynamic Media-Server bereitgestellt wird und er von derselben Domain bereitgestellt wird. Andernfalls geben Sie einen vollständigen Pfad zu einem der Adobe-Dynamic Media-Server an, auf denen die IS-Viewer installiert sind.

Der relative Pfad sieht wie folgt aus:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. Definieren des Container-DIV.

   Fügen Sie der Seite, auf der der Viewer angezeigt werden soll, ein leeres DIV-Element hinzu. Für das DIV-Element muss eine ID definiert sein, da diese ID später an die Viewer-API übergeben wird.

   Das Platzhalter-DIV ist ein positioniertes Element, d. h. die `position` CSS-Eigenschaft ist auf `relative` oder `absolute` festgelegt.

   Im Folgenden finden Sie ein Beispiel für ein definiertes Platzhalter-DIV-Element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Festlegen der Viewer-Größe

   Sie können die statische Größe für den Viewer festlegen, indem Sie sie entweder für `.s7ecatalogsearchviewer` CSS-Klasse der obersten Ebene in absoluten Einheiten deklarieren oder `stagesize` Modifikator verwenden.

   Sie können die Größenanpassung in CSS direkt auf der HTML-Seite oder in einer benutzerdefinierten CSS-Viewer-Datei festlegen, die dann später einem Viewer-Vorgabeneintrag in Dynamic Media Classic zugewiesen oder explizit mit einem Stilbefehl übergeben wird.

   Weitere Informationen [ Formatieren des Viewers mit CSS finden Sie unter ](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0)Anpassen des E-Katalog-Viewers .

   Im Folgenden finden Sie ein Beispiel für die Definition einer statischen Viewer-Größe auf einer HTML-Seite:

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Sie können den `stagesize`-Modifikator entweder im Viewer-Vorgabeneintrag in Dynamic Media Classic festlegen oder ihn explizit mit dem Viewer-Initialisierungscode mit `params` Sammlung oder als API-Aufruf wie im Abschnitt Befehlsreferenz beschrieben übergeben, wie im Folgenden beschrieben:

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. Initialisieren des Viewers.

   Wenn Sie die obigen Schritte ausgeführt haben, erstellen Sie eine Instanz `s7viewers.eCatalogSearchViewer` Klasse, übergeben alle Konfigurationsinformationen an ihren Konstruktor und rufen `init()` Methode in einer Viewer-Instanz auf. Konfigurationsinformationen werden als JSON-Objekt an den Konstruktor übergeben. Dieses Objekt hat mindestens das Feld `containerId` , das den Namen der Viewer-Container-ID enthält und `params` JSON-Objekt mit Konfigurationsparametern verschachtelt ist, die vom Viewer unterstützt werden. In diesem Fall muss für das `params`-Objekt mindestens die Bildbereitstellungs-URL als `serverUrl`-Eigenschaft übergeben werden und das anfängliche Asset muss `asset` Parameter sein. Mit der JSON-basierten Initialisierungs-API können Sie den Viewer mit einer einzigen Codezeile erstellen und starten.

   Es ist wichtig, dass der Viewer-Container zum DOM hinzugefügt wird, damit der Viewer-Code das Container-Element anhand seiner ID finden kann. Einige Browser verzögern die Erstellung von DOM bis zum Ende der Web-Seite. Um maximale Kompatibilität zu erzielen, rufen Sie jedoch die `init()`-Methode kurz vor dem schließenden `BODY`-Tag oder im body-`onload()`-Ereignis auf.

   Gleichzeitig sollte das Container-Element noch nicht unbedingt Teil des Web-Seiten-Layouts sein. Beispielsweise kann sie mithilfe `display:none` ihr zugewiesenen Stils ausgeblendet werden. In diesem Fall verzögert der Viewer den Initialisierungsprozess bis zu dem Moment, an dem die Web-Seite das Container-Element wieder zum Layout zurückbringt. In diesem Fall wird das Laden des Viewers automatisch fortgesetzt.

   Im Folgenden finden Sie ein Beispiel für das Erstellen einer Viewer-Instanz, das Übergeben der erforderlichen Mindestkonfigurationsoptionen an den Konstruktor und das Aufrufen der `init()`-Methode. Im Beispiel wird davon ausgegangen, `eCatalogSearchViewer` die Viewer-Instanz ist. `s7viewer` ist der Name des Platzhalters `DIV`. `https://s7d1.scene7.com/is/image/` ist die Bildbereitstellungs-URL und `Viewers/Pluralist` ist das Asset:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite, die den E-Katalog-Such-Viewer mit einer festen Größe einbettet:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Responsives Design mit unbegrenzter Höhe**

Beim Einbetten eines responsiven Designs verfügt die Web-Seite normalerweise über ein flexibles Layout, das die Laufzeitgröße der Container-`DIV` des Viewers bestimmt. Nehmen wir für die Zwecke dieses Beispiels an, dass die Web-Seite dem Container-`DIV` des Viewers ermöglicht, 40 % der Fenstergröße des Webbrowsers zu verwenden, wobei seine Höhe nicht beschränkt wird. Der resultierende HTML-Code der Web-Seite sieht wie folgt aus:

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

Das Hinzufügen des Viewers zu einer solchen Seite ähnelt dem Einbetten in fester Größe, mit dem einzigen Unterschied, dass Sie die Viewer-Größe nicht explizit definieren müssen.

1. Hinzufügen der Viewer-JavaScript-Datei zu Ihrer Web-Seite.
1. Definieren des Container-DIV.
1. Viewer erstellen und initialisieren.

Alle oben genannten Schritte sind dieselben wie bei der Einbettung in fester Größe. Fügen Sie die Container-`DIV` zum vorhandenen `DIV` „Halter“ hinzu. Der folgende Code ist ein vollständiges Beispiel. Sie können sehen, wie sich die Viewer-Größe ändert, wenn der Browser skaliert wird, und wie das Seitenverhältnis des Viewers mit dem Asset übereinstimmt.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Die folgende Beispielseite zeigt weitere Anwendungsfälle responsiven Designs mit unbegrenzter Höhe in der Praxis:

[Live-Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Flexible Einbettung mit definierter Breite und Höhe**

Bei Einbettungen mit flexibler Größe und definierter Breite und Höhe ist der Web-Seiten-Stil anders. Das heißt, sie stellt dem `DIV` „Halter“ beide Größen zur Verfügung und zentriert ihn im Browser-Fenster. Außerdem legt die Web-Seite die Größe des `HTML`- und `BODY` auf 100 % fest:

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
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Einbetten mithilfe der Setter-basierten API**

Anstelle der Verwendung der JSON-basierten Initialisierung ist es möglich, eine Setter-basierte API und einen Nicht-Args-Konstruktor zu verwenden. Bei diesem API-Konstruktor übernimmt kein Parameter und Konfigurationsparameter werden mithilfe von `setContainerId()`-, `setParam()`- und `setAsset()`-API-Methoden mit separaten JavaScript-Aufrufen angegeben.

Das folgende Beispiel zeigt die Einbettung fester Größe mit einer Setter-basierten API:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
eCatalogSearchViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "https://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```
