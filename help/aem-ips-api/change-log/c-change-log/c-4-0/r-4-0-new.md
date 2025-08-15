---
title: Neue Ergänzungen und Änderungen
description: Beschreibt neue und implementierte Änderungen für die IPS API v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# Neue Ergänzungen und Änderungen{#new-additions-and-changes}

Beschreibt neue und implementierte Änderungen für die IPS API v4.0.

Side-by-Side-API-Versionen mit separaten WSDLs und Schema-Namespaces implementiert.

* Frühere API-Versionen: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0 Version: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

`PostScriptOptions/alpha` Feld hinzugefügt.

`VideoRootUrl`- und `SwfRootUrl` für `getProperty` Vorgang hinzugefügt.

Es wurden optionale `appName`- und `appVersion` hinzugefügt, um aufrufende Anwendungen zu `authHeader`. Protokollierung hinzugefügt zu `ipsApiService.log`.

Dem WSDL-Generierungs-Servlet wurde ein optionaler `serviceUrl` hinzugefügt. Dieser Parameter ist für Debugging-Proxys nützlich. Beispiel: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

`getZipEntries` Vorgang implementiert.

Es wurden Suchbereiche implementiert und Vergleichswerte für Systemfeldbedingungen eingegeben.

Es wurde `'Asset'` Konstante vom Typ Asset-Zeichenfolge hinzugefügt, um Asset-übergreifende Metadatenfelder zu ermöglichen.

`trashState` Parameter für `searchAssets` implementiert.

`getAssetPublishHistory` Vorgang implementiert.

Es wurde eine optionale Kopfzeile `faultHttpStatusCode` SOAP hinzugefügt, um die Fehlerbehandlung in Flex zu aktivieren. Verwenden Sie für Flex `<faultHttpStatusCode>200</faultHttpStatusCode>`. Der Standardstatus-Code für Fehlerantworten lautet `500 (Internal Server Error)`.

Es wurden Vorgänge zum Wiederherstellen von Assets aus dem Papierkorb und zum Leeren von Assets aus dem Papierkorb hinzugefügt.

CRUD-Vorgänge implementiert.

Aktivierte Markierung zu `ImageMap` und `saveImageMap` hinzugefügt.

Unterstützung für verbleibende Dateiaufträge optimieren wurde hinzugefügt.

Es wurden `setAssetsPublishState` für Statusaktualisierungen für die Massenveröffentlichung hinzugefügt.

`ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings` hinzugefügt.

Veralteter `saveMetadataField`-Vorgang zugunsten neuer `createMetadataField`- und `updateMetadataField`.

`deleteAssetsParam` Batch-Löschvorgang implementiert.

`moveAssetsParam` Stapelverschiebungsvorgang implementiert.

`deleteMetadataField` Vorgang implementiert.

Implementierte `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` Vorgänge.

`getAssetCounts` implementiert.

`setImageSetMembers` für das Einschließen von `RenderSet`-Mitgliedern in `ImageSet` Assets wird nun unterstützt.

`replaceImage` Vorgang hinzugefügt.

`copyImage` Vorgang hinzugefügt.

Es wurden `setUrlModifier` Vorgangs- und `urlModifier/urlPostApplyModifier` für `LayerViewInfo`, `TemplateInfo` und `WatermarkInfo` hinzugefügt.

`createDerivedAsset` Vorgang hinzugefügt. Derzeit muss die `ownerHandle` auf ein Bild-Asset verweisen, und der Typ kann `AdjustedView` oder `LayerView` sein.

`createTemplate` Vorgang hinzugefügt. Aufruf zum Erstellen von Vorlagen- oder Wasserzeichen-Assets

IPS-Unternehmenseinstellungen, `CompanySettings`, portiert in die Web-Services-API.

Filterflag `excludeByproducts` `searchAssets` Vorgang hinzugefügt. Wenn Sie dieses Flag auf „true“ setzen, werden `PSDlayer` Bilder und in PDF ausgeschnittene Bilder ausgeführt.

`getGenerationInfo` Vorgang hinzugefügt.

`SystemMessage` Eigenschaftsname wurde `getProperty` Vorgang hinzugefügt.

Einige Konstanten vom Typ Asset-Zeichenfolge wurden geändert, damit sie mit den entsprechenden Feldern von Asset-Informationen übereinstimmen.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: rtf

Das Ergebnisformat der Batch-Vorgänge wurde geändert, um Erfolg, Warnungen und Fehler zusammenzufassen.

Batch`batchSetAssetMetadata`Metadatenvorgang implementiert.

Unterstützung für App-spezifische Daten implementiert.

Es wurde Unterstützung für boolesche Flags für `createTemplate`, `extendLayers` und `extractText` für Upload-Aufträge implementiert, um den Prozess der Photoshop-Verarbeitung zu steuern (ähnlich wie bei Änderungen für das Hochladen von Dateien hinzufügen).

