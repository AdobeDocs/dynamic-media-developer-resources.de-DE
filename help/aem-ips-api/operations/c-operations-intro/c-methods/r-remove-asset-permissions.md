---
description: Entfernt Berechtigungen aus ausgewählten Assets.
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 14%

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
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen. |
| assetHandle | `xsd:string` | Ja | Der Handle für das Asset mit Berechtigungen, die Sie entfernen möchten. |

**Output (removeAssetPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-238fa7bb091548f5ba72ced11fc92d4f}

In diesem Codebeispiel werden Berechtigungen aus einem Asset entfernt.

**Anfrage**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Antwort**

Keine.
