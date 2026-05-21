---
description: Hält einen aktiven Auftrag an.
solution: Experience Manager
title: Auftrag anhalten
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
TQID: 'https://experienceleague.adobe.com/7zMJW9fm8DiAPrO5cCDl87FhFMbgpw5NxoBHmIfEBog'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 16%

---

# Auftrag anhalten{#pausejob}

Hält einen aktiven Auftrag an.

Syntax

## Autorisierte Benutzertypen {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Eingabe (pauseJobParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Übernehmen Sie die Firma. |
| jobHandle | `xsd:string` | Ja | Verarbeiten Sie den Vorgang, den Sie anhalten möchten. |

**Ausgabe (PauseJobReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-ee4914f9496f4bd88556728a48fb22c1}

Dieses Code-Beispiel setzt einen aktiven Auftrag aus.

**Anfrage**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Antwort**

Keine.
