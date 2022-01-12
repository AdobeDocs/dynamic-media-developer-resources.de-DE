---
title: Neue Ergänzungen und Änderungen
description: Beschreibt neue und implementierte Änderungen für die IPS-API v4.0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f07562a8-71e9-4d98-9d0c-5bb32a7e0ef1
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 2%

---

# Neue Ergänzungen und Änderungen{#new-additions-and-changes}

Beschreibt neue und implementierte Änderungen für die IPS-API v4.0.

Implementierung von nebeneinander liegenden API-Versionen mit separaten WSDLs und Schema-Namespaces.

* Frühere API-Versionen: `IpsApi.wsdl, http://www.scene7.com/IpsApi/xsd`.
* SPS 4.0-Version: `IpsApi-2008-01-15.wsdl, http://www.scene7.com/IpsApi/xsd/2008-01-15`.

Hinzugefügt `PostScriptOptions/alpha` -Feld.

Hinzugefügt `VideoRootUrl` und `SwfRootUrl` Eigenschaften für `getProperty` Vorgang.

Optional hinzugefügt `appName` und `appVersion` params in `authHeader` , um die aufrufende Anwendung zu verfolgen. Protokollierung zu hinzugefügt `ipsApiService.log`.

Eine optionale `serviceUrl` param zum WSDL-Generierungsservlet. Dieser Parameter ist für das Debugging von Proxys nützlich. Beispiel: `http://<server>/scene7/webservice/IpsApi-2008-01-15.wsdl?serviceUrl=http://localhost:8081`

implementiert `getZipEntries` Vorgang.

Es wurden Suchbereiche implementiert und Vergleichswerte für Systemfeldbedingungen eingegeben.

Hinzugefügt `'Asset'` String-Konstante für den Asset-Typ, um in erster Linie Asset-übergreifende Metadatenfelder zuzulassen.

implementiert `trashState` param für `searchAssets`.

implementiert `getAssetPublishHistory` Vorgang.

Optional hinzugefügt `faultHttpStatusCode` SOAP-Header zur Aktivierung der Fehlerbehandlung in Flex. Verwenden Sie für Flex `<faultHttpStatusCode>200</faultHttpStatusCode>`. Der Standardstatuscode für Fehlerantworten lautet `500 (Internal Server Error)`.

Es wurden Vorgänge zum Wiederherstellen von Assets aus dem Papierkorb und leere Assets aus dem Papierkorb hinzugefügt.

Implementierung von CRUD-Vorgängen.

Das aktivierte Flag wurde hinzugefügt zu `ImageMap` Typ und `saveImageMap` Vorgang.

Unterstützung für Optimieren von Aufträgen für verbleibende Dateien hinzugefügt.

Hinzugefügt `setAssetsPublishState` für Massenaktualisierungen des Veröffentlichungsstatus.

Hinzugefügt `ImageServingPublishSettings`, `getImageServingPublishSettings`, `setImageServingPublishSettings`.

Veraltet `saveMetadataField` Vorhaben zugunsten neuer `createMetadataField` und `updateMetadataField` Vorgänge.

implementiert `deleteAssetsParam` Batch-Löschvorgang.

implementiert `moveAssetsParam` Vorgang &quot;Batch Move&quot;.

implementiert `deleteMetadataField` Vorgang.

implementiert `get/setImageRenderingPublishSettings`, `get/set/create/updateVignettePublishFormat` Vorgänge.

implementiert `getAssetCounts`.

Hinzugefügte Unterstützung für `setImageSetMembers` einschließlich `RenderSet` Mitglieder in `ImageSet` Assets.

Hinzugefügt `replaceImage` Vorgang.

Hinzugefügt `copyImage` Vorgang.

Hinzugefügt `setUrlModifier` Betrieb und `urlModifier/urlPostApplyModifier` Felder für `LayerViewInfo`, `TemplateInfo`und `WatermarkInfo`.