Implementierte `setImageMaps`- und `setZoomTargets`.

`ViewerPreset` Vorgänge implementiert. Folgende Typen werden erkannt:

* `VideoPlayer` (Im Video werden nur diese Viewer veröffentlicht.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Viewer-Designs unterstützen zwei Parameter: `skinFg` und `skinBg`. Der Backend-Code übernimmt alle erforderlichen Verarbeitungsschritte, um die Abwärtskompatibilität aufrechtzuerhalten.

`getAssociatedAssets` Vorgang implementiert.

Es wurde `ReprocessAssets` Auftragstyp hinzugefügt, um die Neuverarbeitung zuvor hochgeladener Primärquelldateien zu ermöglichen, einschließlich des Neukomprimierens von PDFs und der Neuoptimierung von Bildern.

`PropertySetType` Feldtyp wurde in `propertyType` umbenannt. Diese Umbenennung wirkt sich auf den `createPropertySetType` und `getPropertySetType/getPropertySetTypes` Antwort aus.

Es wurde `batchSetImageFields` Vorgang implementiert, um das Festlegen von Bildbenutzerdaten und anderen bearbeitbaren Bildfeldern zu unterstützen.

47 Das Feld fileSize wurde zu verschiedenen Asset-Informationstypen hinzugefügt:

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

`getActivePublishContexts` Vorgang implementiert. Dieser Vorgang gibt ein Array von Veröffentlichungskontextnamen mit aktiven Veröffentlichungsservern für das angegebene Unternehmen zurück. Die Namen des aktuellen Veröffentlichungskontexts sind:

* `ImageServing`
* `ImageRendering`
* `Video`

`getSearchStrings` Vorgang implementiert. Gibt ein Array von Suchzeichenfolgen für das angegebene Asset zurück.

Es wurden Gebietsschema-Parameter für Aufträge und ein Mechanismus zum Festlegen des Gebietsschemas für API-Vorgänge hinzugefügt. Die Zeichenfolge des Gebietsschemas sollte als `<language_code>[-<country_code>]` formatiert sein. Der Sprach-Code ist ein Code mit zwei Kleinbuchstaben gemäß ISO-639, und der optionale Ländercode ist ein Code mit zwei Großbuchstaben gemäß ISO-3166.

Es wurde ein optionaler Gebietsschema-Parameter zum `authHeader` SOAP-Header hinzugefügt, um das Gebietsschema für API-Vorgänge festzulegen. Wenn dieser Parameter nicht vorhanden ist, wird der HTTP-Header `Accept-Language` verwendet. Wenn auch dieser Header nicht vorhanden ist, wird das Standardgebietsschema für den IPS-Server verwendet.

Es wurde Unterstützung für GET/SET für stark typisierte Metadatenfelder hinzugefügt.

SOAP- und HTTP-Header-Unterstützung für die gzip-Antwortsteuerung implementiert.

`gzipResponse`-Markierung wurde `authHeader` hinzugefügt. Wenn sie nicht vorhanden ist, prüft die API die HTTP-`Accept-Encoding`-Kopfzeile.

SearchAssets für stark typisierte Metadatenfeld-Bedingungen wird nun unterstützt.

* Bei allen Feldtypen kann der Wert mit einem Zeichenfolgenvergleichsoperator ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`) übergeben werden
* Bei booleschen Feldern kann `boolVal` mit dem `Equals` op. übergeben werden.
* Bei Int-Feldern können `longVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder `minLong/maxLong` mit numerischen Bereichsvorgängen ( `Between, NotBetween`) übergeben werden.
* Bei Float-Feldern können `doubleVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder `minDouble/maxDouble` mit numerischen Bereichsvorgängen ( `Between, NotBetween`) übergeben werden.
* Bei Datumsfeldern können Sie `dateVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) übergeben oder minDate/maxDate mit numerischen Bereichsvorgängen ( `Between, NotBetween`).

Es wurden die Felder Beschreibung, `jobSubType` und `originalJobName` zum `JobLog` hinzugefügt.

* `originalJobName` ist der Auftragsname, der an `submitJob` gesendet wird (ohne Eindeutigkeitssuffixe oder Nachfolgeauftragsnamen).
* `jobSubType` wird nur von `ImageServingPublishJob`-Aufträgen verwendet (wobei es sich um einen der folgenden Aufträge handelt: `full`, `increment, fullwithsearch,` oder `fulloverride`).
* `description` ist eine leere Zeichenfolge für alle Vorgangstypen, enthält aber letztendlich zusammenfassende Vorgangsinformationen, wie z. B. den Upload-Pfad.

Darüber hinaus sind die folgenden Felder nicht in `getJobLogs` und `getJobLogDetails` enthalten. In früheren Versionen waren sie nur mit `getJobLogDetails` verfügbar.

