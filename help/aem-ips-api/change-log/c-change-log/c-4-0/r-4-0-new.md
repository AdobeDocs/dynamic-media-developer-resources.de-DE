---
title: Neue Ergänzungen und Änderungen
description: Beschreibt neue und implementierte Änderungen für die IPS-API v4.0.
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

Beschreibt neue und implementierte Änderungen für die IPS-API v4.0.

Implementierung von nebeneinander liegenden API-Versionen mit separaten WSDLs und Schema-Namespaces.

* Frühere API-Versionen: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0-Version: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Das Feld `PostScriptOptions/alpha` wurde hinzugefügt.

Die Eigenschaften `VideoRootUrl` und `SwfRootUrl` für den Vorgang `getProperty` wurden hinzugefügt.

Die optionalen Parameter `appName` und `appVersion` wurden zu `authHeader` hinzugefügt, um aufrufende Anwendungen zu verfolgen. Protokollierung zu `ipsApiService.log` hinzugefügt.

Dem WSDL-Generierungsservlet wurde ein optionaler Parameter `serviceUrl` hinzugefügt. Dieser Parameter ist für das Debugging von Proxys nützlich. Beispiel: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

Der `getZipEntries`-Vorgang wurde implementiert.

Es wurden Suchbereiche implementiert und Vergleichswerte für Systemfeldbedingungen eingegeben.

String-Konstante vom Typ `'Asset'` Asset-Typ wurde hinzugefügt, um in erster Linie Asset-übergreifende Metadatenfelder zu ermöglichen.

Implementierung des `trashState` -Parameters für `searchAssets`.

Der `getAssetPublishHistory`-Vorgang wurde implementiert.

Der optionale Header `faultHttpStatusCode` SOAP wurde hinzugefügt, um die Fehlerbehebung in Flex zu ermöglichen. Verwenden Sie für Flex `<faultHttpStatusCode>200</faultHttpStatusCode>`. Der Standardstatuscode für Fehlerantworten ist `500 (Internal Server Error)`.

Es wurden Vorgänge zum Wiederherstellen von Assets aus dem Papierkorb und leere Assets aus dem Papierkorb hinzugefügt.

Implementierung von CRUD-Vorgängen.

Dem Vorgang `ImageMap` und `saveImageMap` wurde eine aktivierte Markierung hinzugefügt.

Unterstützung für Optimieren von Aufträgen für verbleibende Dateien hinzugefügt.

Für Massenaktualisierungen zum Veröffentlichungsstatus wurde `setAssetsPublishState` hinzugefügt.

`ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings` hinzugefügt.

Veraltete `saveMetadataField`-Operation zugunsten neuer `createMetadataField`- und `updateMetadataField`-Vorgänge.

Der Batch-Löschvorgang wurde implementiert. `deleteAssetsParam`

Implementierung des Batch-Verschiebungsvorgangs `moveAssetsParam` .

Der `deleteMetadataField`-Vorgang wurde implementiert.

Implementierte Vorgänge `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` .

`getAssetCounts` wurde implementiert.

Unterstützung für `setImageSetMembers` hinzugefügt, um `RenderSet` Mitglieder in `ImageSet` -Assets aufzunehmen.

Vorgang `replaceImage` wurde hinzugefügt.

Vorgang `copyImage` wurde hinzugefügt.

Die Felder `setUrlModifier` und `urlModifier/urlPostApplyModifier` wurden für `LayerViewInfo`, `TemplateInfo` und `WatermarkInfo` hinzugefügt.

Vorgang `createDerivedAsset` wurde hinzugefügt. Derzeit muss der `ownerHandle` auf ein Bild-Asset verweisen und der Typ kann `AdjustedView` oder `LayerView` sein.

Vorgang `createTemplate` wurde hinzugefügt. Aufrufen, um Vorlagen- oder Wasserzeichen-Assets zu erstellen.

