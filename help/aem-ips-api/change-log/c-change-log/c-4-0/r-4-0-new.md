---
description: Beschreibt neue und implementierte Änderungen an der IPS-API, Version 4.0.
seo-description: Beschreibt neue und implementierte Änderungen an der IPS-API, Version 4.0.
seo-title: Neue Hinzufügungen und Änderungen
solution: Experience Manager
title: Neue Hinzufügungen und Änderungen
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 2%

---


# Neue Hinzufügungen und Änderungen{#new-additions-and-changes}

Beschreibt neue und implementierte Änderungen an der IPS-API, Version 4.0.

Implementierte Versionen von nebeneinander liegenden APIs mit separaten WSDLs und Schema-Namensräumen.

* Frühere API-Versionen: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0-Version: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Das Feld `PostScriptOptions/alpha` wurde hinzugefügt.

Die Eigenschaften `VideoRootUrl` und `SwfRootUrl` für `getProperty` wurden hinzugefügt.

Es wurden optionale Parameter `appName` und `appVersion` zu `authHeader` hinzugefügt, um aufrufende Anwendungen zu verfolgen. Protokollierung zu `ipsApiService.log` hinzugefügt.

Es wurde ein optionaler Parameter `serviceUrl` zum WSDL-Generierungsservlet hinzugefügt. Dies ist besonders beim Debugging von Proxys nützlich. Beispiel: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Der Vorgang `getZipEntries` wurde implementiert.

Implementierung von Suchbereichen und eingegebenen Vergleichswerten für Systemfeldbedingungen.

Die Stringkonstante `'Asset'` des Asset-Typs wurde hinzugefügt, um in erster Linie Asset-übergreifende Metadatenfelder zuzulassen.

Implementierung von `trashState` param für `searchAssets`.

Der Vorgang `getAssetPublishHistory` wurde implementiert.

Der optionale SOAP-Header `faultHttpStatusCode` wurde hinzugefügt, um die Fehlerbearbeitung in Flex zu aktivieren. Verwenden Sie für Flex `<faultHttpStatusCode>200</faultHttpStatusCode>`. Der Standardstatuscode für Fehlerantworten ist `500 (Internal Server Error)`.

Es wurden Vorgänge zum Wiederherstellen von Assets aus dem Papierkorb und leere Assets aus dem Papierkorb hinzugefügt.

Implementierung von CRUD-Operationen.

Das Flag enabled wurde zum Vorgang `ImageMap` und `saveImageMap` hinzugefügt.

Unterstützung für Aufträge zur Optimierung der verbleibenden Dateien hinzugefügt.

`setAssetsPublishState` für Massenaktualisierungen im Veröffentlichungsstatus hinzugefügt.

`ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings` hinzugefügt.

Veraltete `saveMetadataField`-Operation zu Gunsten neuer `createMetadataField`- und `updateMetadataField`-Vorgänge.

Vorgang zum Löschen von Stapeln wurde implementiert.`deleteAssetsParam`

Der Stapelverschiebungsvorgang wurde implementiert.`moveAssetsParam`

Der Vorgang `deleteMetadataField` wurde implementiert.

Implementierte Vorgänge `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat`.

Implementiert `getAssetCounts`.

Unterstützung für `setImageSetMembers` zur Aufnahme von `RenderSet`-Mitgliedern in `ImageSet`-Assets hinzugefügt.

Der Vorgang `replaceImage` wurde hinzugefügt.

Der Vorgang `copyImage` wurde hinzugefügt.

Der Vorgang `setUrlModifier` und die Felder `urlModifier/urlPostApplyModifier` für `LayerViewInfo`, `TemplateInfo` und `WatermarkInfo` wurden hinzugefügt.

Der Vorgang `createDerivedAsset` wurde hinzugefügt. Derzeit muss `ownerHandle` auf ein Bild-Asset verweisen und der Typ kann `AdjustedView` oder `LayerView` sein.

Der Vorgang `createTemplate` wurde hinzugefügt. Derzeit kann dies aufgerufen werden, um Vorlagen- oder Wasserzeichenelemente zu erstellen.

