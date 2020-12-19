---
description: Entfernt Assets aus einem Projekt. Zerstört die Assets nicht.
seo-description: Entfernt Assets aus einem Projekt. Zerstört die Assets nicht.
seo-title: removeProjectAssets
solution: Experience Manager
title: removeProjectAssets
topic: Scene7 Image Production System API
uuid: bae09dc3-4328-4264-8fb2-e4f0c53546eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '189'
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

**Input (removeProjectAssetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit den Assets, die Sie verschieben möchten. |
| ` *`projectHandle`*` | `xsd:string` | Ja | Das Handle zu den zu verschiebenden Projekt-Assets. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Ja | Array von Handles zu den Assets, die Sie verschieben möchten. |

**Output (removeProjectAssetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Asset-Anzahl erfolgreich entfernt. |
| ` *`warningCount`*` | `xsd:int` | Ja | Die Anzahl der Warnungen, die beim Versuch des Vorgangs generiert wurden, Assets aus dem Projekt zu entfernen. |
| ` *`errorCount`*` | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, Assets aus dem Projekt zu entfernen. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Warnungen generiert haben, wenn der Vorgang versuchte, sie aus dem Projekt zu entfernen. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Fehler generiert haben, wenn der Vorgang versuchte, sie aus dem Projekt zu entfernen. |

## Beispiele {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Mit diesem Codebeispiel werden zwei Assets aus einem Projekt entfernt (vom Projekthandle angegeben).

**Anforderung**

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