IPS-Unternehmenseinstellungen, `CompanySettings`, portiert auf die Web-Services-API.

`excludeByproducts` Filterkennzeichnung zum `searchAssets` -Vorgang hinzugefügt. Wenn dieses Flag auf &quot;true&quot;gesetzt wird, werden `PSDlayer` Bilder und PDF gerippte Bilder ausgeführt.

Vorgang `getGenerationInfo` wurde hinzugefügt.

Der Eigenschaftsname `SystemMessage` wurde zum Vorgang `getProperty` hinzugefügt.

Es wurden einige String-Konstanten vom Typ Asset geändert, die mit den entsprechenden Asset Info -Feldern übereinstimmen.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Das Ergebnisformat von Batch-Vorgängen wurde geändert, um Erfolg, Warnungen und Fehler zusammenzufassen.

Implementierte Batch-Metadatenoperation `batchSetAssetMetadata` .

Die Unterstützung für App-spezifische Daten wurde implementiert.

Die Unterstützung für boolesche Flags für Upload-Aufträge mit `createTemplate`, `extendLayers` und `extractText` wurde implementiert, um die Verarbeitung von Photoshop-Aufträgen zu steuern (ähnlich wie bei Änderungen beim Hochladen von Dateien).

Implementierung der Vorgänge `setImageMaps` und `setZoomTargets`.

Implementierung von `ViewerPreset` -Vorgängen. Die erkannten Typen sind:

* `VideoPlayer` (Video veröffentlicht diese Viewer nur.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Viewer-Skins unterstützen zwei Parameter: `skinFg` und `skinBg`. Der Backend-Code führt die gesamte erforderliche Verarbeitung aus, um die Abwärtskompatibilität zu gewährleisten.

Der `getAssociatedAssets`-Vorgang wurde implementiert.

Der Auftragstyp `ReprocessAssets` wurde hinzugefügt, um die erneute Verarbeitung zuvor hochgeladener Primärquelldateien zu ermöglichen, einschließlich des erneuten Abschneidens von PDF und der Neuoptimierung von Bildern.

Der Feldtyp `PropertySetType` wurde in `propertyType` umbenannt. Diese Umbenennung wirkt sich auf die Antwort `createPropertySetType` und `getPropertySetType/getPropertySetTypes` aus.

Der Vorgang `batchSetImageFields` wurde implementiert, um das Festlegen von Bildbenutzerdaten und anderen bearbeitbaren Bildfeldern zu unterstützen.

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

Der `getActivePublishContexts`-Vorgang wurde implementiert. Dieser Vorgang gibt ein Array von Veröffentlichungskontextnamen mit aktiven Veröffentlichungsservern für das angegebene Unternehmen zurück. Aktuelle Veröffentlichungskontextnamen sind:

* `ImageServing`
* `ImageRendering`
* `Video`

Der `getSearchStrings`-Vorgang wurde implementiert. Es wird ein Array von Suchzeichenfolgen für das angegebene Asset zurückgegeben.

Es wurden Gebietsschema-Parameter für Aufträge und ein Mechanismus zum Festlegen des Gebietsschemas für API-Vorgänge hinzugefügt. Die Gebietsschema-Zeichenfolge sollte als `<language_code>[-<country_code>]` formatiert sein. Der Sprachcode ist ein aus zwei Buchstaben bestehender Code in Kleinbuchstaben gemäß ISO-639 und der optionale Ländercode ist ein aus zwei Buchstaben bestehender Code in Großbuchstaben gemäß ISO-3166.

Der Kopfzeile `authHeader` SOAP optionaler Parameter für das Gebietsschema wurde hinzugefügt, um das Gebietsschema für API-Vorgänge festzulegen. Wenn dieser Parameter nicht vorhanden ist, wird der HTTP-Header `Accept-Language` verwendet. Wenn diese Kopfzeile ebenfalls nicht vorhanden ist, wird das standardmäßige Gebietsschema für den IPS-Server verwendet.

Unterstützung für stark typisierte Metadatenfelder hinzugefügt.

Die SOAP- und HTTP-Header-Unterstützung für die gzip-Antwortsteuerung wurde implementiert.

Markierung `gzipResponse` wurde zu `authHeader` hinzugefügt. Ist er nicht vorhanden, prüft die API den HTTP-Header `Accept-Encoding`.

Unterstützung für searchAssets für stark typisierte Metadatenfeldbedingungen hinzugefügt.

* Für alle Feldtypen kann der Wert mit einem Zeichenfolgenvergleichsoperator ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`) übergeben werden.
* Bei booleschen Feldern kann `boolVal` mit der `Equals` op übergeben werden.
* Bei Int-Feldern kann `longVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder `minLong/maxLong` mit einem numerischen Bereichsvorgang ( `Between, NotBetween`) übergeben werden.
* Bei Gleitkommafeldern kann `doubleVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder `minDouble/maxDouble` mit einem numerischen Bereichsvorgang ( `Between, NotBetween`) übergeben werden.
* Für Datumsfelder können Sie `dateVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) übergeben oder minDate/maxDate mit einem numerischen Bereichsvorgang ( `Between, NotBetween`) übergeben.

