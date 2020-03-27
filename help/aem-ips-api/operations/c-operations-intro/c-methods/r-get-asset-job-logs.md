---
description: Ruft die Auftragsprotokolle für ein Asset ab. Elemente, die im Array zurückgegeben werden, enthalten detaillierte Informationen zu jedem Eintrag im Auftragsprotokoll für dieses Asset. Das Antwortfeld logMessage wird basierend auf dem Feld authHeader lokalisiert.
seo-description: Ruft die Auftragsprotokolle für ein Asset ab. Elemente, die im Array zurückgegeben werden, enthalten detaillierte Informationen zu jedem Eintrag im Auftragsprotokoll für dieses Asset. Das Antwortfeld logMessage wird basierend auf dem Feld authHeader lokalisiert.
seo-title: getAssetJobLogs
solution: Experience Manager
title: getAssetJobLogs
topic: Scene7 Image Production System API
uuid: 7ea81baf-769b-4c73-bbc6-f52c89c98d50
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetJobLogs{#getassetjoblogs}

Ruft die Auftragsprotokolle für ein Asset ab. Elemente, die im Array zurückgegeben werden, enthalten detaillierte Informationen zu jedem Eintrag im Auftragsprotokoll für dieses Asset. Das Antwortfeld logMessage wird basierend auf dem Feld authHeader lokalisiert.

Syntax

## Autorisierte Benutzertypen {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-9586617e124b4da4acb6b66b2a9adad8}

**Input (getAssetJobLogsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, zu der das Asset gehört. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Das Handle für das Asset mit den abzurufenden Auftragsprotokollen. |

**Output (getAssetJobLogsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`jobLogArray`*` | `types:AssetJobLogArray` | Ja | Auftragsprotokollarray. |

## Beispiele {#section-f03d7f3ec5d043d38227f926fb7609f6}

Dieses Codebeispiel ruft die Auftragsprotokolle eines bestimmten Assets ab. Die Antwort gibt ein Auftragsprotokollarray mit detaillierten Informationen zu allen Aufträgen zurück, in denen das Asset verwendet wurde.

**Anforderung**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**Antwort**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```

