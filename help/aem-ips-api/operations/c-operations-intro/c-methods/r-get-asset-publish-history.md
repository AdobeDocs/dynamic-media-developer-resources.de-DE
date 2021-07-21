---
description: Gibt den Veröffentlichungsverlauf für ein Asset zurück.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 16%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle für das Unternehmen mit dem Asset-Veröffentlichungsverlauf. |
| `*`assetHandle`*` | `xsd:string` | Ja | Das Asset mit dem Veröffentlichungsverlauf, den Sie untersuchen möchten. |

**Ausgabe (getAssetPublishHistoryReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | Ja | Der Veröffentlichungsverlauf des Assets. |

## Beispiele {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Dieses Codebeispiel gibt den Veröffentlichungsverlauf eines Assets zurück. Ein Asset wurde nie veröffentlicht, wenn der Server ein leeres Array zurückgibt.

**Anforderung**

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
