---
description: Fügt einem Projekt ein oder mehrere Assets hinzu.
seo-description: Fügt einem Projekt ein oder mehrere Assets hinzu.
seo-title: addProjectAssets
solution: Experience Manager
title: addProjectAssets
topic: Scene7 Image Production System API
uuid: 48abea17-058e-4469-bb16-0abee8ef5214
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 11%

---


# addProjectAssets{#addprojectassets}

Fügt einem Projekt ein oder mehrere Assets hinzu.

Syntax

## Autorisierte Benutzertypen {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-20d498e971b6466298e60c8a77fc32b2}

**Input (addProjectAssetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Behandeln Sie die mit dem aktuellen Projekt verknüpfte Firma. |
| ` *`projectHandle`*` | `xsd:string` | Ja | Bearbeiten Sie das Projekt, dem Sie Assets hinzufügen. |
| ` *`projectHandleArray`*` | `xsd:HandleArray` | Ja | Array von Assets, die Sie dem aktuellen Projekt hinzufügen. |

**Output (addProjectAssetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Die Anzahl der erfolgreich hinzugefügten Assets. |
| ` *`warningCount`*` | `xsd:int` | Ja | Die Anzahl der Warnungen, die beim Versuch des Vorgangs generiert wurden, Assets zu einem Projekt hinzuzufügen. |
| ` *`errorCount`*` | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, Assets zu einem Projekt hinzuzufügen. |
| ` *`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | Nein | Array von Warnungen, die von Assets generiert wurden, wenn der Vorgang versuchte, sie einem Projekt hinzuzufügen. |
| ` *`companyHandle`*` | `xsd:AssetOperationFaultArray` | Nein | Array von Fehlern, die von Assets generiert wurden, wenn der Vorgang versuchte, sie einem Projekt hinzuzufügen. |

## Beispiele {#section-bee5be2402f54cb9a3a02cc07def4135}

In diesem Beispiel wird einem in der Anforderung angegebenen Projekt in einem Asset-Handle-Array ein einzelnes Asset (durch dessen Handle referenziert) hinzugefügt. Der Vorgang wurde erfolgreich abgeschlossen, wenn die Antwort `successCount` `1` zurückgibt.

**Anforderung**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Antwort**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

