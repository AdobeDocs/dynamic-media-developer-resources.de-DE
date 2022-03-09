---
description: PostScript-Dateieigenschaften.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 14%

---

# GenerationInfo{#generationinfo}

PostScript-Dateieigenschaften.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| Suchmaschine | `xsd:string` | Verwendete Generierungs-Engine (Werte finden Sie unter &quot;Generierungsinformationen&quot;). |
| originator | `types:Asset` | Asset-Datensatz des bei der Generierung verwendeten primären Assets. |
| generiert | `types:Asset` | Asset-Datensatz des generierten Assets. |
| attributeArray | `types:GenerationAttributeArray` | Array von Attributen, die mit dem Generierungsprozess verknüpft sind. |
