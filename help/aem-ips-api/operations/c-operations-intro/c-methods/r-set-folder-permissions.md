---
description: Legt die Ordnerberechtigungen fest.
seo-description: Legt die Ordnerberechtigungen fest.
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
topic: Scene7 Image Production System API
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 14%

---


# setFolderPermissions{#setfolderpermissions}

Legt die Ordnerberechtigungen fest.

Syntax

## Autorisierte Benutzertypen {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-2a41135054954396b40f1228f2e63b42}

**Input (setFolderPermissionsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Ordner-Handle. |
| ` *`setChildren`*` | `xsd:boolean` | Ja | Legt Berechtigungen für untergeordnete Elemente fest, die dem Ordner gehören. |
| ` *`permissionArray`*` | `types:PermissionUpdateArray` | Ja | Berechtigungsarray. |

**Output (setFolderPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-01730da4be874553ab44e3241cdf6357}

In diesem Codebeispiel werden ein Firmen-Handle, ein Ordnerhandle und ein Berechtigungsarray mit detaillierten Informationen zum Ordner angegeben. Es werden dieselben Berechtigungen für die untergeordneten Elemente des übergeordneten Ordners angewendet.

**Anforderung**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**Antwort**

Keine.
