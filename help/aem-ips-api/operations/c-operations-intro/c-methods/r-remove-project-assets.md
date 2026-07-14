---
description: Entfernt Assets aus einem Projekt. Zerstört die Assets nicht.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
TQID: 'https://experienceleague.adobe.com/GHGyYEF5H3Me5jKtkfd15Ok8KEk2hrRuVxrKCF7cZ-E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 179
ht-degree: 10%

---

# removeProjectAssets{#removeprojectassets}

Entfernt Assets aus einem Projekt. Zerstört die Assets nicht.

Syntax

## Autorisierte Benutzertypen {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-169d8e317417415b87df86242f65710e}

**Eingabe (removeProjectAssetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das -Handle an die Firma mit den Assets, die Sie verschieben möchten. |
| projectHandle | `xsd:string` | Ja | Der Handler zu den Projekt-Assets, die Sie verschieben möchten. |
| assetHandleArray | `types:HandleArray` | Ja | Array von Griffen auf die Assets, die verschoben werden sollen. |

**Ausgabe (removeProjectAssetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Asset-Anzahl erfolgreich entfernt. |
| warningCount | `xsd:int` | Ja | Die Anzahl der Warnhinweise, die beim Versuch generiert wurden, Assets aus dem Projekt zu entfernen. |
| errorCount | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch erzeugt wurden, Assets aus dem Projekt zu entfernen. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind und Warnungen generiert haben, als der Vorgang versucht hat, sie aus dem Projekt zu entfernen. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind und Fehler generiert haben, als der Vorgang versucht hat, sie aus dem Projekt zu entfernen. |

## Beispiele {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Dieses Codebeispiel entfernt zwei Assets aus einem Projekt (angegeben durch das Projekt-Handle).

**Anfrage**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```

