---
description: Gibt den Veröffentlichungsverlauf für ein Asset zurück.
seo-description: Gibt den Veröffentlichungsverlauf für ein Asset zurück.
seo-title: getAssetPublishHistory
solution: Experience Manager
title: getAssetPublishHistory
uuid: 15025c3d-eac3-4cb8-9a2a-fd80bd67478f
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
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

**Input (getAssetPublishHistoryParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle für die Firma mit dem Asset-Veröffentlichungsverlauf. |
| `*`assetHandle`*` | `xsd:string` | Ja | Das Asset mit dem Veröffentlichungsverlauf, den Sie untersuchen möchten. |

**Output (getAssetPublishHistoryReturn)**

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

