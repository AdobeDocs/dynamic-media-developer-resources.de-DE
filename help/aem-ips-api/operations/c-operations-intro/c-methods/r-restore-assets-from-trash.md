---
description: Stellt Assets aus dem Papierkorb wieder her.
seo-description: Stellt Assets aus dem Papierkorb wieder her.
seo-title: restoreAssetsFromTrash
solution: Experience Manager
title: restoreAssetsFromTrash
uuid: f7424d4c-7807-4de9-ad0c-f96364bf7b82
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 11%

---


# restoreAssetsFromTrash{#restoreassetsfromtrash}

Stellt Assets aus dem Papierkorb wieder her.

Syntax

## Autorisierte Benutzertypen {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-200a61d040c94e489a85241b29cd499a}

**Input (restoreAssetsFromTrashParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zu einer Firma mit den Assets, die Sie wiederherstellen möchten. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | Array von Handles für die Assets, die Sie wiederherstellen möchten. |

**Output (restoreAssetsFromTrashReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Anzahl der Assets, die erfolgreich aus dem Papierkorb entfernt wurden. |
| `*`warningCount`*` | `xsd:int` | Ja | Anzahl der Warnungen, die beim Versuch des Vorgangs generiert wurden, Assets aus dem Papierkorb wiederherzustellen. |
| `*`errorCount`*` | `xsd:int` | Ja | Anzahl der Fehler, die beim Versuch generiert wurden, Assets aus dem Papierkorb wiederherzustellen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Warnungen generiert haben, wenn der Vorgang versucht hat, Assets aus dem Papierkorb wiederherzustellen. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Fehler generiert haben, wenn der Vorgang versucht hat, Assets aus dem Papierkorb wiederherzustellen. |

## Beispiele {#section-98fe0394b0634ca397c395f14f8a9358}

Dieses Codebeispiel stellt Assets aus dem Papierkorb wieder her. Die Antwort zeigt an, dass der Vorgang erfolgreich abgeschlossen wurde.

**Anforderung**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**Antwort**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```

