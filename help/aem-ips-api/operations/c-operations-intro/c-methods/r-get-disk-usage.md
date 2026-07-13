---
description: Gibt Informationen zur Struktur eines Unternehmens zurück (Anzahl der Dateien usw.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
TQID: 'https://experienceleague.adobe.com/mF0YHIw8BZhBRK240EmiiaHoyBbTdaW-ajl7veY1ywk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 11%

---

# getDiskUsage{#getdiskusage}

Gibt Informationen zur Struktur eines Unternehmens zurück (Anzahl der Dateien usw.).

## Autorisierte Benutzertypen {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, dessen Festplattenauslastung Sie abrufen möchten. |

**Ausgabe (getDiskUsageReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| diskUsageArray | `types:DiskUsageArray` | Ja | Array der verwendeten Unternehmensfestplatten. |

## Beispiele {#section-cb16a97badc94076ad5da277db5ed16a}

Der Name dieser Anfrage ist irreführend. Anstatt nur einen Skalarwert zurückzugeben, der angibt, wie viel Festplattenspeicher ein Unternehmen verwendet, erhält es auch andere Informationen über die Struktur eines Unternehmens.

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

