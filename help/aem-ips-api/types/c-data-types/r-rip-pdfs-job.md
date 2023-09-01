---
title: RipPdfsJob
description: Ein Prozess, der ein vorhandenes PDF-Asset erneut erzeugt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7a787b45-3cda-44f2-8357-8b6217b679e0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---

# [!DNL RipPdfsJob]{#rippdfsjob}

Ein Prozess, der ein vorhandenes PDF-Asset erneut erzeugt.

>[!NOTE]
>
>Dieser Auftragstyp wird nicht mehr unterstützt. Übergang zu `ReprocessAssetsJob` für alle zukünftigen Integrationen.

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Handle mit dem Array der zu rippenden PDF-Dateien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> createMask</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:boolean</span> </p> </td> 
   <td colname="col3"> <p>Bestimmt, ob Sie eine Maske erstellen möchten oder nicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> manualCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ManualCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Manuelles Zuschneiden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoColorCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:AutoColorCropOptions</span> </p> </td> 
   <td colname="col3"> <p>Automatische Zuschneideoptionen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> autoTransparentCropOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:PostTransparentCropOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postScriptOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:PostScriptOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> pdfOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:PDFOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> illustratorOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:IllustratorOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> colorManagementOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ColorManagementOptions</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> projectHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>Ein Array von Projekt-Handles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>E-Mail-Einstellungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postHttpUrl</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Die URL, in die die Dateien hochgeladen werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageServingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ImageServingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails für einen Image Serving-Veröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postImageRenderingPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:ImageRenderingPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails für einen Veröffentlichungsauftrag zum Rendern von Bildern, der nach Abschluss des Uploads ausgeführt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> postVideoPublishJob</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:VideoPublishJob</span> </p> </td> 
   <td colname="col3"> <p>Auftragsdetails für einen Videoveröffentlichungsauftrag, der nach Abschluss des Uploads ausgeführt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> inDesignOptions</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:InDesignOptions</span> </p> </td> 
   <td colname="col3"> <p>Optionen zum Hochladen von Adobe InDesign-Dateien auf den Bildserver. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> knockoutBackground</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> Typen:KnockoutBackgroundOptions</span> </p> </td> 
   <td colname="col3"> <p>Maskieren Sie den Hintergrund für ausgewählte Bilder. Mit dieser Funktion können Sie sie in anderen Ebenen mit einer Transparenz außerhalb des Betreffbilds überlagern. </p> <p>Optional. </p> <p>Siehe<a href="../../types/c-data-types/r-knockout-background-options.md#reference-9196371848964d91842b337640791c9c" format="dita" scope="local"> KnockoutBackgroundOptions</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Anmerkungen {#section-0822e70fa4784131baa5ad0ba8c0fb3b}

Auswahlmöglichkeiten für `*CropOptions` include:

* `manualCropOptions`
* `autoColorCropOptions`
* `autoTransparentCropOptions`

Auswahlmöglichkeiten für `*PublishJob` include:

* `postImageServingPublishJob`
* `postImageRenderingPublishJob`
* `postVideoPublishJob`