Hinzugefügt `createDerivedAsset` Vorgang. Derzeit ist das `ownerHandle` muss auf ein Bild-Asset verweisen und der Typ kann `AdjustedView` oder `LayerView`.

Hinzugefügt `createTemplate` Vorgang. Rufen Sie auf, um Vorlagen- oder Wasserzeichen-Assets zu erstellen.

Einstellungen des IPS-Unternehmens, `CompanySettings`, portiert auf die Web-Services-API.

Hinzugefügt `excludeByproducts` Filtermarkierung auf `searchAssets` Vorgang. Festlegen dieser Markierung auf &quot;true&quot;wird ausgeführt `PSDlayer` Bilder und PDF gerippte Bilder.

Hinzugefügt `getGenerationInfo` Vorgang.

Hinzugefügt `SystemMessage` Eigenschaftsname in `getProperty` Vorgang.

Es wurden einige String-Konstanten vom Typ Asset geändert, die mit den entsprechenden Asset Info -Feldern übereinstimmen.

* WordDoc: Word
* ExcelDoc: Excel
* PowerPointDoc: PowerPoint
* RTFDoc: Rtf

Das Ergebnisformat von Batch-Vorgängen wurde geändert, um Erfolg, Warnungen und Fehler zusammenzufassen.

implementiert `batchSetAssetMetadata` Vorgang für Batch-Metadaten.

Die Unterstützung für App-spezifische Daten wurde implementiert.

Implementierte Unterstützung für boolesche Flags für `createTemplate`, `extendLayers`und `extractText` für Upload-Aufträge zur Steuerung der Photoshop-Verarbeitung (ähnlich wie Änderungen beim Hinzufügen von Datei-Uploads).

implementiert `setImageMaps` und `setZoomTargets` Vorgänge.

implementiert `ViewerPreset` Vorgänge. Die erkannten Typen sind:

* `VideoPlayer` (Video veröffentlicht diese Viewer nur.)
* `Brochure`
* `BasicZoom`
* `AdvancedZoom`
* `Spin`
* `Custom types`

Viewer-Skins unterstützen zwei Parameter: `skinFg` und `skinBg`. Der Backend-Code führt die gesamte erforderliche Verarbeitung aus, um die Abwärtskompatibilität zu gewährleisten.

implementiert `getAssociatedAssets` Vorgang.

Hinzugefügt `ReprocessAssets` Auftragstyp, um die erneute Verarbeitung von zuvor hochgeladenen Primärquelldateien zu ermöglichen, einschließlich des erneuten Abrufs von PDF und der Neuoptimierung von Bildern.

Umbenannt `PropertySetType` Feldtyp zu `propertyType`. Diese Umbenennung wirkt sich auf die `createPropertySetType` Parameter und `getPropertySetType/getPropertySetTypes` Antwort.

implementiert `batchSetImageFields` -Operation, um das Festlegen von Bildbenutzerdaten und anderen bearbeitbaren Bildfeldern zu unterstützen.

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

implementiert `getActivePublishContexts` Vorgang. Dieser Vorgang gibt ein Array von Veröffentlichungskontextnamen mit aktiven Veröffentlichungsservern für das angegebene Unternehmen zurück. Aktuelle Veröffentlichungskontextnamen sind:

* `ImageServing`
* `ImageRendering`
* `Video`

implementiert `getSearchStrings` Vorgang. Es wird ein Array von Suchzeichenfolgen für das angegebene Asset zurückgegeben.

Es wurden Gebietsschema-Parameter für Aufträge und ein Mechanismus zum Festlegen des Gebietsschemas für API-Vorgänge hinzugefügt. Die Gebietsschema-Zeichenfolge sollte als `<language_code>[-<country_code>]`. Der Sprachcode ist ein aus zwei Buchstaben bestehender Code in Kleinbuchstaben gemäß ISO-639 und der optionale Ländercode ist ein aus zwei Buchstaben bestehender Code in Großbuchstaben gemäß ISO-3166.

