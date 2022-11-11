---
description: Verwendet getActiveJobs zur Verfolgung von Desktop-Uploads.
solution: Experience Manager
title: UploadPostJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 60163016-fe96-4ac2-9208-da8192042d0f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 7%

---

# [!DNL UploadPostJob]{#uploadpostjob}

Verwendet getActiveJobs zur Verfolgung von Desktop-Uploads.

Siehe auch [Hochladen von Assets über HTTP-POSTs zum Hochladen...](../../c-http-post.md#concept-457855c0cdc943339ca1f1bed356991d).

>[!NOTE]
>
>Alle POST-Anforderungen für einen Upload-Auftrag müssen von derselben IP-Adresse stammen.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Erforderlich? </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoColorCropOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Optionen für automatische Zuschnitte von Bildern basierend auf Farben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoSetCreateOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Skripten zur automatischen Set-Generierung, die auf hochgeladene Dateien angewendet werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoTransparentCropOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Entfernt den Leerraum von den Kanten der Bilder basierend auf Transparenz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ColorManagementOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Optionen, die Sie während eines Uploads angeben können. Die Einstellung wirkt sich darauf aus, wie die Farbe für den Upload verwaltet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createMask</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Ja</b> </p> </td> 
   <td colname="col4"> <p>Ob eine Maske erstellt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p><b>Ja</b> </p> </td> 
   <td colname="col4"> <p>Auswahl der E-Mail-Einstellungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:InDesignOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Optionen zum Hochladen von InDesign-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> IllustratorOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:IllustratorOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Optionen zum Hochladen von Illustrator-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:KnockoutBackgroundOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Maskieren Sie den Hintergrund für ausgewählte Bilder. Auf diese Weise können Sie sie in anderen Ebenen mit einer Transparenz außerhalb des Betreffbilds überlagern. Optional. </p> <p>Siehe<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ManualCropOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Optionen für manuelles Zuschneiden von Bildern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> mediaOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:MediaOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Optionen, mit denen Sie ein Miniaturbild aus dem Video festlegen können. </p> <p>Siehe <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> overwrite</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Ja</p> </td> 
   <td colname="col4"> <p>Gibt an, ob Dateien beim Hochladen überschrieben werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:PDFOptions</span> </td> 
   <td colname="col3"> <p>Nein</p> </td> 
   <td colname="col4"> <p>Optionen zum Hochladen von PDF-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> photoshopOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:FotoshopOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Optionen zum Hochladen von Photoshop-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Die URL, in die die Dateien hochgeladen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:PostScriptOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Optionen zum Hochladen von Post-Script-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preserveCrop</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Steuert die Beibehaltung einer vorhandenen Definition des Zuschnitts. Der Standardwert ist „true“.</p> <p>Wenn Sie den Parameter manualCropOptions und die entsprechenden Werte angeben, werden die neuen Werte (außer 0,0,0,0) unabhängig vom Wert preserveCrop auf das Asset angewendet.</p><p>Wenn Sie <i>not</i> den Parameter manualCropOptions angeben, wird der Wert von preserveCrop beibehalten. Und im Fall von "true"werden die vorhandenen preserveCrop-Werte beibehalten. im Fall von false werden die Werte preserveCrop entfernt.</p><p>Beispiel:</p><p><p>&lt;preservecrop&gt;false&lt;/preservecrop&gt;<br />&lt;manualcropoptions&gt;<br />   &lt;left&gt;190&lt;/left&gt;<br />   &lt;right&gt;310&lt;/right&gt;<br />   &lt;top&gt;160&lt;/top&gt;<br />   &lt;bottom&gt;120&lt;/bottom&gt;<br />&lt;/manualcropoptions&gt;</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> preservePublishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Ja</b> </p> </td> 
   <td colname="col4"> <p>Steuert, ob der Veröffentlichungsstatus eines vorhandenen Assets beim Überschreiben beibehalten wird. Wenn nicht festgelegt, wird die Standardeinstellung für das Unternehmen verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:HandleArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Projekt-Handles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><b>Ja</b> </p> </td> 
   <td colname="col4"> <p>Gibt an, ob die Dateien für die Veröffentlichung markiert sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unCompressOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UnCompressOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Extrahieren und verarbeiten Sie den Inhalt der hochgeladenen TAR-/ZIP-Dateien mit diesen optionalen Einstellungen. </p> <p>Siehe <a href="../../types/c-data-types/r-uncompress-options.md#reference-510ec7028b1540bc9b58745f242d49d5" format="dita" scope="local"> UnCompressOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> unsharpMaskOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UnsharpMaskOptions</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Optionen, mit denen Sie die Einstellungen der Unschärfemaske beim Erstellen einer optimierten Pyramid TIF-Datei steuern können. Verwenden Sie diese Einstellungen, um die Bildschärfe zu verbessern. </p> <p>Siehe <a href="../../types/c-data-types/r-unsharp-mask-options.md#reference-b9a96244d7ee4424bc4ac3c23be3be3d" format="dita" scope="local"> UnsharpMaskOptions</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> xmpKeywords</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Eine zusätzliche Metadatenoption für alle Elemente im Upload-Auftrag. </p> </td> 
  </tr> 
 </tbody> 
</table>
