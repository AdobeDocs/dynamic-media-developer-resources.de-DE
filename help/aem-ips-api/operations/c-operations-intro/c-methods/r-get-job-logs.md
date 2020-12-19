---
description: Ruft die angegebenen Auftragsprotokolle für die ausgewählte Firma ab. Sie können nach Zeichen, Richtung, Beginn- und Enddatum und Anzahl der Zeilen sortieren.
seo-description: Ruft die angegebenen Auftragsprotokolle für die ausgewählte Firma ab. Sie können nach Zeichen, Richtung, Beginn- und Enddatum und Anzahl der Zeilen sortieren.
seo-title: getJobLogs
solution: Experience Manager
title: getJobLogs
topic: Scene7 Image Production System API
uuid: 850ccfad-6cdb-4eda-a20a-762fadadf8b2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 10%

---


# getJobLogs{#getjoblogs}

Ruft die angegebenen Auftragsprotokolle für die ausgewählte Firma ab. Sie können nach Zeichen, Richtung, Beginn- und Enddatum und Anzahl der Zeilen sortieren.

Syntax

## Autorisierte Benutzertypen {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-8cfdc7994da24678a45edcb37e9a2166}

**Input (getJobLogsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Nein | Der Griff der Firma. |
| ` *`userHandle`*` | `xsd:string` | Nein | Ruft Protokolle für Aufträge ab, die von einem bestimmten Benutzer gesendet wurden. |
| ` *`sortBy`*` | `xsd:string` | Nein | Ermöglicht die Auswahl der Sortierfelder. |
| ` *`sortDirection`*` | `xsd:string` | Nein | Sortierreihenfolge (aufsteigend oder absteigend). |
| ` *`startDate`*` | `xsd:dateTime` | Nein | Datum und Uhrzeit des Beginns des Auftragsprotokolls. Geben Sie die Zeitzone mit der Anforderung für dieses Feld ein. |
| ` *`endDate`*` | `xsd:dateTime` | Nein | Datum und Uhrzeit des Endes des Auftragsprotokolls. Geben Sie die Zeitzone mit der Anforderung für dieses Feld ein. |
| ` *`numRows`*` | `xsd:int` | Nein | Maximale Anzahl der zurückzugebenden Zeilen. |

**Output (getJobLogsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`jobLogArray`*` | `types: JobLogArray` | Ja | Array von Auftragsprotokollen. |

## Beispiele {#section-35871c94b4a44559912577efddbc46a6}

Dieses Codebeispiel gibt IPS-Auftragsprotokolle für eine bestimmte Firma zurück. Sie können damit auch Auftragsprotokolle für einen bestimmten Benutzer oder eine bestimmte Firma und einen bestimmten Benutzer zurückgeben.

**Anforderung**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**Antwort**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```