IPS-Firma-Einstellungen, `CompanySettings`, auf Web-Services-API portiert.

Das Filter-Flag `excludeByproducts` wurde dem Vorgang `searchAssets` hinzugefügt. Wenn Sie dieses Flag auf &quot;true&quot;setzen, werden `PSDlayer`-Bilder und gerippte PDF-Bilder ausgeführt.

Der Vorgang `getGenerationInfo` wurde hinzugefügt.

Der Operation `SystemMessage` wurde der Eigenschaftsname `getProperty` hinzugefügt.

Es wurden einige Zeichenfolgenkonstanten des Elementtyps entsprechend den entsprechenden Feldern für Asset-Informationen geändert.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Das Ergebnisformat von Stapelvorgängen wurde geändert, um den Erfolg, Warnungen und Fehler zusammenzufassen.

Der Vorgang für Stapelmetadaten wurde implementiert.`batchSetAssetMetadata`

Implementierte Unterstützung für App-spezifische Daten.

Unterstützung für boolesche Flags für `createTemplate`, `extendLayers` und `extractText` für Upload-Aufträge zur Steuerung der Photoshop-Verarbeitung implementiert (ähnlich wie bei Änderungen beim Hochladen von Dateien).

Die Vorgänge `setImageMaps` und `setZoomTargets` wurden implementiert.

Implementierte Vorgänge `ViewerPreset`. Die erkannten Typen sind:

