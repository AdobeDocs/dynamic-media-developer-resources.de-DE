---
description: Gibt den Veröffentlichungsverlauf für ein Asset zurück.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '89'
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
