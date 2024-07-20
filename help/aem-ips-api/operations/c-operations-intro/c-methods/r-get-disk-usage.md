---
description: Gibt Informationen zur Struktur eines Unternehmens (Anzahl Dateien usw.) zurück.
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 11%

---

# getDiskUsage{#getdiskusage}

Gibt Informationen zur Struktur eines Unternehmens (Anzahl Dateien usw.) zurück.

## Autorisierte Benutzertypen {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen, dessen Festplattenauslastung Sie abrufen möchten. |

**Ausgabe (getDiskUsageReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| diskUsageArray | `types:DiskUsageArray` | Ja | Array der Unternehmensdatenträger. |

## Beispiele {#section-cb16a97badc94076ad5da277db5ed16a}

Der Name dieser Anfrage ist irreführend. Statt lediglich einen Skalarwert zurückzugeben, der angibt, wie viel Festplattenspeicher ein Unternehmen verwendet, erhält es auch andere Informationen über die Struktur eines Unternehmens.

**Anfrage**

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
