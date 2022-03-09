---
description: Zuweisen oder Aktualisieren von Assets in einem Projekt.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 20%

---

# setProjectAssets{#setprojectassets}

Zuweisen oder Aktualisieren von Assets in einem Projekt.

Syntax

## Autorisierte Benutzertypen {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Eingabe (setProjectAssetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyName | `xsd:string` | Ja | Handle des Unternehmens. |
| projectHandle | `xsd:string` | Ja | Projekthandle. |
| assetHandleArray | `types:HandleArray` | Ja | Das Array der Asset-Handles, die Sie mit dem Projekt verknüpfen möchten. |

**Ausgabe (setProjectAssetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Die Anzahl der erfolgreich hinzugefügten Assets. |

## Beispiele {#section-33c1a909c3dc4aa98da474c23a036596}

In diesem Codebeispiel wird einem Projekt ein Asset zugewiesen. Die Anfrage gibt eine Erfolgsanzahl von 1 zurück.

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