* `endDate` (wenn der Vorgang abgeschlossen ist).
* `fileDuplicateCount` (zuvor war es immer mit `0` `getJobLogs`)
* `fileUpdateCount` (wurde zuvor immer mit `0` `getJobLogs` und in `fileSuccessCount` eingeschlossen; jetzt ist er in separate Felder unterteilt).

Das Feld assetHandle wurde zum `JobLogDetail` hinzugefügt.

Optionaler Beschreibungsparameter zu `submitJob` hinzugefügt. Dieser Parameter wird zum Abrufen in `getScheduledJobs`, `getActiveJobs` und `getJobLogs` übergeben.

Das Feld SKU-System ist veraltet. Das Feld wird ignoriert, wenn es als `SystemFieldCondition` an `searchAssets` übergeben wird.

`excludeAssetTypeArray` Filter zu `searchAssets` hinzugefügt.

`MaskInfo` zum `Asset` hinzugefügt.

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
   <td colname="col1"> <p> <span class="codeph"> WordDoc-</span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Word-Dokument für Dateien, die auf .doc enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc-</span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Excel-Dokument für Dateien, die auf .xls enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc-</span> </p> </td> 
   <td colname="col2"> <p>Microsoft® PowerPoint-Dokument für Dateien, die auf .ppt enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc-</span> </p> </td> 
   <td colname="col2"> <p>RTF-Datei für hochgeladene Dateien mit der Endung .rtf. </p> </td> 
  </tr> 
 </tbody> 
</table>

Es wurden zusätzliche Optionen zum `UploadDirectoryJob` und `UploadUrlsJob` hinzugefügt, um die Verarbeitung von PostScript-, Illustrator- und PDF-Dateien unabhängig zu steuern. Alle vorhandenen Aufträge liefern die erforderlichen Parameter für jede der drei Verarbeitungs-Pipelines, damit sie genau wie heute funktionieren. Der ursprüngliche `PostScriptOptions` wird verwendet, um die Verarbeitung für Illustrator- und EPS/PS-Dateien festzulegen. Optional können bestimmte Dateioptionenblöcke bereitgestellt werden, um die Verarbeitung anzugeben. Die Liste der Änderungen umfasst:

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
   <td colname="col1" morerows="1"> <p> <span class="codeph"> [!DNL PostScriptOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL process] </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_6BBFF026010F4913BD632B3312E17C4B"> 
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> keine </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rastern </span>Standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Verwalten Sie nur das Asset und erstellen Sie keine Ableitungen beim Hochladen. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Rendern Sie die EPS- und PostScript-Datei in einem Bild mit der vorgeschriebenen Auflösung und dem vorgeschriebenen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Alpha-</span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Wird beim Rastern der Datei in einem Bild wirksam. Es wird ein transparenter Hintergrund erstellt, wenn die Originaldatei auf diese Weise für das Überlagern von Logos definiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> keine </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> </span> (Standard) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Verwalten Sie nur das Asset und erstellen Sie keine Ableitungen beim Hochladen. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Rendern Sie die Datei in einem Bild mit der vorgeschriebenen Auflösung und dem vorgeschriebenen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Auflösung wird gerastert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Zielfarbraum für die Wiedergabe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Alpha-</span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Wird beim Rastern der Datei in einem Bild wirksam. Erstellt einen transparenten Hintergrund, wenn die Originaldatei auf diese Weise zum Erstellen von Überlagerungen von Logos definiert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions-</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> keine </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> </span> (Standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Verwalten Sie nur das Asset und erstellen Sie keine Ableitungen beim Hochladen. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Rendern Sie die Datei in einem Bild mit der vorgeschriebenen Auflösung und dem vorgeschriebenen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Auflösung wird gerastert </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Zielfarbraum für die Wiedergabe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog-</span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definiert, ob eine mehrseitige PDF nach dem Rendering in einem E-Katalog kombiniert werden soll (der Standardwert ist „true„). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords-</span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definiert, ob Wörter aus der PDF in die Datenbank extrahiert werden, damit sie später an einen Suchserver übergeben werden (der Standardwert lautet „false„). </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können auch Abfragen über `getScheduledJobs` durchführen.

Die Konfigurationseigenschaft `webservice.gzip.response` wurde geändert, sodass sie einen der folgenden Werte annimmt:

<table id="table_FCBBF1643DC84F5CBF81DCA6B552E0C4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Wert </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL never] </span> </p> </td> 
   <td colname="col2"> <p>Keine Gzip-Antwort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>Gzip-Antwort nur, wenn authHeader/gzipResponse wahr ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip , wenn authHeader/gzipResponse wahr ist oder keine gzipResponse-Kopfzeile vorhanden ist und die HTTP Accept-Encoding-Kopfzeile gzip enthält. (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>Immer gzip -Antwort, unabhängig von Kopfzeilenwerten. Verwenden Sie diesen Wert nur zu Debugging-Zwecken. </p> </td> 
  </tr> 
 </tbody> 
</table>
