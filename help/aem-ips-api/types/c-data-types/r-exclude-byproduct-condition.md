---
description: Bestimmt, welche Generation-Engine und welcher generierte Asset-Typ von den Suchergebnissen ausgeschlossen werden soll.
solution: Experience Manager
title: ExcludeByproductCondition
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 9%

---


# ExcludeByproductCondition{#excludebyproductcondition}

Bestimmt, welche Generation-Engine und welcher generierte Asset-Typ von den Suchergebnissen ausgeschlossen werden soll.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`Suchmaschine`*` | `xsd:string` | Die Generation-Engine, die Assets erstellt hat, die Sie ausschließen möchten. Werte finden Sie unter Generierungsinformationen. |
| `*`generateAssetType`*` | `xsd:string` | Ausgeschlossener Asset-Typ. Werte finden Sie unter Asset-Typen. |

