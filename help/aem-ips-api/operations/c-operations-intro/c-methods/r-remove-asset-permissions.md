---
description: Entfernt Berechtigungen aus ausgewählten Assets.
seo-description: Entfernt Berechtigungen aus ausgewählten Assets.
seo-title: removeAssetPermissions
solution: Experience Manager
title: removeAssetPermissions
topic: Scene7 Image Production System API
uuid: 5a351862-f412-4d89-90b7-9e70a26eacbc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeAssetPermissions{#removeassetpermissions}

Entfernt Berechtigungen aus ausgewählten Assets.

Syntax

## Autorisierte Benutzertypen {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**Input (removeAssetPermissionsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Das Handle für das Asset mit den Berechtigungen, die Sie entfernen möchten. |

**Output (removeAssetPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-238fa7bb091548f5ba72ced11fc92d4f}

In diesem Codebeispiel werden Berechtigungen aus einem Asset entfernt.

**Anforderung**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Antwort**

Keine.
