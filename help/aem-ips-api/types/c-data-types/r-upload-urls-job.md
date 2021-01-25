---
description: Lädt URLs von dem Speicherort hoch, an den Sie Dateien abrufen möchten.
seo-description: Lädt URLs von dem Speicherort hoch, an den Sie Dateien abrufen möchten.
seo-title: UploadUrlsJob
solution: Experience Manager
title: UploadUrlsJob
topic: Dynamic Media Image Production System API
uuid: 6140e969-bf61-4b62-9a60-29609626b0b4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 1%

---


# UploadUrlsJob{#uploadurlsjob}

Lädt URLs von dem Speicherort hoch, an den Sie Dateien abrufen möchten.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoColorCropOptions</span> </td> 
   <td colname="col3"> Optionen für die automatische Beschneidung von Bildern basierend auf Farbe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoSetCreationOptions</span> </td> 
   <td colname="col3"> Array von Skripten zur automatischen Set-Generierung, die auf hochgeladene Dateien angewendet werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> Entfernt den Leerraum von den Kanten der Bilder, basierend auf Transparenz. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Legt fest, ob eine Maske erstellt werden soll. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ColorManagementOptions</span> </td> 
   <td colname="col3"> Optionen, die Sie beim Hochladen angeben können. Die Einstellung wirkt sich darauf aus, wie die Farbe für den Hochladevorgang verwaltet wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auswahl der E-Mail-Einstellungen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:IllustratorOptions</span> </td> 
   <td colname="col3"> Optionen zum Hochladen von Illustrator-Dateien auf den Image-Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:InDesignOptions</span> </td> 
   <td colname="col3"> Optionen zum Hochladen von InDesign-Dateien auf den Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3">Maskiert den Hintergrund für ausgewählte Bilder. Dadurch können Sie sie in anderen Ebenen mit einer Transparenz außerhalb des Betreffbilds überlagern. Optional. Siehe<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ManualCropOptions</span> </td> 
   <td colname="col3"> Optionen für manuelle Beschneidungen von Bildern. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:MediaOptions</span> </td> 
   <td colname="col3">Optionen, mit denen Sie ein Miniaturbild aus dem Video festlegen können. Siehe <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numUrls</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3">Gibt die Anzahl der URLs zurück, die in einem Auftrag gesendet wurden. Verwendet von <a href="../../operations/c-operations-intro/c-methods/r-get-active-jobs.md#reference-67483cbd71d04042b48434d886e8a7a0" format="dita" scope="local"> getActiveJobs</a> und <a href="../../operations/c-operations-intro/c-methods/r-get-scheduled-jobs.md#reference-2bab1861325f4bff84c879d1efa9146e" format="dita" scope="local"> getScheduledJobs</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> überschreiben</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Gibt an, ob Dateien beim Hochladen überschrieben werden sollen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:PDFOptions</span> </td> 
   <td colname="col3"> Optionen zum Hochladen von PDF-Dateien auf den Image-Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:FotoshopOptions</span> </td> 
   <td colname="col3"> Optionen zum Hochladen von Photoshop-Dateien auf den Image-Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Die URL, unter der die Dateien hochgeladen werden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> Details zu einem Image Rendering-Veröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Alle Medienoptionen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:PostScriptOptions</span> </td> 
   <td colname="col3"> Optionen zum Hochladen von PostScript-Dateien auf den Image-Server. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:VideoPublishJob</span> </td> 
   <td colname="col3"> Details zu einem Videoveröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Steuert die Beibehaltung einer vorhandenen Schnittdefinition. Standard ist true </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Steuert, ob der Veröffentlichungsstatus eines vorhandenen Assets beim Überschreiben beibehalten wird. Ist dies nicht der Fall, wird die Standardeinstellung für die Firma verwendet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:HandleArray</span> </td> 
   <td colname="col3"> Array von Projekthandles. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Ob die Dateien als veröffentlichungsbereit markiert wurden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UnCompressOptions</span> </td> 
   <td colname="col3">Extrahieren und verarbeiten Sie den Inhalt der hochgeladenen TAR-/ZIP-Dateien mit diesen optionalen Einstellungen. Siehe <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UnsharpMaskOptions</span> </td> 
   <td colname="col3">Optionen, mit denen Sie die Einstellungen für Unschärfemaske beim Erstellen einer optimierten Pyramidendatei steuern können. Verwenden Sie diese Einstellungen, um die Bildschärfe zu verbessern. Siehe <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> urlArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:UrlArray</span> </td> 
   <td colname="col3"> Ein Array von URLs, die Sie hochladen möchten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Eine zusätzliche Metadatenoption für alle Elemente im Upload-Auftrag. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anmerkungen {#section-637405ff7e0b4a71b83fd359b92fa0c2}

Für `CropOptions` können Sie nur eine der folgenden Optionen auswählen:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Für `PublishJob` können Sie nur eine der folgenden Optionen auswählen:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postvideoPublishJob`

