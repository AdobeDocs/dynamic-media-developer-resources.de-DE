---
description: Gibt den Veröffentlichungsverlauf für ein Asset zurück.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
TQID: 'https://experienceleague.adobe.com/fXYa2SsttVpR9a1bebJ1oouyK8peSZ5GdgldPqU9s1g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 15%

---

# getAssetPublishHistory{#getassetpublishhistory}

Gibt den Veröffentlichungsverlauf für ein Asset zurück.

Syntax

## Autorisierte Benutzertypen {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-3541bd9914a44b89acfc1d419b560ee6}

**Eingabe (getAssetPublishHistoryParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen mit dem Veröffentlichungsverlauf für Assets. |
| assetHandle | `xsd:string` | Ja | Das Asset mit dem Veröffentlichungsverlauf, den Sie untersuchen möchten. |

**Ausgabe (getAssetPublishHistoryReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| pubHistoryArray | `types:PublishHistoryArray` | Ja | Der Veröffentlichungsverlauf des Assets. |

## Beispiele {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Dieses Code-Beispiel gibt den Veröffentlichungsverlauf eines Assets zurück. Ein Asset wurde noch nie veröffentlicht, wenn der Server ein leeres Array zurückgibt.

**Anfrage**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**Antwort**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```
