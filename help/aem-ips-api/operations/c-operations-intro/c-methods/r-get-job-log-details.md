---
description: Ruft die Details eines Unternehmens-Auftragsprotokolls ab.
solution: Experience Manager
title: getJobLogDetails
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d2e4eea6-041b-4a80-beda-cbb8d74cd50b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 9%

---

# getJobLogDetails{#getjoblogdetails}

Ruft die Details eines Unternehmens-Auftragsprotokolls ab.

Die `logMessage` Das Antwortfeld wird basierend auf dem `authHeader` `locale` -Feld.

## Autorisierte Benutzertypen {#section-6f720a7baad64eb3805868c88af9a960}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-47d411a755224c23a4521f10341d66ab}

**Eingabe (getJobLogDetailsParam)**

<table id="table_A77122D73F684B3F8F5AFA1C11C189ED"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Erforderlich </th> 
   <th colname="col4" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Der Handle des Unternehmens, zu dem das Auftragsprotokoll gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ein Handle für einen aktiven oder abgeschlossenen Auftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ursprünglicher Name des Auftragsprotokolls. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Mindestens eine Protokolltyp-Konstante. Falls vorhanden, werden nur die angegebenen Protokolltypen zurückgegeben. Standardmäßig werden alle Protokolltypen zurückgegeben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Maximale Anzahl an <span class="codeph"> detailArray</span> zurückzugebenden Elementen. Der Höchstwert und der Standardwert sind 1000. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Seitenzahl <span class="codeph"> recordsPerPage</span>-Ergebnisse zurückgeben. Der Standardwert ist 1. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Einer der Konstantenwerte für das Auftragsdetailsortierungsfeld (Datum oder LogType). Der Standardwert ist Datum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Eine der Zeichenfolgenkonstanten Sortierrichtung . Der Standardwert ist aufsteigend. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (getJobLogDetailsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`jobLogArray`*` | `types:JobLogArray` | Ja | Array von Auftragsprotokollen. |

## Beispiele {#section-007678b8b8d94e8f91d09f6bc855f394}

Dieses Codebeispiel gibt alle Auftragsprotokolldetails für ein bestimmtes Unternehmen zurück. Das erste Array enthält standardmäßige Auftragsprotokolldetails. Ein eingebettetes Array gibt zusätzliche Informationen zum Auftrag zurück.

**Anforderung**

```java
<ns1:getJobLogDetailsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:jobHandle>47||Add_2007-09-14-15:04:34</ns1:jobHandle>
</ns1:getJobLogDetailsParam>
```

**Antwort**

```java
<getJobLogDetailsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>some_address@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
         <detailArray>
            <items>
               <logMessage>Upload has begun!</logMessage>
               <logType>BeginUpload</logType>
            </items>
            <items>
               <logMessage>Add_2007-09-14-15:04:34</logMessage>
               <logType>OriginalJobName</logType>
            </items>
            <items>
               <logMessage>s7oslo</logMessage>
               <logType>JobClient</logType>
            </items>
            ...
         </detailArray>
      </items>
   </jobLogArray>
</getJobLogDetailsReturn>
```
