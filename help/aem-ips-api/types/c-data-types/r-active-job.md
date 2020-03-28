---
description: Ein Auftrag, der auf einem Server ausgeführt wird. Außerdem handelt es sich um eine Instanz eines geplanten Auftrags.
seo-description: Ein Auftrag, der auf einem Server ausgeführt wird. Außerdem handelt es sich um eine Instanz eines geplanten Auftrags.
seo-title: ActiveJob
solution: Experience Manager
title: ActiveJob
topic: Scene7 Image Production System API
uuid: d7120a88-6f3e-4844-aafa-83d419470fad
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ActiveJob{#activejob}

Ein Auftrag, der auf einem Server ausgeführt wird. Außerdem handelt es sich um eine Instanz eines geplanten Auftrags.

Aufträge gibt es in drei Status:

* Ausführung geplant.
* Wird derzeit ausgeführt.
* Ausführung abgeschlossen (und bereits Informationen in ein Auftragsprotokoll geschrieben).

Geben Sie einen Auftragstypwert an, um den Auftragstyp zurückzugeben. Sie können die folgenden Aufträge zurückgeben:

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Benutzen Sie die Firma. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nehmen Sie mit dem Auftrag Kontakt auf. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Name</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Eindeutiger Name für den Auftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Ursprünglicher Name des mit dem Auftrag gesendeten <span class="codeph"> ActiveJob</span> -Typs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auswahl der vom System zurückgegebenen Auftragstypen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auswahl der vom System zurückgegebenen Status aktiver Aufträge. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> E-Mail-Adresse des Benutzers, der den Auftrag geplant hat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Das Gebietsschema für Auftragsprotokolldetails und E-Mail-lokale Anpassung. <p>Geben Sie Gebietsschemata als <span class="codeph"> &lt;language_code&gt;[-&lt;country_code&gt;]</span>an, wobei der Sprachencode aus Kleinbuchstaben und aus zwei Buchstaben besteht, wie in ISO-639 angegeben, und der optionale Ländercode aus Großbuchstaben besteht, die aus zwei Buchstaben bestehen, wie in ISO-3166 angegeben. Die Zeichenfolge für Englisch (USA) lautet beispielsweise: <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Beschreibung</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Auftragsbeschreibung, die ursprünglich im <span class="codeph"> submitJob</span>angegeben wurde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Servername</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Name des Servers, auf dem der Auftrag ausgeführt wird. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Startdatum</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum, Uhrzeit und Zeitzone des aktiven Auftrags. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Gesamtgröße des aktiven Auftrags. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Fortschritt</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Auftragsfortschritt (d. h. wie nahe der Abschluss des Auftrags ist). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Eine Textmeldung, die den Auftragsstatus beschreibt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> lastProgressUpdate <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum, Uhrzeit und Zeitzone der letzten Aktualisierung des Fortschritts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:TaskProgressArray</span> </td> 
   <td colname="col3"> Informationen zum Fortschritt der asynchronen Aufgabe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageServingPublishJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Image Serving-Veröffentlichungsauftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageServingRenderJob <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageServingRenderJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Image Render-Veröffentlichungsauftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:VideoPublishJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Videoveröffentlichungsauftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Veröffentlichungsauftrag im Serververzeichnis. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UploadUrlsJob</span> </td> 
   <td colname="col3"> Auftragsdetails für einen Upload-URLs-Auftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UploadPostJob</span> </td> 
   <td colname="col3"> Auftragsdetailverfolgung beim Hochladen auf dem Desktop. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ExportJob</span> </td> 
   <td colname="col3">Zulassen des autorisierten Exports von zuvor hochgeladenen Dateien. Siehe <a href="https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_exportjob.html" format="http" scope="external"> Exportauftrag</a>. </td> 
  </tr> 
 </tbody> 
</table>

