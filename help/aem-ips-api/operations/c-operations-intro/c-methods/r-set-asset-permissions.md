---
description: Legt die Berechtigungen für ein einzelnes Asset mithilfe eines Berechtigungs-Assets fest.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
TQID: 'https://experienceleague.adobe.com/dd96ai2DgoCqZ1NR-2rixSHDEaBSgk6ioQIqmG-1RoE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 8%

---

# setAssetPermissions{#setassetpermissions}

Legt die Berechtigungen für ein einzelnes Asset mithilfe eines Berechtigungs-Assets fest.

Assets übernimmt standardmäßig die Berechtigungen des übergeordneten Ordners. Nachdem Sie Berechtigungen für ein Asset festgelegt haben, erbt es die Berechtigungen des übergeordneten Assets nicht mehr, es sei denn, Sie rufen `removeAssetPermissions` auf.

## Autorisierte Benutzertypen {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-e05abbce6453450fb38747101cb5e228}

**Eingabe (setAssetPermissionsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das -Handle an das Unternehmen, das den Ordner enthält, mit dem Sie arbeiten möchten. |
| assetHandle | `xsd:string` | Ja | Ordner-Handle |
| permissionArray | `types:PermissionsUpdateArray` | Ja | Berechtigungs-Array |

**Ausgabe (setAssetPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-38955bc330bb4909b6b06027ef2b143e}

Dieses Codebeispiel legt Berechtigungen für ein Asset fest. Sie enthält das Unternehmens- und Asset-Handle sowie ein Berechtigungs-Array.

**Anfrage**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**Antwort**

Keine.
