---
description: Bestimmt, welche Generierungsmaschine und welcher generierte Asset-Typ aus den Suchergebnissen ausgeschlossen werden sollen.
solution: Experience Manager
title: ExcludeByproductCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5b37e01b-9e9c-4d34-9d39-1f9bfe356e53
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# [!DNL ExcludeByproductCondition]{#excludebyproductcondition}

Bestimmt, welche Generierungsmaschine und welcher generierte Asset-Typ aus den Suchergebnissen ausgeschlossen werden sollen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| [!DNL engine] | `xsd:string` | Die Generierungs-Engine, die Assets erstellt hat, die Sie ausschließen möchten. Werte finden Sie unter Generierungsinformationen . |
| generatedAssetType | `xsd:string` | Ausgeschlossener Asset-Typ. Werte finden Sie unter Asset-Typen . |
