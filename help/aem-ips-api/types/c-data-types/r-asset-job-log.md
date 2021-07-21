---
description: Die Details eines Auftragsprotokolleintrags, der mit einem bestimmten Asset verknüpft ist. Von getAssetJobLogs zurückgegebene Daten.
solution: Experience Manager
title: AssetJobLog
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2c8ebec2-a664-46cd-b843-9893bfa0a9d1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 6%

---

# AssetJobLog{#assetjoblog}

Die Details eines Auftragsprotokolleintrags, der mit einem bestimmten Asset verknüpft ist. Von getAssetJobLogs zurückgegebene Daten.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auftragshandle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auftragsname. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Meldung im Auftragsprotokoll. <p><span class="codeph"> Das Feld </span> logMessageresponse wird basierend auf dem Feld  <span class="codeph"> </span> authHeaderlocale lokalisiert. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Auftragstyp im Protokolleintrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> E-Mail des Benutzers, der den Auftrag gesendet hat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Auftragsdatum. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> auxArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:JobLogDetailArray</span> </td> 
   <td colname="col3"> Array von Protokollnachrichten für Hilfsaufträge für jedes Auftragsprotokoll. </td> 
  </tr> 
 </tbody> 
</table>
