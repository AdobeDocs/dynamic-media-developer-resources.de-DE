---
description: Eigenschaften von PostScript-Dateien.
seo-description: Eigenschaften von PostScript-Dateien.
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---


# GenerationInfo{#generationinfo}

Eigenschaften von PostScript-Dateien.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`Suchmaschine`*` | `xsd:string` | Verwendete Generierungsmaschine (für Werte siehe &quot;Informationen zur Generierung&quot;). |
| `*`originator`*` | `types:Asset` | Asset-Datensatz des primären Assets, das bei der Generierung verwendet wird. |
| `*`generiert`*` | `types:Asset` | Asset-Datensatz des generierten Assets. |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | Array von Attributen, die mit dem Generierungsprozess verknüpft sind. |

