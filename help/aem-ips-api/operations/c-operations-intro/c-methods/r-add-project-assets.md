---
description: Fügt einem Projekt mindestens ein Asset hinzu.
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 10%

---

# addProjectAssets{#addprojectassets}

Fügt einem Projekt mindestens ein Asset hinzu.

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
| companyHandle | `xsd:string` | Ja | Verarbeiten Sie das mit dem aktuellen Projekt verknüpfte Unternehmen. |
| projectHandle | `xsd:string` | Ja | Handle mit dem Projekt, dem Sie Assets hinzufügen. |
| projectHandleArray | `xsd:HandleArray` | Ja | Array von Assets, die Sie zum aktuellen Projekt hinzufügen. |

**Output (addProjectAssetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Die Anzahl der erfolgreich hinzugefügten Assets. |
| warningCount | `xsd:int` | Ja | Die Anzahl der Warnungen, die generiert wurden, wenn der Vorgang versuchte, einem Projekt Assets hinzuzufügen. |
| errorCount | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch generiert wurden, einem Projekt Assets hinzuzufügen. |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | Nein | Array von Warnungen, die von Assets generiert wurden, wenn der Vorgang versuchte, sie einem Projekt hinzuzufügen. |
| companyHandle | `xsd:AssetOperationFaultArray` | Nein | Array von Fehlern, die von Assets generiert wurden, wenn der Vorgang versuchte, sie einem Projekt hinzuzufügen. |

## Beispiele {#section-bee5be2402f54cb9a3a02cc07def4135}

In diesem Beispiel wird einem in der Anfrage angegebenen Projekt ein einzelnes Asset (referenziert durch sein Handle) in einem Asset-Handle-Array hinzugefügt. Der Vorgang wurde erfolgreich abgeschlossen, wenn die Antwort `successCount` `1` zurückgibt.

**Anfrage**

```java {.line-numbers}
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Antwort**

```java {.line-numbers}
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```
