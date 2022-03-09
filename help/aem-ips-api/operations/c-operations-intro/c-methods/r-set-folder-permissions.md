---
description: Legt die Ordnerberechtigungen fest.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 15%

---

# setFolderPermissions{#setfolderpermissions}

Legt die Ordnerberechtigungen fest.

Syntax

## Autorisierte Benutzertypen {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-2a41135054954396b40f1228f2e63b42}

**Eingabe (setFolderPermissionsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle des Unternehmens. |
| folderHandle | `xsd:string` | Ja | Ordner-Handle. |
| setChildren | `xsd:boolean` | Ja | Legt Berechtigungen für untergeordnete Elemente fest, die zum Ordner gehören. |
| permissionArray | `types:PermissionUpdateArray` | Ja | Berechtigungs-Array. |

**Ausgabe (setFolderPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-01730da4be874553ab44e3241cdf6357}

In diesem Codebeispiel werden ein Unternehmens-Handle, ein Ordner-Handle und ein Berechtigungs-Array mit detaillierten Informationen zum Ordner angegeben. Sie wendet dieselben Berechtigungen für die untergeordneten Elemente des übergeordneten Ordners an.

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
