---
description: Eigenschaften von PostScript-Dateien.
seo-description: Eigenschaften von PostScript-Dateien.
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
topic: Dynamic Media Image Production System API
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

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