Die Felder `jobSubType` und `originalJobName` wurden zum Typ `JobLog` hinzugefügt.

* `originalJobName` ist der Auftragsname, der an `submitJob` gesendet wird (ohne Eindeutigkeitssuffixe oder Nachfolgenauftragsnamen).
* `jobSubType` wird nur von `ImageServingPublishJob` Aufträgen verwendet (wobei es einer von `full`, `increment, fullwithsearch,` oder `fulloverride` ist).
* `description` ist eine leere Zeichenfolge für alle Auftragstypen, enthält jedoch letztendlich Zusammenfassungsauftragsinformationen, z. B. den Upload-Pfad.

Darüber hinaus sind die folgenden Felder nicht sowohl in `getJobLogs` als auch in `getJobLogDetails` enthalten. In früheren Versionen waren sie nur mit `getJobLogDetails` verfügbar.

* `endDate` (wenn der Auftrag abgeschlossen wurde).
* `fileDuplicateCount` (zuvor war es immer `0` mit `getJobLogs`)
* `fileUpdateCount` (zuvor war es immer `0` mit `getJobLogs` und war in `fileSuccessCount` enthalten; jetzt wird es in separate Felder aufgeteilt).

Das Feld assetHandle wurde dem Typ `JobLogDetail` hinzugefügt.

Optionaler Beschreibungsparameter zu `submitJob` hinzugefügt. Dieser Parameter wird zum Abrufen in `getScheduledJobs`, `getActiveJobs` und `getJobLogs` übergeben.

Das SKU-Systemfeld wurde veraltet. Das Feld wird ignoriert, wenn es als `SystemFieldCondition` an `searchAssets` übergeben wird.

`excludeAssetTypeArray` Filter zu `searchAssets` hinzugefügt.

`MaskInfo`-Typ zu `Asset` hinzugefügt.

Es wurden neue Asset-Typen für die Verwaltung durch IPS hinzugefügt:

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
   <td colname="col2"> <p>Microsoft® Word-Dokument für Dateien, die mit .doc enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ExcelDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® Excel-Dokument für Dateien, die mit .xls enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PowerPointDoc </span> </p> </td> 
   <td colname="col2"> <p>Microsoft® PowerPoint-Dokument für Dateien, die mit .ppt enden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RTFDoc </span> </p> </td> 
   <td colname="col2"> <p>RTF-Datei für Dateien, die mit .rtf hochgeladen wurden. </p> </td> 
  </tr> 
 </tbody> 
</table>

