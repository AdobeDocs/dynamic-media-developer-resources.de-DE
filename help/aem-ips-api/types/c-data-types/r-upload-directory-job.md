---
description: Lädt Dateien aus angegebenen Serververzeichnissen wiederholt hoch.
solution: Experience Manager
title: UploadDirectoryJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a23f1bc2-aa6a-4c1d-aab5-7f6dbd08682c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---

# [!DNL UploadDirectoryJob]{#uploaddirectoryjob}

Lädt Dateien aus angegebenen Serververzeichnissen wiederholt hoch.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoColorOptions</span> </td> 
   <td colname="col3"> <p>Automatische Bildbeschneidungsoptionen (basierend auf Farbe). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Array von Skripten zur automatischen Set-Generierung, die auf hochgeladene Dateien angewendet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Entfernt den Leerraum von den Kanten der Bilder basierend auf Transparenz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Optionen, die Sie während eines Uploads angeben können. Die Einstellung wirkt sich darauf aus, wie die Farbe für den Upload verwaltet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Ob beim Hochladen eine Maske erstellt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>IPS-Ordner für die Dateien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Auswahl der E-Mail-Einstellungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Illustrator-Dateien auf den Bildserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Gibt an, ob beim Hochladen Unterordner hinzugefügt werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von InDesign-Dateien auf den Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Maskieren Sie den Hintergrund für ausgewählte Bilder. Auf diese Weise können Sie sie in anderen Ebenen mit einer Transparenz außerhalb des Betreffbilds überlagern. </p> <p>Optional. </p> <p>Siehe <a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Manuelles Zuschneiden von Bildern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:MediaOptions</span> </td> 
   <td colname="col3"> <p>Optionen, mit denen Sie ein Miniaturbild aus dem Video festlegen können. </p> <p>Siehe <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> overwrite</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Optionen zum Überschreiben von Dateien beim Hochladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PDFOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von PDF-Dateien auf den Bildserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:FotoshopOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Photoshop-Dateien auf den Bildserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Die URL des Dateiupload-Ziels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageRenderingPublish</span> </span>Job </td> 
   <td colname="col2"> <span class="codeph"> types:ImageRendingPublishJob</span> </td> 
   <td colname="col3"> <p>Details für einen Image Rendering-Veröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:ImageServingPublishJob</span> </td> 
   <td colname="col3"> <p>Details zu einem Image Serving-Veröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Ob nur Dateien hochgeladen werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von PostScript-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:VideoPublishJob</span> </td> 
   <td colname="col3"> <p>Details zu einem Video-Veröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Steuert die Beibehaltung einer vorhandenen Definition des Zuschnitts. Der Standardwert ist "true". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Steuert, ob der Veröffentlichungsstatus eines vorhandenen Assets beim Überschreiben beibehalten wird. Wenn nicht festgelegt, wird die Standardeinstellung für das Unternehmen verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processMetadataFiles</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Ob für diesen Auftrag separate Metadaten-XML-Dateien verarbeitet werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>Array von Projekt-Handles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Bestimmt, ob Dateien für die Veröffentlichung markiert sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDir</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Source-Upload-Verzeichnis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Extrahieren und verarbeiten Sie den Inhalt der hochgeladenen TAR-/ZIP-Dateien mit diesen optionalen Einstellungen. </p> <p>Siehe <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Optionen, mit denen Sie die Einstellungen der Unschärfemaske beim Erstellen einer optimierten Pyramid TIF-Datei steuern können. Verwenden Sie diese Einstellungen, um die Bildschärfe zu verbessern. </p> <p>Siehe <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnschärfemaskeOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> xmpKeywords</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Eine zusätzliche Metadatenoption für alle Elemente im Upload-Auftrag </p> </td> 
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
