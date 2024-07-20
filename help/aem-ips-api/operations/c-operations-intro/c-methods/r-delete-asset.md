---
description: Löscht ein Asset.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 10%

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

**Input (deleteAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle des Unternehmens, zu dem der Ordner gehört. |
| assetHandle | `xsd:string` | Ja | Das Handle für das zu löschende Asset. |

**Output (deleteAssetParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-d5657289f5234bb0a613dcf691507958}

Mit diesem Beispielcode werden alle Asset-Typen aus einem bestimmten Unternehmen gelöscht. Dazu ist ein Asset-Handle erforderlich, das Sie von einem anderen Vorgang abrufen müssen.

**Anfrage**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Antwort**

Keine.
