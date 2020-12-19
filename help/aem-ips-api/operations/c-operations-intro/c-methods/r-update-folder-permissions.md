---
description: Aktualisieren Sie die Ordnerberechtigungen.
seo-description: Aktualisieren Sie die Ordnerberechtigungen.
seo-title: updateFolderPermissions
solution: Experience Manager
title: updateFolderPermissions
topic: Scene7 Image Production System API
uuid: 940d7b63-80cf-4097-9cf9-8499b69181b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 18%

---


# updateFolderPermissions{#updatefolderpermissions}

Aktualisieren Sie die Ordnerberechtigungen.

Syntax

## Autorisierte Benutzertypen {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-339e6e17c5504e1ea79fbdc05f618050}

**Input (updateFolderPermissionsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Ordner-Handle. |
| ` *`updateChildren`*` | `xsd:boolean` | Ja | Legt fest, ob untergeordnete Elemente mit für den Ordner der obersten Ebene festgelegten Berechtigungen aktualisiert werden sollen. |
| ` *`updateArray`*` | `types:PermissionUpdateArray` | Ja | Das Array der Berechtigungsaktualisierungen, die Sie auf den Ordner anwenden möchten. |

**Output (updateFolderPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-c3fe4d4388674870a3856c35ef66b631}

**Anforderung**

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
