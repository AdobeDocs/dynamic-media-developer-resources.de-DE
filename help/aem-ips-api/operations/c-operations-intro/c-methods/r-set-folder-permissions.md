---
description: Legt die Ordnerberechtigungen fest.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
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
| `*`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| `*`folderHandle`*` | `xsd:string` | Ja | Ordner-Handle. |
| `*`setChildren`*` | `xsd:boolean` | Ja | Legt Berechtigungen für untergeordnete Elemente fest, die dem Ordner gehören. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` | Ja | Berechtigungsarray. |

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
