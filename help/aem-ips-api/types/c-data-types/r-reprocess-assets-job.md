---
description: Vorgangstyp, um die Neuverarbeitung zuvor hochgeladener Primärdateien zu ermöglichen, einschließlich Neukomprimierung von PDFs und Neuoptimierung von Bildern.
solution: Experience Manager
title: AssetsJob neu verarbeiten
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6078246-54e1-4119-b4f8-ba6a28577cff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 2%

---

# [!DNL ReprocessAssetsJob]{#reprocessassetsjob}

Vorgangstyp, um die Neuverarbeitung zuvor hochgeladener Primärdateien zu ermöglichen, einschließlich Neukomprimierung von PDFs und Neuoptimierung von Bildern.

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
   <td colname="col2"> <p><span class="codeph">:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Asset-Handle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> readyForPublish</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Ob die Dateien zur Veröffentlichung bereit markiert sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preservePublishState</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Steuert, ob der Veröffentlichungsstatus eines vorhandenen Assets beim Überschreiben beibehalten wird. Ist dies nicht festgelegt, wird die Standardeinstellung des Unternehmens verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Ob eine Maske erstellt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> preserveCrop</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Steuert die Beibehaltung vorhandener Zuschnittdefinitionen. Der Standardwert ist „true“.</p> <p>Wenn Sie den manualCropOptions-Parameter und die entsprechenden Werte angeben, werden die neuen Werte (ohne 0,0,0,0) unabhängig vom preserveCrop-Wert auf das Asset angewendet.</p><p>Wenn Sie <i>nicht</i> den Parameter manualCropOptions angeben, wird der Wert von preserveCrop beibehalten. Im Fall von „true“ werden die vorhandenen preserveCrop-Werte beibehalten. Im Fall von „false“ werden die preserveCrop-Werte entfernt.</p><p>Beispiel:</p><p><p>&lt;preserveCrop&gt;false&lt;/preserveCrop&gt;<br />&lt;manualCropOptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualCropOptions&gt;</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Manuelles Zuschneiden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen für das automatische Zuschneiden von Bildern basierend auf Farben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:AutoTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Entfernt Leerraum an den Bildrändern, basierend auf Transparenz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:FotoshopOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Photoshop-Dateien auf den Bildserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von PostScript-Dateien auf den Bildserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von PDF-Dateien auf den Bildserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> mediaOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:MediaOptions</span> </p> </td> 
   <td colname="col3"> <p>A/V-Mediendateioptionen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Illustrator-Dateien auf den Bildserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen, die Sie während eines Uploads angeben können. Der Satz wirkt sich darauf aus, wie die Farbe für den Upload verwaltet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:AutoSetCreationOptions</span> </p> </td> 
   <td colname="col3"> <p>Array von Skripten zur automatischen Satzgenerierung, die auf hochgeladene Dateien angewendet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Ein Array von Projekt-Handles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Optionen für E-Mail-Einstellungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postJobOnlyIfFiles</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:Boolean</span> </p> </td> 
   <td colname="col3"> <p>Ob nur Dateien hochgeladen werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>URL zum Speicherort des Datei-Uploads. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails für einen Image-Serving-Veröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails für einen Image-Rendering-Veröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails für einen Videoveröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von InDesign-Dateien auf den Bildserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Den Hintergrund für ausgewählte Bilder maskieren. Auf diese Weise können Sie sie in anderen Ebenen mit einer Transparenz außerhalb des Betreffbildes überlagern. </p> <p>Optional. </p> <p>Siehe<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> unSharpMaskOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:UnSharpMaskOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen, mit denen Sie die Einstellungen für Unschärfemasken beim Erstellen einer optimierten Pyramid TIF-Datei steuern können. Verwenden Sie diese Einstellungen, um die Bildschärfe zu verbessern. </p> <p>Siehe <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-unsharp-mask-options.html?lang=de"> UnschärfemaskenOptionen</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Hinweise**

Zu den Auswahlmöglichkeiten für `*CropOptions` gehören:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Zu den Auswahlmöglichkeiten für `*PublishJob` gehören:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
