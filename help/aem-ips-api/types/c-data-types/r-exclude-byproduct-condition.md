---
description: Bestimmt, welche Generierungsmaschine und welcher generierte Asset-Typ aus den Suchergebnissen ausgeschlossen werden sollen.
solution: Experience Manager
title: ExcludeByproductCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5b37e01b-9e9c-4d34-9d39-1f9bfe356e53
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 10%

---

# ExcludeByproductCondition{#excludebyproductcondition}

Bestimmt, welche Generierungsmaschine und welcher generierte Asset-Typ aus den Suchergebnissen ausgeschlossen werden sollen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| Suchmaschine | `xsd:string` | Die Generierungs-Engine, die Assets erstellt hat, die Sie ausschließen möchten. Werte finden Sie unter Generierungsinformationen . |
| generatedAssetType | `xsd:string` | Ausgeschlossener Asset-Typ. Werte finden Sie unter Asset-Typen . |