Es wurden zusätzliche Optionen zu `UploadDirectoryJob` und `UploadUrlsJob` hinzugefügt, um die unabhängige Verarbeitung von Postscript-, Illustrator- und PDF-Dateien zu steuern. Alle vorhandenen Aufträge stellen die erforderlichen Parameter für jede der drei Verarbeitungs-Pipelines bereit, damit sie genau wie heute funktionieren. Der ursprüngliche Block `PostScriptOptions` wird verwendet, um die Verarbeitung für Illustrator- und EPS/PS-Dateien festzulegen. Optional können bestimmte Dateioptionen-Blöcke bereitgestellt werden, um die Verarbeitung anzugeben. Die Liste der Änderungen umfasst:

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
      <li id="li_AA1131A68FB242C9A1380DE6F8F318C7"> <p> <span class="codeph"> Keine </span> </p> </li> 
      <li id="li_141F4C3FC9D34C9AABECA91394A82969"> <p> <span class="codeph"> Rasterize </span>(Standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_14D0A696DF4E408DA50E102057EB7AC7"> 
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Verwalten Sie das Asset nur und erstellen Sie beim Hochladen keine Ableitungen. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Rendern Sie die EPS- und PostScript-Datei in einem Bild mit der vorgeschriebenen Auflösung und dem erforderlichen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Wird beim Rastern der Datei in ein Bild wirksam. Es erzeugt einen transparenten Hintergrund, wenn die ursprüngliche Datei so definiert ist, dass Logos überlagert werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="3"> <p> <span class="codeph"> [!DNL IllustratorOptions] </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_C2F1000A01DE41678A8E1DDE0C8A0E97"> 
      <li id="li_53749049B383441A81CB427A5B5F26A8"> <span class="codeph"> Keine </span> </li> 
      <li id="li_C5332FC35E5C4687B30D4C1081015BB0"> <span class="codeph"> Rasterize </span> (Standard) </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_41924574773542B7BFC4989667C14E97"> 
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Verwalten Sie das Asset nur und erstellen Sie beim Hochladen keine Ableitungen. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Rendern Sie die Datei in ein Bild mit der vorgeschriebenen Auflösung und dem erforderlichen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rastern der Auflösung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Zielfarbraum für die Wiedergabe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Wird beim Rastern der Datei in ein Bild wirksam. Erstellt einen transparenten Hintergrund, wenn die ursprüngliche Datei so definiert ist, um überlagerte Logos zu erstellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="4"> <p> <span class="codeph"> PDFOptions </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> process </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Keine </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rasterize </span> (Standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Verwalten Sie das Asset nur und erstellen Sie beim Hochladen keine Ableitungen. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Rendern Sie die Datei in ein Bild mit der vorgeschriebenen Auflösung und dem erforderlichen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL resolution] </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rastern der Auflösung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> [!DNL colorspace] </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Zielfarbraum für die Wiedergabe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definiert, ob nach dem Rendern eine mehrseitige PDF in einen eCatalog kombiniert werden soll (Standard ist "true"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolean&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definiert, ob Wörter aus der PDF zur späteren Bereitstellung an einen Suchserver in die DB extrahiert werden (der Standardwert ist "false"). </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können auch über &quot;`getScheduledJobs`&quot;abfragen.

Die Konfigurationseigenschaft `webservice.gzip.response` wurde geändert, um einen der folgenden Werte zu übernehmen:

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
   <td colname="col2"> <p>Keine gzip-Antwort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL soap] </span> </p> </td> 
   <td colname="col2"> <p>Gzip-Antwort nur dann, wenn authHeader/gzipResponse "true"ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL accept] </span> </p> </td> 
   <td colname="col2"> <p>Gzip , wenn authHeader/gzipResponse wahr ist oder kein gzipResponse-Header vorhanden ist und der HTTP Accept-Encoding-Header gzip enthält. (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [!DNL always] </span> </p> </td> 
   <td colname="col2"> <p>Immer gzip-Antwort, unabhängig von Header-Werten. Verwenden Sie diesen Wert nur zum Debugging. </p> </td> 
  </tr> 
 </tbody> 
</table>
