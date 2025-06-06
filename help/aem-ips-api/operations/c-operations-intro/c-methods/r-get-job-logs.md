---
description: Ruft die angegebenen Vorgangslogs für das ausgewählte Unternehmen ab. Sie können nach Zeichen, Richtung, Start- und Enddatum und Anzahl der Zeilen sortieren.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 10%

---

# getJobLogs{#getjoblogs}

Ruft die angegebenen Vorgangslogs für das ausgewählte Unternehmen ab. Sie können nach Zeichen, Richtung, Start- und Enddatum und Anzahl der Zeilen sortieren.

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

**Eingabe (getJobLogsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Nein | Die Firma kümmert sich um. |
| userHandle | `xsd:string` | Nein | Ruft Protokolle für Aufträge ab, die von einem bestimmten Benutzer gesendet werden. |
| sortBy | `xsd:string` | Nein | Hier können Sie die Sortierfelder auswählen. |
| sortDirection | `xsd:string` | Nein | Sortierreihenfolge (aufsteigend oder absteigend). |
| startDate | `xsd:dateTime` | Nein | Datum und Uhrzeit des Starts des Vorgangslogs. Geben Sie die Zeitzone mit der Anfrage für dieses Feld an. |
| endDate | `xsd:dateTime` | Nein | Datum und Uhrzeit des Endes des Vorgangslogs. Geben Sie die Zeitzone mit der Anfrage für dieses Feld an. |
| numRows | `xsd:int` | Nein | Maximale Anzahl an zurückzugebenden Zeilen |

**Ausgabe (getJobLogsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | Ja | Array von Vorgangslogs. |

## Beispiele {#section-35871c94b4a44559912577efddbc46a6}

Dieses Code-Beispiel gibt IPS-Auftragsprotokolle für ein bestimmtes Unternehmen zurück. Sie können damit auch Vorgangslogs für einen bestimmten Benutzer oder eine bestimmte Firma und einen bestimmten Benutzer zurückgeben.

**Anfrage**

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