Der optionale Parameter locale wurde zum `authHeader` SOAP-Kopfzeile zum Festlegen des Gebietsschemas für API-Vorgänge. Wenn dieser Parameter nicht vorhanden ist, wird der HTTP-Header `Accept-Language` verwendet. Wenn diese Kopfzeile ebenfalls nicht vorhanden ist, wird das standardmäßige Gebietsschema für den IPS-Server verwendet.

Unterstützung für stark typisierte Metadatenfelder hinzugefügt.

SOAP- und HTTP-Header-Unterstützung für die gzip-Antwortsteuerung implementiert.

Hinzugefügt `gzipResponse` Markierung auf `authHeader`. Ist dies nicht der Fall, prüft die API das HTTP `Accept-Encoding` -Kopfzeile.

Unterstützung für searchAssets für stark typisierte Metadatenfeldbedingungen hinzugefügt.

* Für alle Feldtypen kann der Wert mit einem Zeichenfolgenvergleichsoperator ( `Equals, NotEquals, Contains, NotContains, StartsWith, EndsWith`)
* Für boolesche Felder: `boolVal` kann mit der `Equals` op.
* Für Eingabefelder: `longVal` kann mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder `minLong/maxLong` kann mit numerischen Bereichsvorgängen ( `Between, NotBetween`).
* Für Gleitkommafelder: `doubleVal` kann mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder `minDouble/maxDouble` kann mit numerischen Bereichsvorgängen ( `Between, NotBetween`).
* Für Datumsfelder können Sie `dateVal` mit einem numerischen Vergleichsoperator ( `Equals, NotEquals, LessThan, LessThanEquals, GreaterThan, GreaterThanEquals`) oder Sie können minDate/maxDate mit numerischen Bereichsvorgängen ( `Between, NotBetween`).

Beschreibung hinzugefügt, `jobSubType`und `originalJobName` Felder zu `JobLog` Typ.

* `originalJobName` ist der Auftragsname, der an übermittelt wird. `submitJob` (ohne Eindeutigkeitssuffixe oder Nachfolgenauftragsnamen).
* `jobSubType` wird nur von `ImageServingPublishJob` Aufträge (wobei es sich um einen von `full`, `increment, fullwithsearch,` oder `fulloverride`).
* `description` ist eine leere Zeichenfolge für alle Auftragstypen, enthält jedoch letztendlich Zusammenfassungsauftragsinformationen wie den Upload-Pfad.

Darüber hinaus sind die folgenden Felder nicht in beiden `getJobLogs` und `getJobLogDetails`. In früheren Versionen waren sie nur mit `getJobLogDetails`.

* `endDate` (wenn der Auftrag abgeschlossen wurde).
* `fileDuplicateCount` (zuvor war es immer `0` mit `getJobLogs`)
* `fileUpdateCount` (zuvor war immer `0` mit `getJobLogs` und in `fileSuccessCount`; jetzt in separate Felder aufgeteilt).

Das Feld assetHandle wurde zu `JobLogDetail` Typ.

Optionaler Beschreibungsparameter zu `submitJob`. Dieser Parameter wird zum Abrufen in weitergeleitet. `getScheduledJobs`, `getActiveJobs`und `getJobLogs`.

Das SKU-Systemfeld wurde veraltet. Das Feld wird ignoriert, wenn es als `SystemFieldCondition` nach `searchAssets`.

Hinzugefügt `excludeAssetTypeArray` filtern `searchAssets`.

Hinzugefügt `MaskInfo` type to `Asset`.

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

