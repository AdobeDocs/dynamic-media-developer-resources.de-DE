---
description: Legt die Berechtigungen für ein einzelnes Asset mithilfe eines Berechtigungs-Assets fest.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
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
