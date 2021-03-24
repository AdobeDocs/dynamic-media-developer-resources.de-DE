---
description: Legt die Berechtigungen eines einzelnen Assets mithilfe eines Berechtigungsassets fest.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# setAssetPermissions{#setassetpermissions}

Legt die Berechtigungen eines einzelnen Assets mithilfe eines Berechtigungsassets fest.

Assets erben standardmäßig die Berechtigungen ihres übergeordneten Ordners. Nachdem Sie Berechtigungen für ein Asset festgelegt haben, erbt es nicht mehr die Berechtigungen des übergeordneten Elements, es sei denn, Sie rufen `removeAssetPermissions` auf.

## Autorisierte Benutzertypen {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-e05abbce6453450fb38747101cb5e228}

**Input (setAssetPermissonsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, die den Ordner enthält, mit dem Sie arbeiten möchten. |
| `*`assetHandle`*` | `xsd:string` | Ja | Ordner-Handle. |
| `*`permissionArray`*` | `types:PermissionsUpdateArray` | Ja | Berechtigungsarray. |

**Output (setAssetPermisonsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-38955bc330bb4909b6b06027ef2b143e}

In diesem Codebeispiel werden Berechtigungen für ein Asset festgelegt. Es enthält die Firma und den Asset-Handle sowie ein Berechtigungsarray.

**Anforderung**

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
