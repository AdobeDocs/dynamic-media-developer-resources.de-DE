---
description: Auftragstyp, um die erneute Verarbeitung bereits hochgeladener Primärdateien zu ermöglichen, einschließlich der Wiedergabe von PDFs und der Neuoptimierung von Bildern.
seo-description: Auftragstyp, um die erneute Verarbeitung bereits hochgeladener Primärdateien zu ermöglichen, einschließlich der Wiedergabe von PDFs und der Neuoptimierung von Bildern.
seo-title: ReprocessAssetsJob
solution: Experience Manager
title: ReprocessAssetsJob
topic: Dynamic Media Image Production System API
uuid: 5b4aa838-0fb4-4ae8-be5a-8ce1e1487127
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 2%

---


# ReprocessAssetsJob{#reprocessassetsjob}

Auftragstyp, um die erneute Verarbeitung bereits hochgeladener Primärdateien zu ermöglichen, einschließlich der Wiedergabe von PDFs und der Neuoptimierung von Bildern.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Asset-Handle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Ob die Dateien als veröffentlichungsbereit markiert wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Steuert, ob der Veröffentlichungsstatus eines vorhandenen Assets beim Überschreiben beibehalten wird. Ist dies nicht der Fall, wird die Standardeinstellung für die Firma verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Legt fest, ob eine Maske erstellt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Steuert die Beibehaltung einer vorhandenen Schnittdefinition. Der Standardwert ist „true“.</p> <p>Wenn Sie den Parameter manualCropOptions und die entsprechenden Werte angeben, werden die neuen Werte (außer 0,0,0,0) unabhängig vom Wert preserveCrop auf das Asset angewendet.</p><p>Wenn Sie <i>not</i> den Parameter manualCropOptions angeben, wird der Wert von preserveCrop beibehalten. Und bei true werden die vorhandenen preserveCrop-Werte beibehalten. Bei false werden die preserveCrop-Werte entfernt.</p><p>Beispiel:</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />    &lt;left&gt;190&lt;/left&gt;<br />    &lt;right&gt;310&lt;/right&gt;<br />    &lt;top&gt;160&lt;/top&gt;<br />    &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Manuelle Beschneidungsoptionen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen für die automatische Beschneidung von Bildern basierend auf Farbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Entfernt den Leerraum von den Kanten der Bilder, basierend auf Transparenz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:FotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Photoshop-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von PostScript-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von PDF-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen für A/V-Mediendateien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Illustrator-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen, die Sie beim Hochladen angeben können. Die Einstellung wirkt sich darauf aus, wie die Farbe für den Hochladevorgang verwaltet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Array von Skripten zur automatischen Set-Generierung, die auf hochgeladene Dateien angewendet werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Ein Array von Projekthandles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Optionen für E-Mail-Einstellungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Legt fest, ob nur Dateien hochgeladen werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>URL zum Speicherort des Datei-Uploads. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails, damit ein Image-Server-Veröffentlichungsauftrag nach Abschluss des Uploads ausgeführt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails, damit ein Veröffentlichungsauftrag zum Rendern eines Bilds nach Abschluss des Uploads ausgeführt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails, damit ein Videoveröffentlichungsauftrag nach Abschluss des Uploads ausgeführt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von InDesign-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Maskiert den Hintergrund für ausgewählte Bilder. Dadurch können Sie sie in anderen Ebenen mit einer Transparenz außerhalb des Betreffbilds überlagern. </p> <p>Optional. </p> <p>Siehe<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:UnsharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen, mit denen Sie die Einstellungen für Unschärfemaske beim Erstellen einer optimierten Pyramidendatei steuern können. Verwenden Sie diese Einstellungen, um die Bildschärfe zu verbessern. </p> <p>Siehe <a href="https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Anmerkungen**

Zu den Optionen für `*CropOptions` gehören:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Zu den Optionen für `*PublishJob` gehören:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

