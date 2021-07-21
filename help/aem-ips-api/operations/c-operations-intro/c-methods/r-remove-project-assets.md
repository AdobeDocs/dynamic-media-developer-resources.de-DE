---
description: Entfernt Assets aus einem Projekt. Löscht die Assets nicht.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 10%

---

# removeProjectAssets{#removeprojectassets}

Entfernt Assets aus einem Projekt. Löscht die Assets nicht.

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
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle für das Unternehmen mit den Assets, die Sie verschieben möchten. |
| `*`projectHandle`*` | `xsd:string` | Ja | Der Handle für die Projekt-Assets, die Sie verschieben möchten. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | Array von Handles zu den Assets, die Sie verschieben möchten. |

**Ausgabe (removeProjectAssetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Asset-Anzahl wurde erfolgreich entfernt. |
| `*`warningCount`*` | `xsd:int` | Ja | Die Anzahl der Warnungen, die generiert wurden, wenn der Vorgang versucht hat, Assets aus dem Projekt zu entfernen. |
| `*`errorCount`*` | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch generiert wurden, Assets aus dem Projekt zu entfernen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Warnungen generiert haben, wenn der Vorgang versucht hat, sie aus dem Projekt zu entfernen. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Fehler generiert haben, wenn der Vorgang versucht hat, sie aus dem Projekt zu entfernen. |

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
