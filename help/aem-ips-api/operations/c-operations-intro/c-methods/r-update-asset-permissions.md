---
description: Aktualisiert Asset-Berechtigungen.
solution: Experience Manager
title: updateAssetPermissons
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 12972a52-7b70-405c-9c73-e5ce6ab7dd9b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 20%

---

# updateAssetPermissons{#updateassetpermissons}

Aktualisiert Asset-Berechtigungen.

Syntax

## Autorisierte Benutzertypen {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-392cb3076cf84790a32fd913f2b111a3}

**Input (updateAssetPermissionsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle des Unternehmens. |
| assetHandle | `xsd:string` | Ja | Asset-Handle. |
| updateArray | `types:PermissionUpdateArray` | Ja | Berechtigungen, die Sie auf das Asset anwenden möchten. |

**Ausgabe (updateAssetPermissionsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**Anfrage**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**Antwort**

Keine.
