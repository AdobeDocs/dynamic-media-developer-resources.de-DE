---
description: Assets in einem Projekt zuweisen oder aktualisieren
seo-description: Assets in einem Projekt zuweisen oder aktualisieren
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
topic: Scene7 Image Production System API
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 18%

---


# setProjectAssets{#setprojectassets}

Assets in einem Projekt zuweisen oder aktualisieren

Syntax

## Autorisierte Benutzertypen {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Input (setProjectAssetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`projectHandle`*` | `xsd:string` | Ja | Projekthandle. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Ja | Das Array der Asset-Handles, die Sie mit dem Projekt verknüpfen möchten. |

**Output (setProjectAssetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Die Anzahl der erfolgreich hinzugefügten Assets. |

## Beispiele {#section-33c1a909c3dc4aa98da474c23a036596}

Dieses Codebeispiel weist einem Projekt ein Asset zu. Die Anforderung gibt einen Erfolgszähler von 1 zurück.

**Anforderung**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Antwort**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

