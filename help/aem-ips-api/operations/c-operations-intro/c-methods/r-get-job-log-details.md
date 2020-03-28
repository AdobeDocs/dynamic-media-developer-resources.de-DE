---
description: Ruft die Details des Auftragsprotokolls einer Firma ab.
seo-description: Ruft die Details des Auftragsprotokolls einer Firma ab.
seo-title: getJobLogDetails
solution: Experience Manager
title: getJobLogDetails
topic: Scene7 Image Production System API
uuid: e4314348-2160-4775-a02f-b4892924f064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getJobLogDetails{#getjoblogdetails}

Ruft die Details des Auftragsprotokolls einer Firma ab.

Das `logMessage` Antwortfeld wird basierend auf dem `authHeader` Feld lokalisiert `locale` .

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

**Input (getJobLogDetailsParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Das Handle der Firma, zu der das Auftragsprotokoll gehört. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ein Handle für einen aktiven oder abgeschlossenen Auftrag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Ursprünglicher Name des Auftragsprotokolls. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:StringArray</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> Eine oder mehrere Protokolltyp-Konstanten. Falls vorhanden, werden nur die angegebenen Protokolltypen zurückgegeben. Standardmäßig werden alle Protokolltypen zurückgegeben. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> recordsPerPage <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Maximale Anzahl der <span class="codeph"> DetailArray</span> -Elemente, die zurückgegeben werden sollen. Der Höchst- und Standardwert ist 1000. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Ergebnisseite</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4">Seitenzahl der zurückzugebenden <span class="codeph"> DatensätzePerPage</span>-Ergebnisse. Der Standardwert ist 1. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortieren nach</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Einer der Konstantenwerte für "Auftragsdetails-Sortierfeld"(Datum oder LogType). Der Standardwert ist Datum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Sortierrichtung</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Eine der Zeichenfolgenkonstanten "Sortierrichtung". Der Standardwert ist aufsteigend. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getJobLogDetailsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`jobLogArray`*` | `types:JobLogArray` | Ja | Array von Auftragsprotokollen. |

## Beispiele {#section-007678b8b8d94e8f91d09f6bc855f394}

Dieses Codebeispiel gibt alle Auftragsprotokolldetails für eine bestimmte Firma zurück. Das erste Array enthält Standardauftragsprotokolldetails. Ein eingebettetes Array gibt weitere Informationen zum Auftrag zurück.

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

