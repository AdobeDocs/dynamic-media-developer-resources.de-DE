---
description: Dateieigenschaften von PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

Dateieigenschaften von PostScript.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| [!DNL engine] | `xsd:string` | Verwendete Generierungs-Engine (Werte finden Sie unter &quot;Generierungsinformationen&quot;). |
| [!DNL originator] | `types:Asset` | Asset-Datensatz des bei der Generierung verwendeten primären Assets. |
| [!DNL generated] | `types:Asset` | Asset-Datensatz des generierten Assets. |
| attributeArray | `types:GenerationAttributeArray` | Array von Attributen, die mit dem Generierungsprozess verknüpft sind. |
