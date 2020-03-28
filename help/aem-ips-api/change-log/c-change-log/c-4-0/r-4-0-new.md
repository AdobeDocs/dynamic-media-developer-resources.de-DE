---
description: Beschreibt neue und implementierte Änderungen an der IPS-API, Version 4.0.
seo-description: Beschreibt neue und implementierte Änderungen an der IPS-API, Version 4.0.
seo-title: Neue Hinzufügungen und Änderungen
solution: Experience Manager
title: Neue Hinzufügungen und Änderungen
topic: Scene7 Image Production System API
uuid: ca4bbe36-c1b7-471f-90a8-6b695d56ac7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Neue Hinzufügungen und Änderungen{#new-additions-and-changes}

Beschreibt neue und implementierte Änderungen an der IPS-API, Version 4.0.

Implementierte Versionen von nebeneinander liegenden APIs mit separaten WSDLs und Schema-Namensräumen.

* Frühere API-Versionen: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0-Version: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Feld `PostScriptOptions/alpha` hinzugefügt.

Es wurden `VideoRootUrl` und `SwfRootUrl` Eigenschaften für den `getProperty` Vorgang hinzugefügt.

Es wurden optionale `appName` und `appVersion` Parameter zur Verfolgung der aufrufenden Anwendung `authHeader` hinzugefügt. Protokollierung zu `ipsApiService.log`.

Es wurde ein optionaler `serviceUrl` Parameter zum Servlet der WSDL-Generation hinzugefügt. Dies ist besonders beim Debugging von Proxys nützlich. Beispiel: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Implementierter `getZipEntries` Vorgang.

Implementierung von Suchbereichen und eingegebenen Vergleichswerten für Systemfeldbedingungen.

Es wurde eine Konstante für die Zeichenfolge `'Asset'` vom Asset-Typ hinzugefügt, die in erster Linie Asset-übergreifende Metadatenfelder zulässt.

Implementierter `trashState` Parameter für `searchAssets`.

Implementierter `getAssetPublishHistory` Vorgang.

Es wurde ein optionaler `faultHttpStatusCode` SOAP-Header hinzugefügt, der die Fehlerbearbeitung in Flex ermöglicht. Verwenden Sie für Flex `<faultHttpStatusCode>200</faultHttpStatusCode>`. Der Standardstatuscode für Fehlerantworten ist `500 (Internal Server Error)`.

Es wurden Vorgänge zum Wiederherstellen von Assets aus dem Papierkorb und leere Assets aus dem Papierkorb hinzugefügt.

Implementierung von CRUD-Operationen.

Ein aktiviertes Flag zum `ImageMap` Typ und `saveImageMap` Vorgang wurde hinzugefügt.

Unterstützung für Aufträge zur Optimierung der verbleibenden Dateien hinzugefügt.

Es wurde `setAssetsPublishState` für Massenaktualisierungen des Veröffentlichungsstatus hinzugefügt.

Added `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Veralteter `saveMetadataField` Betrieb zu Gunsten neuer `createMetadataField` und `updateMetadataField` Operationen.

Der Vorgang zum Löschen von `deleteAssetsParam` Stapeln wurde implementiert.

Implementierter `moveAssetsParam` Stapelverschiebungsvorgang.

Implementierter `deleteMetadataField` Vorgang.

Implementierte `get/setImageRenderingPublishSettings`Vorgänge `get/set/create/updateVignettePublishFormat` .

Implemented `getAssetCounts`.

Unterstützung für `setImageSetMembers` die Einbeziehung von `RenderSet` Mitgliedern in `ImageSet` Assets hinzugefügt.

Vorgang `replaceImage` hinzugefügt.

Vorgang `copyImage` hinzugefügt.

Vorgang `setUrlModifier` und `urlModifier/urlPostApplyModifier` Felder für `LayerViewInfo`, `TemplateInfo`und `WatermarkInfo`.

Vorgang `createDerivedAsset` hinzugefügt. Derzeit `ownerHandle` muss der Typ auf ein Bild-Asset verweisen, und der Typ kann `AdjustedView` oder `LayerView`.

Vorgang `createTemplate` hinzugefügt. Derzeit kann dies aufgerufen werden, um Vorlagen- oder Wasserzeichenelemente zu erstellen.

IPS-Firma-Einstellungen, `CompanySettings`die auf die Web-Services-API portiert wurden.

Filtermarkierung `excludeByproducts` zum `searchAssets` Vorgang hinzugefügt. Wenn Sie dieses Flag auf &quot;true&quot;setzen, werden `PSDlayer` Bilder und gerippte PDF-Bilder ausgeführt.

Vorgang `getGenerationInfo` hinzugefügt.

Der `SystemMessage` Eigenschaftsname des `getProperty` Vorgangs wurde hinzugefügt.

Es wurden einige Zeichenfolgenkonstanten des Elementtyps entsprechend den entsprechenden Feldern für Asset-Informationen geändert.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Das Ergebnisformat von Stapelvorgängen wurde geändert, um den Erfolg, Warnungen und Fehler zusammenzufassen.

Implementierter `batchSetAssetMetadata` Batch-Metadatenvorgang.

Implementierte Unterstützung für App-spezifische Daten.

Die Unterstützung für boolesche Flags für Upload-Aufträge `createTemplate`, `extendLayers`und `extractText` für Upload-Aufträge wurde implementiert, um die Verarbeitung von Fotoshop zu steuern (ähnlich wie bei Änderungen beim Hochladen von Dateien).

Implementierte `setImageMaps` und `setZoomTargets` Vorgänge.

Implementierte `ViewerPreset` Vorgänge Die erkannten Typen sind:

* `VideoPlayer` (Video veröffentlicht diese Viewer nur.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Viewer-Skins unterstützen zwei Parameter: `skinFg` und `skinBg`. Backend-Code führt die gesamte erforderliche Verarbeitung aus, um die Abwärtskompatibilität zu gewährleisten.

Implementierter `getAssociatedAssets` Vorgang.

Der `ReprocessAssets` Auftragstyp wurde hinzugefügt, um die erneute Verarbeitung bereits hochgeladener Masterdateien zu ermöglichen, einschließlich der Wiedergabe von PDFs und der Neuoptimierung von Bildern.

Der `PropertySetType` Feldtyp wurde in `propertyType`. Dies wirkt sich auf den `createPropertySetType` Parameter und die `getPropertySetType/getPropertySetTypes` Antwort aus.

Der `batchSetImageFields` Vorgang wurde implementiert, um das Festlegen von Bildbenutzerdaten und anderen bearbeitbaren Bildfeldern zu unterstützen.

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

Implementierter `getActivePublishContexts` Vorgang. Dieser Vorgang gibt ein Array von Veröffentlichungskontextnamen mit aktiven Veröffentlichungsservern für die angegebene Firma zurück. Die Namen der aktuellen Veröffentlichungskontexte lauten:

* `ImageServing`
* `ImageRendering`
* `Video`

Implementierter `getSearchStrings` Vorgang. Gibt ein Array von Suchzeichenfolgen für das angegebene Asset zurück.

Es wurden Gebietsschema-Parameter für Aufträge und ein Mechanismus zum Festlegen des Gebietsschemas für API-Vorgänge hinzugefügt. Die Zeichenfolge im Gebietsschema sollte wie `<language_code>[-<country_code>]`. Der Sprachencode ist ein aus zwei Buchstaben bestehender Code in Kleinbuchstaben gemäß ISO-639, und der optionale Ländercode ist ein aus zwei Buchstaben bestehender Code gemäß ISO-3166.

Der `authHeader` SOAP-Kopfzeile wurde ein optionaler Parameter für Gebietsschema hinzugefügt, um das Gebietsschema für API-Vorgänge festzulegen. Ist dieser Parameter nicht vorhanden, wird der HTTP-Header verwendet `Accept-Language` . Wenn dieser Header ebenfalls nicht vorhanden ist, wird das Standardgebietsschema für den IPS-Server verwendet.

Unterstützung von get/set für stark typisierte Metadatenfelder hinzugefügt.

Implementierung der SOAP- und HTTP-Header-Unterstützung für gzip-Antwortsteuerung.

Flag `gzipResponse` hinzugefügt zu `authHeader`. Ist sie nicht vorhanden, prüft die API auch den HTTP- `Accept-Encoding` Header.

Unterstützung für searchAssets für stark typisierte Metadatenfeldbedingungen hinzugefügt.

* Bei allen Feldtypen kann der Wert mit einem Zeichenfolgenvergleichsoperator ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`) übergeben werden.
* Bei booleschen Feldern `boolVal` kann mit der `Equals` Spitze übergeben werden.
* Bei Int-Feldern `longVal` kann ein numerischer Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder `minLong/maxLong` ein numerischer Bereichsvorgang ( `Between, NotBetween`) übergeben werden.
* Bei Gleitkommafeldern `doubleVal` können Sie mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) weitergeleitet werden oder `minDouble/maxDouble` mit einem numerischen Bereichsvorgang ( `Between, NotBetween`) weitergeleitet werden.
* Bei Datumsfeldern können Sie `dateVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) übergeben oder minDate/maxDate mit einem numerischen Bereichsvorgängen ( `Between, NotBetween`) übergeben.

Beschreibung, `jobSubType`und `originalJobName` Felder zum `JobLog` Typ hinzugefügt.

* `originalJobName` ist der Auftragsname, der an `submitJob` (ohne eindeutige Suffixe oder Folgenauftragsnamen) übermittelt wird.
* `jobSubType` wird derzeit nur von `ImageServingPublishJob` Aufträgen verwendet (bei denen es sich um einen von `full`, `increment, fullwithsearch,` oder `fulloverride`) handelt.
* `description` ist derzeit eine leere Zeichenfolge für alle Auftragstypen, enthält jedoch letztendlich Informationen zum Zusammenfassungsauftrag, wie den Upload-Pfad.

Darüber hinaus sind die folgenden Felder nicht sowohl in `getJobLogs` als auch in `getJobLogDetails`enthalten. In früheren Versionen waren sie nur mit verfügbar `getJobLogDetails`.

* `endDate` (wenn der Auftrag abgeschlossen wurde).
* `fileDuplicateCount` (zuvor war es immer `0` mit `getJobLogs`)
* `fileUpdateCount` (zuvor war immer `0` mit `getJobLogs` und in `fileSuccessCount`enthalten; Es wird nun in separate Felder aufgeteilt).

AssetHandle-Feld zum `JobLogDetail` Typ hinzugefügt.

Optionaler Beschreibungsparameter wurde hinzugefügt `submitJob`. Dies wird für den Abruf in `getScheduledJobs`, `getActiveJobs`und `getJobLogs`weitergeleitet.

Das SKU-Systemfeld wurde überholt. Das Feld wird ignoriert, wenn es als `SystemFieldCondition` an übergeben wird `searchAssets`.

Filter `excludeAssetTypeArray` hinzugefügt zu `searchAssets`.

Der `MaskInfo` Typ wurde hinzugefügt `Asset`.

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
   <td colname="col1"> <p> <span class="codeph"> WordDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft Word-Dokument für Dateien, die mit .doc enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft Excel-Dokument für Dateien, die mit .xls enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft PowerPoint-Dokument für Dateien, die mit .ppt enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>RTF-Datei für Dateien, die mit .rtf hochgeladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

Es wurden zusätzliche Optionen hinzugefügt, um die Verarbeitung von PostScript-, Illustrator- und PDF-Dateien unabhängig voneinander zu steuern `UploadDirectoryJob` und `UploadUrlsJob` zu steuern. Alle bestehenden Aufträge werden die erforderlichen Parameter für jede der drei Verarbeitungsleitungen bereitstellen, damit sie genau wie heute funktionieren. Der ursprüngliche `PostScriptOptions` Block wird verwendet, um die Verarbeitung für Illustrator- und EPS/PS-Dateien festzulegen. Optional können spezifische Dateioptionenblöcke zur Angabe der Verarbeitung bereitgestellt werden. Die Liste der Änderungen umfasst:

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> PostScriptOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> verarbeiten </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Keine </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rastern </span>(Standard) </p> </li> 
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
   <td colname="col1" morerows="3"> <p> <span class="codeph"> IllustratorOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> verarbeiten </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Keine </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rastern </span> (Standard) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Verwalten Sie das Asset nur und erstellen Sie keine Ableitungen beim Hochladen. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Rendern Sie die Datei in einem Bild mit der vorgeschriebenen Auflösung und dem vorgeschriebenen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Auflösung wird gerastert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Farbraum </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Farbraum der Zielgruppe zum Rendern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Dies wirkt sich beim Rastern der Datei in ein Bild aus. Erstellt einen transparenten Hintergrund, wenn die Originaldatei auf diese Weise zum Erstellen von Überlagerungslogos definiert ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> verarbeiten </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Keine </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rastern </span> (Standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Verwalten Sie das Asset nur und erstellen Sie keine Ableitungen beim Hochladen. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Rendern Sie die Datei in einem Bild mit der vorgeschriebenen Auflösung und dem vorgeschriebenen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Auflösung wird gerastert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Farbraum </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Farbraum der Zielgruppe zum Rendern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesch&gt; </span> </p> </td> 
   <td colname="col4"> <p>Legt fest, ob nach dem Rendern eine mehrseitige PDF-Datei in einen E-Katalog kombiniert werden soll (Standard ist true). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesch&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definiert, ob Wörter aus der PDF-Datei zur späteren Bereitstellung an einen Suchserver in die DB extrahiert werden (Standard ist false). </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können auch von `getScheduledJobs`hier aus Abfragen ausführen.

Die `webservice.gzip.response` Konfigurationseigenschaft wurde geändert, um einen der folgenden Werte zu übernehmen:

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

