---
description: Ein Prozess, der ein vorhandenes PDF-Asset erneut extrahiert.
seo-description: Ein Prozess, der ein vorhandenes PDF-Asset erneut extrahiert.
seo-title: RipPdfsJob
solution: Experience Manager
title: RipPdfsJob
topic: Scene7 Image Production System API
uuid: 95990d53-4baf-44a2-8d84-3cab2b5c9105
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# RipPdfsJob{#rippdfsjob}

Ein Prozess, der ein vorhandenes PDF-Asset erneut extrahiert.

>[!NOTE]
>
>Dieser Auftragstyp ist veraltet. Transition für `ReprocessAssetsJob` alle zukünftigen Integrationen.

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
   <td colname="col1"> <p><span class="codeph"> pdfHandleArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Handle mit dem Array der zu rippenden PDF-Dateien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Legt fest, ob eine Maske erstellt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Manuelle Beschneidungsoptionen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Automatische Beschneidungsoptionen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> PDF- <span class="varname"> Optionen</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Ein Array von Projekthandles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>E-Mail-Einstellungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Die URL, in die die Dateien hochgeladen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postImageServingPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails, damit ein Image-Server-Veröffentlichungsauftrag nach Abschluss des Uploads ausgeführt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postImageRenderingPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails, damit ein Veröffentlichungsauftrag zum Rendern eines Bilds nach Abschluss des Uploads ausgeführt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> postVideoPublishJob <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails, damit ein Videoveröffentlichungsauftrag nach Abschluss des Uploads ausgeführt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> InDesign-Optionen</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Adobe InDesign-Dateien auf den Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> knockout <span class="varname"> Background</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Maskiert den Hintergrund für ausgewählte Bilder. Dadurch können Sie sie in anderen Ebenen mit einer Transparenz außerhalb des Betreffbilds überlagern. </p> <p>Optional. </p> <p>Siehe<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anmerkungen {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

Zu den Optionen `*CropOptions` gehören:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Zu den Optionen `*PublishJob` gehören:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`