Zusätzliche Optionen zu `UploadDirectoryJob` und `UploadUrlsJob` zur unabhängigen Steuerung der Verarbeitung von Postscript-, Illustrator- und PDF-Dateien. Alle vorhandenen Aufträge stellen die erforderlichen Parameter für jede der drei Verarbeitungs-Pipelines bereit, damit sie genau wie heute funktionieren. Das Original `PostScriptOptions` -Block wird verwendet, um die Verarbeitung für Illustrator- und EPS/PS-Dateien festzulegen. Optional können bestimmte Dateioptionen-Blöcke bereitgestellt werden, um die Verarbeitung anzugeben. Die Liste der Änderungen umfasst:

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
      <li id="li_D8AA718D9F504B91AB557216D2D7DBCC"> <p>Verwalten Sie das Asset nur und erstellen Sie beim Hochladen keine Ableitungen. </p> </li> 
      <li id="li_3F56CEABAB3E43EAB157C83583A2F58D"> <p>Rendern Sie die EPS- und PostScript-Datei in ein Bild mit der vorgeschriebenen Auflösung und dem erforderlichen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> alpha </span> </p> <p>Optional. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesch&gt; </span> </p> </td> 
   <td colname="col4"> <p>Wird beim Rastern der Datei in ein Bild wirksam. Es erzeugt einen transparenten Hintergrund, wenn die ursprüngliche Datei so definiert ist, dass Logos überlagert werden. </p> </td> 
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
      <li id="li_3886554059AB4F7383619A9CB7292E0E"> <p>Verwalten Sie das Asset nur und erstellen Sie beim Hochladen keine Ableitungen. </p> </li> 
      <li id="li_BF3F5E54484C46D8887CA48D8646648E"> <p>Rendern Sie die Datei in ein Bild mit der vorgeschriebenen Auflösung und dem erforderlichen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rastern der Auflösung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Farbraum </span> </p> </td> 
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
   <td colname="col2"> <p> <span class="codeph"> verarbeiten </span> </p> </td> 
   <td colname="col3"> <p> 
     <ul id="ul_EF9C27EE7A154DA890CB9E6BA174D767"> 
      <li id="li_0BB0FC1BA43043EEA1EA257E5D603978"> <p> <span class="codeph"> Keine </span> </p> </li> 
      <li id="li_E3FA07129C2646C7B98854C22CDAC1F0"> <p> <span class="codeph"> Rastern </span> (Standard) </p> </li> 
     </ul> </p> </td> 
   <td colname="col4"> <p> 
     <ul id="ul_84EE74454FF5434087A895F915E68103"> 
      <li id="li_4312A1CD5F4B44589678311A59536FA7"> <p>Verwalten Sie das Asset nur und erstellen Sie beim Hochladen keine Ableitungen. </p> </li> 
      <li id="li_06FBA83EA3F248E288F4790255802DE6"> <p>Rendern Sie die Datei in ein Bild mit der vorgeschriebenen Auflösung und dem erforderlichen Farbraum. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> resolution </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;integer&gt; </span> </p> </td> 
   <td colname="col4"> <p>Rastern der Auflösung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> Farbraum </span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>Zielfarbraum für die Wiedergabe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> pdfCatalog </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesch&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definiert, ob nach dem Rendern eine mehrseitige PDF in einen eCatalog kombiniert werden soll (Standard ist "true"). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> <span class="codeph"> extractSearchWords </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;boolesch&gt; </span> </p> </td> 
   <td colname="col4"> <p>Definiert, ob Wörter aus der PDF zur späteren Bereitstellung an einen Suchserver in die DB extrahiert werden (der Standardwert ist "false"). </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können auch eine Abfrage über `getScheduledJobs`.

Die `webservice.gzip.response` Konfigurationseigenschaft einen der folgenden Werte annehmen:

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
   <td colname="col2"> <p>Gzip-Antwort nur dann, wenn authHeader/gzipResponse "true"ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> akzeptieren </span> </p> </td> 
   <td colname="col2"> <p>Gzip , wenn authHeader/gzipResponse wahr ist oder kein gzipResponse-Header vorhanden ist und der HTTP Accept-Encoding-Header gzip enthält. (Standard). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immer </span> </p> </td> 
   <td colname="col2"> <p>Immer gzip-Antwort, unabhängig von Header-Werten. Verwenden Sie diesen Wert nur zum Debugging. </p> </td> 
  </tr> 
 </tbody> 
</table>
