---
description: Lädt Dateien aus angegebenen Serverordnern wiederholt hoch.
seo-description: Lädt Dateien aus angegebenen Serverordnern wiederholt hoch.
seo-title: UploadDirectoryJob
solution: Experience Manager
title: UploadDirectoryJob
topic: Scene7 Image Production System API
uuid: 6e6ae415-7c54-4bbb-aa98-ff9a77d956b0
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# UploadDirectoryJob{#uploaddirectoryjob}

Lädt Dateien aus angegebenen Serverordnern wiederholt hoch.

Syntax

## Parameter {#section-69c07f4e7b2e4a0fba143ffaa9f4d48f}

<table id="table_6E40A78846F444BDB8E437413B90CFCE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoColorOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoColorOptions</span> </td> 
   <td colname="col3"> <p>Automatische Optionen zum Beschneiden von Bildern (je nach Farbe). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoSetCreationOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Array von Skripten zur automatischen Set-Generierung, die auf hochgeladene Dateien angewendet werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Entfernt den Leerraum von den Kanten der Bilder, basierend auf Transparenz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Optionen, die Sie beim Hochladen angeben können. Die Einstellung wirkt sich darauf aus, wie die Farbe für den Hochladevorgang verwaltet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Legt fest, ob beim Hochladen eine Maske erstellt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> älteste Ordner</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>IPS-Ordner für die Dateien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Auswahl der E-Mail-Einstellungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Illustrator-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> Unterordner <span class="varname"> einschließen</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Gibt an, ob beim Hochladen Unterordner einbezogen werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> InDesign-Optionen</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von InDesign-Dateien auf den Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> knockout <span class="varname"> Background</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Maskiert den Hintergrund für ausgewählte Bilder. Dadurch können Sie sie in anderen Ebenen mit einer Transparenz außerhalb des Betreffbilds überlagern. </p> <p>Optional. </p> <p>Siehe <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Manuelle Optionen zum Beschneiden von Bildern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:MediaOptions</span> </td> 
   <td colname="col3"> <p>Optionen, mit denen Sie ein Miniaturbild aus dem Video festlegen können. </p> <p>Siehe <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> Medienoptionen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> überschreiben</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Optionen zum Überschreiben von Dateien beim Hochladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> PDF- <span class="varname"> Optionen</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:PDFOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von PDF-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:FotoshopOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Fotoshop-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Die URL des Dateiupload-Ziels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingVeröffentlichungsauftrag</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>Details zu einem Image Rendering-Veröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postImageServingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>Details zu einem Image Serving-Veröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Legt fest, ob nur Dateien hochgeladen werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von PostScript-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postVideoPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:VideoPublishJob</span> </td> 
   <td colname="col3"> <p>Details zu einem Videoveröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Steuert die Beibehaltung einer vorhandenen Schnittdefinition. Der Standardwert ist true. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Steuert, ob der Veröffentlichungsstatus eines vorhandenen Assets beim Überschreiben beibehalten wird. Ist dies nicht der Fall, wird die Standardeinstellung für die Firma verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Gibt an, ob für diesen Auftrag separate Metadaten-XML-Dateien verarbeitet werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:HandleArray</span> </td> 
   <td colname="col3"> <p>Array von Projekthandles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Bestimmt, ob Dateien für die Veröffentlichung markiert wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Dir</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Upload-Ordner der Quelle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> unCompressOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Extrahieren und verarbeiten Sie den Inhalt der hochgeladenen TAR-/ZIP-Dateien mit diesen optionalen Einstellungen. </p> <p>Siehe <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Optionen, mit denen Sie die Einstellungen für Unschärfemaske beim Erstellen einer optimierten Pyramidendatei steuern können. Verwenden Sie diese Einstellungen, um die Bildschärfe zu verbessern. </p> <p>Siehe <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_unsharp_mask_options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> xmpKeywords <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Eine zusätzliche Metadatenoption für alle Elemente im Upload-Auftrag </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anmerkungen {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Sie `CropOptions`können beispielsweise nur eine der folgenden Optionen auswählen:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Sie `PublishJob`können beispielsweise nur eine der folgenden Optionen auswählen:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

