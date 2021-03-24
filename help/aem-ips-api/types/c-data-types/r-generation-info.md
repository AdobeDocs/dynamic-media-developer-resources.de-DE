---
description: Eigenschaften von PostScript-Dateien.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

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