* `VideoPlayer` (Video veröffentlicht diese Viewer nur.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Viewer-Skins unterstützen zwei Parameter: `skinFg` und `skinBg`. Backend-Code führt die gesamte erforderliche Verarbeitung aus, um die Abwärtskompatibilität zu gewährleisten.

Der Vorgang `getAssociatedAssets` wurde implementiert.

Der Auftragstyp `ReprocessAssets` wurde hinzugefügt, um die erneute Verarbeitung zuvor hochgeladener Primärquelldateien zu ermöglichen, einschließlich des Abschneidens von PDFs und der Neuoptimierung von Bildern.

Der Feldtyp wurde in `PropertySetType` in `propertyType` umbenannt. Dies betrifft den Parameter `createPropertySetType` und die Antwort `getPropertySetType/getPropertySetTypes`.

Der Vorgang `batchSetImageFields` wurde implementiert, um das Festlegen von Bildbenutzerdaten und anderen bearbeitbaren Bildfeldern zu unterstützen.

47 Das Feld fileSize wurde verschiedenen Asset-Info-Typen hinzugefügt:

* `VignetteInfo`
* `CabinetInfo`
* `WindowCoveringInfo`
* `IccProfileInfo`
* `FontInfo`
* `XslInfo`
* `ViewerSwfInfo`
* `XmlInfo`
* `SvgInfo`
* `ZipInfo`
* `VideoInfo`
* `AcoInfo`
* `PdfInfo`
* `PsdInfo`
* `FlashInfo`
* `InDesignInfo`
* `PostScriptInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `IllustratorInfo`
* `WordInfo`
* `ExcelInfo`
* `PowerPointInfo`
* `RTFInfo`

Der Vorgang `getActivePublishContexts` wurde implementiert. Dieser Vorgang gibt ein Array von Veröffentlichungskontextnamen mit aktiven Veröffentlichungsservern für die angegebene Firma zurück. Die Namen der aktuellen Veröffentlichungskontexte lauten:

* `ImageServing`
* `ImageRendering`
* `Video`

Der Vorgang `getSearchStrings` wurde implementiert. Gibt ein Array von Suchzeichenfolgen für das angegebene Asset zurück.

Es wurden Gebietsschema-Parameter für Aufträge und ein Mechanismus zum Festlegen des Gebietsschemas für API-Vorgänge hinzugefügt. Die Zeichenfolge im Gebietsschema sollte als `<language_code>[-<country_code>]` formatiert werden. Der Sprachencode ist ein aus zwei Buchstaben bestehender Code in Kleinbuchstaben gemäß ISO-639, und der optionale Ländercode ist ein aus zwei Buchstaben bestehender Code gemäß ISO-3166.

Der SOAP-Kopfzeile wurde der optionale Parameter locale hinzugefügt, um das Gebietsschema für API-Vorgänge festzulegen. `authHeader` Ist dieser Parameter nicht vorhanden, wird der HTTP-Header `Accept-Language` verwendet. Wenn dieser Header ebenfalls nicht vorhanden ist, wird das Standardgebietsschema für den IPS-Server verwendet.

Unterstützung von get/set für stark typisierte Metadatenfelder hinzugefügt.

Implementierung der SOAP- und HTTP-Header-Unterstützung für gzip-Antwortsteuerung.

`gzipResponse`-Flag zu `authHeader` hinzugefügt. Ist sie nicht vorhanden, prüft die API auch den HTTP `Accept-Encoding`-Header.

Unterstützung für searchAssets für stark typisierte Metadatenfeldbedingungen hinzugefügt.

* Bei allen Feldtypen kann der Wert mit einem Zeichenfolgenvergleichsoperator ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`) übergeben werden.
* Bei booleschen Feldern kann `boolVal` mit der `Equals` op übergeben werden.
* Bei Int-Feldern kann `longVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder `minLong/maxLong` mit einem numerischen Bereichsvorgang ( `Between, NotBetween`) übergeben werden.
* Bei Float-Feldern kann `doubleVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder `minDouble/maxDouble` mit einem numerischen Bereichsvorgang ( `Between, NotBetween`) übergeben werden.
* Bei Datumsfeldern können Sie `dateVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) übergeben oder Sie können minDate/maxDate mit einem numerischen Datumsbereich ( `Between, NotBetween`) übergeben.

Die Felder &quot;`jobSubType`&quot;und &quot;`originalJobName`&quot;wurden dem Typ &quot;`JobLog`&quot;hinzugefügt.

* `originalJobName` ist der Name des Auftrags, an den gesendet wird  `submitJob` (ohne eindeutige Suffixe oder Follower-Auftragsnamen).
* `jobSubType` wird derzeit nur von  `ImageServingPublishJob` Aufträgen verwendet (bei denen es sich um einen von  `full`,  `increment, fullwithsearch,` oder  `fulloverride`) handelt.
* `description` ist derzeit eine leere Zeichenfolge für alle Auftragstypen, enthält jedoch letztendlich Informationen zum Zusammenfassungsauftrag, wie den Upload-Pfad.

Darüber hinaus sind die folgenden Felder nicht sowohl in `getJobLogs` als auch in `getJobLogDetails` enthalten. In früheren Versionen waren sie nur mit `getJobLogDetails` verfügbar.

* `endDate` (wenn der Auftrag abgeschlossen wurde).
* `fileDuplicateCount` (zuvor war es immer  `0` mit  `getJobLogs`)
* `fileUpdateCount` (zuvor war es immer  `0` mit  `getJobLogs` und in enthalten  `fileSuccessCount`; Es wird nun in separate Felder aufgeteilt).

Feld assetHandle wurde zum Typ `JobLogDetail` hinzugefügt.

Optionaler Beschreibungsparameter zu `submitJob` hinzugefügt. Dies wird zum Abrufen in `getScheduledJobs`, `getActiveJobs` und `getJobLogs` weitergeleitet.

Das SKU-Systemfeld wurde überholt. Das Feld wird ignoriert, wenn es als `SystemFieldCondition` an `searchAssets` übergeben wird.

Filter `excludeAssetTypeArray` zu `searchAssets` hinzugefügt.

Der Typ `MaskInfo` wurde zu `Asset` hinzugefügt.

Neue Asset-Typen für die Verwaltung durch IPS hinzugefügt:

<table id="table_DCCE936B797A448598C30E3B344525A5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Asset-Typ </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Illustrator </span> </p> </td> 
   <td colname="col2"> <p>Adobe Illustrator-Datei. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PostScript </span> </p> </td> 
   <td colname="col2"> <p>EPS- und PostScript-Dateien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WordDoc  </span> </p> </td> 
   <td colname="col2"> <p>Microsoft Word-Dokument für Dateien, die mit .doc enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc  </span> </p> </td> 
   <td colname="col2"> <p>Microsoft Excel-Dokument für Dateien, die mit .xls enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc  </span> </p> </td> 
   <td colname="col2"> <p>Microsoft PowerPoint-Dokument für Dateien, die mit .ppt enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc  </span> </p> </td> 
   <td colname="col2"> <p>RTF-Datei für Dateien, die mit .rtf hochgeladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

Es wurden zusätzliche Optionen zu `UploadDirectoryJob` und `UploadUrlsJob` hinzugefügt, um die Verarbeitung von PostScript-, Illustrator- und PDF-Dateien unabhängig zu steuern. Alle bestehenden Aufträge werden die erforderlichen Parameter für jede der drei Verarbeitungsleitungen bereitstellen, damit sie genau wie heute funktionieren. Der ursprüngliche `PostScriptOptions`-Block wird verwendet, um die Verarbeitung für Illustrator- und EPS/PS-Dateien festzulegen. Optional können spezifische Dateioptionenblöcke zur Angabe der Verarbeitung bereitgestellt werden. Die Liste der Änderungen umfasst:

<table id="table_D4E5ACCB2D144D05A5FA0129AA5F9344"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Feld </p> </th> 
   <th colname="col2" class="entry"> <p>Parameter </p> </th> 
   <th colname="col3" class="entry"> <p>Wert </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> verarbeiten </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Keine </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rastern  </span>(Standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Verwalten Sie das Asset nur und erstellen Sie keine Ableitungen beim Hochladen. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Rendern Sie die EPS- und PostScript-Datei in einem Bild mit der vorgeschriebenen Auflösung und dem vorgeschriebenen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesch&gt; </span> </p> </td> 
   <td colname="col4"> <p>Wird beim Rastern der Datei in ein Bild wirksam. Es wird ein transparenter Hintergrund erstellt, wenn die Originaldatei so definiert ist, dass Logos überlagert werden können. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> verarbeiten </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Keine </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rastern  </span> (Standard) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Verwalten Sie das Asset nur und erstellen Sie keine Ableitungen beim Hochladen. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Rendern Sie die Datei in einem Bild mit der vorgeschriebenen Auflösung und dem vorgeschriebenen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Auflösung wird gerastert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Farbraum </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Farbraum der Zielgruppe zum Rendern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha  </span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Dies wirkt sich beim Rastern der Datei in ein Bild aus. Erstellt einen transparenten Hintergrund, wenn die Originaldatei auf diese Weise zum Erstellen von Überlagerungslogos definiert ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> verarbeiten </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Keine </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rastern  </span> (Standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Verwalten Sie das Asset nur und erstellen Sie keine Ableitungen beim Hochladen. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Rendern Sie die Datei in einem Bild mit der vorgeschriebenen Auflösung und dem vorgeschriebenen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Auflösung wird gerastert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Farbraum </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Farbraum der Zielgruppe zum Rendern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesch&gt; </span> </p> </td> 
   <td colname="col4"> <p>Legt fest, ob nach dem Rendern eine mehrseitige PDF-Datei in einen E-Katalog kombiniert werden soll (Standard ist true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesch&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definiert, ob Wörter aus der PDF-Datei zur späteren Bereitstellung an einen Suchserver in die DB extrahiert werden (Standard ist false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können auch von `getScheduledJobs` aus Abfragen ausführen.

Die Konfigurationseigenschaft `webservice.gzip.response` wurde geändert, um einen der folgenden Werte aufzunehmen:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Wert </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nie </span> </p> </td> 
   <td colname="col2"> <p>Keine gzip-Antwort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> soap </span> </p> </td> 
   <td colname="col2"> <p>Gzip-Antwort nur, wenn authHeader/gzipResponse "true"ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> akzeptieren </span> </p> </td> 
   <td colname="col2"> <p>Gzip, wenn authHeader/gzipResponse wahr ist oder kein gzipResponse-Header vorhanden ist und HTTP Accept-Encoding-Header gzip enthält. (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immer </span> </p> </td> 
   <td colname="col2"> <p>Immer gzip-Antwort, unabhängig von Header-Werten. Verwenden Sie diesen Wert nur zum Debugging. </p> </td> 
  </tr> 
 </tbody> 
</table>

