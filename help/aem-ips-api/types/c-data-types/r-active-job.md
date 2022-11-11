---
title: ActiveJob
description: Ein Auftrag, der auf einem Server ausgeführt wird. Außerdem handelt es sich um eine Instanz eines geplanten Auftrags.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3d878207-99e4-4c75-ab12-b38a37c82fb7
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 1%

---

# [!DNL ActiveJob]{#activejob}

Ein Auftrag, der auf einem Server ausgeführt wird. Außerdem handelt es sich um eine Instanz eines geplanten Auftrags.

Aufträge sind in drei Status verfügbar:

* Geplant für die Ausführung.
* Wird derzeit ausgeführt.
* Ausführung abgeschlossen (und bereits Informationen in ein Auftragsprotokoll geschrieben).

Um den Auftragstyp zurückzugeben, geben Sie einen Auftragstyp-Wert an. Sie können die folgenden Aufträge zurückgeben:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## Parameter {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Handle mit dem Unternehmen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Führen Sie den Auftrag aus. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Eindeutiger Name für den Auftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Ursprünglicher Name der <span class="codeph"> ActiveJob</span> Typ, der mit dem Auftrag gesendet wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auswahl der vom System zurückgegebenen Auftragstypen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auswahl der vom System zurückgegebenen aktiven Auftragsstatus. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> E-Mail-Adresse des Benutzers, der den Auftrag geplant hat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Das Gebietsschema für Auftragsprotokolldetails und E-Mail-Lokalisierung. <p>Gebietsschemata als <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>, wobei der Sprachcode ein aus zwei Buchstaben bestehender Code in Kleinbuchstaben ist, wie in ISO-639 angegeben, und der optionale Ländercode ein aus Großbuchstaben bestehender Code aus zwei Buchstaben gemäß ISO-3166 ist. Die Gebietsschema-Zeichenfolge für Englisch (USA) lautet beispielsweise: <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Die ursprünglich unter <span class="codeph"> submitJob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Name des Servers, auf dem der Auftrag ausgeführt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum, Uhrzeit und Zeitzone für den aktiven Auftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gesamtgröße des aktiven Auftrags. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progress</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Auftragsfortschritt (d. h. wie nah der Auftrag am Ende ist). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Eine Textmeldung, die den Auftragsfortschritt beschreibt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum, Uhrzeit und Zeitzone der letzten Aktualisierung des Fortschritts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:TaskProgressArray</span> </td> 
   <td colname="col3"> Informationen zum Fortschritt asynchroner Aufgaben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Image-Serving-Veröffentlichungsauftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageServingRenderJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Image-Rendering-Veröffentlichungsauftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:VideoPublishJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Video-Veröffentlichungsauftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Veröffentlichungsauftrag in Serverordnern. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UploadUrlsJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Upload-URLs-Auftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UploadPostJob</span> </td> 
   <td colname="col3"> Auftragsdetails, Tracking des Desktop-Uploads. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ExportJob</span> </td> 
   <td colname="col3">Zulassen des autorisierten Exports von zuvor hochgeladenen Dateien. Siehe <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-exportjob.html" format="http" scope="external"> Exportauftrag</a>. </td> 
  </tr> 
 </tbody> 
</table>
