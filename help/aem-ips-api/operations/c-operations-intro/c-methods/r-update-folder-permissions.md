---
description: Aktualisieren von Ordnerberechtigungen.
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 16%

---

# updateFolderPermissions{#updatefolderpermissions}

Aktualisieren von Ordnerberechtigungen.

Syntax

## Autorisierte Benutzertypen {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-339e6e17c5504e1ea79fbdc05f618050}

**Input (updateFolderPermissionsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Firmengriff. |
| folderHandle | `xsd:string` | Ja | Ordner-Handle |
| updateChildren | `xsd:boolean` | Ja | Legt fest, ob untergeordnete Elemente mit Berechtigungen aktualisiert werden, die für den Ordner der obersten Ebene festgelegt sind. |
| updateArray | `types:PermissionUpdateArray` | Ja | Das Array von Berechtigungsaktualisierungen, die Sie auf den Ordner anwenden möchten. |

**Ausgabe (updateFolderPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-c3fe4d4388674870a3856c35ef66b631}

**Anfrage**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**Antwort**

Keine.
