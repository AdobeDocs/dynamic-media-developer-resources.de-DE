---
description: Löscht ein Asset.
seo-description: Löscht ein Asset.
seo-title: deleteAsset
solution: Experience Manager
title: deleteAsset
uuid: 47f700e0-04bf-4d33-a18a-d938f7e9e326
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---


# deleteAsset{#deleteasset}

Löscht ein Asset.

Syntax

## Autorisierte Benutzertypen {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss über Lese- und Löschzugriff auf das Asset verfügen.

## Parameter {#section-0eed164e278b456fbdfb7a50727a0416}

**Eingabe (deleteAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, zu der der Ordner gehört. |
| `*`assetHandle`*` | `xsd:string` | Ja | Das Handle des zu löschenden Assets. |

**Output (deleteAssetParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-d5657289f5234bb0a613dcf691507958}

Dieser Beispielcode löscht alle Asset-Typen aus einer bestimmten Firma. Es ist ein Asset-Handle erforderlich, das Sie von einem anderen Vorgang abrufen müssen.

**Anforderung**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Antwort**

Keine.
