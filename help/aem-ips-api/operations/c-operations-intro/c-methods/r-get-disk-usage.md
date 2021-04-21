---
description: Gibt Informationen zur Dateistruktur einer Firma (Anzahl der Dateien usw.) zurück.
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 13%

---


# getDiskUsage{#getdiskusage}

Gibt Informationen zur Dateistruktur einer Firma (Anzahl der Dateien usw.) zurück.

## Autorisierte Benutzertypen {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, deren Speichernutzung Sie abrufen möchten. |

**Output (getDiskUsageReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | Ja | Array der verwendeten Firma. |

## Beispiele {#section-cb16a97badc94076ad5da277db5ed16a}

Der Name dieser Anforderung ist irreführend. Statt lediglich einen Skalarwert zurückzugeben, der den von einer Firma belegten Speicherplatz widerspiegelt, werden auch andere Informationen über die Struktur einer Firma abgerufen.

**Anforderung**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**Antwort**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```

