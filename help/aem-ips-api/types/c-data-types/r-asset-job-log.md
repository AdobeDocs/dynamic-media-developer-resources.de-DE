---
description: Die Details eines Auftragsprotokolls, der mit einem bestimmten Asset verknüpft ist. Von getAssetJobLogs zurückgegebene Daten.
seo-description: Die Details eines Auftragsprotokolls, der mit einem bestimmten Asset verknüpft ist. Von getAssetJobLogs zurückgegebene Daten.
seo-title: AssetJobLog
solution: Experience Manager
title: AssetJobLog
topic: Scene7 Image Production System API
uuid: 0dd65da1-f358-4d9a-98a2-abfb036347e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetJobLog{#assetjoblog}

Die Details eines Auftragsprotokolls, der mit einem bestimmten Asset verknüpft ist. Von getAssetJobLogs zurückgegebene Daten.

Syntax

## Parameter {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auftragsbearbeitung </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auftragsname. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Meldung im Auftragsprotokoll. <p><span class="codeph"> Das Antwortfeld logMessage</span> wird basierend auf dem <span class="codeph"> Gebietsschema-Feld authHeader</span> lokalisiert. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auftragstyp im Protokolleintrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> E-Mail des Benutzers, der den Auftrag gesendet hat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Auftragsdatum. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> auxArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:JobLogDetailArray</span> </td> 
   <td colname="col3"> Array von Hilfsauftragsprotokollmeldungen für jedes Auftragsprotokoll. </td> 
  </tr> 
 </tbody> 
</table>

