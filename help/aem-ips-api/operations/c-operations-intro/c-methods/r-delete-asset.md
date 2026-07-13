---
description: Löscht ein Asset.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
TQID: 'https://experienceleague.adobe.com/aZnVNkDpTGXy7OrqVts-KHyOB-gdsA8XYlICQ-JC6aM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 92
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
>Der Benutzer muss Lese- und Löschzugriff auf das Asset haben.

## Parameter {#section-0eed164e278b456fbdfb7a50727a0416}

**Eingabe (deleteAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle des Unternehmens, zu dem der Ordner gehört. |
| assetHandle | `xsd:string` | Ja | Das Handle zum zu löschenden Asset. |

**Ausgabe (deleteAssetParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-d5657289f5234bb0a613dcf691507958}

Dieser Beispiel-Code löscht alle Arten von Assets aus einer bestimmten Firma. Dazu ist ein Asset-Handle erforderlich, das Sie von einem anderen Vorgang erhalten müssen.

**Anfrage**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Antwort**

Keine.

