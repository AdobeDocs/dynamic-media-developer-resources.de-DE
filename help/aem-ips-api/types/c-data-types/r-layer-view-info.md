---
description: Eigenschaften der Ansicht der Ebene.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 11%

---


# LayerViewInfo{#layerviewinfo}

Eigenschaften der Ansicht der Ebene.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`url`*` | `xsd:string` | Image-Server-URL, die die Vorlage darstellt. Kombiniert die Felder `urlModifier` und `urlPostAp- plyModifier`. |
| `*`urlModifier`*` | `xsd:string` | Image Serving-Protokollbefehle, die vor der Anforderung oder den Befehlen `urlPostApplyModifier` angewendet werden sollen. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Image Serving-Protokollbefehle, die nach `urlModifier` angewendet werden, und Anforderungsbefehle. |

