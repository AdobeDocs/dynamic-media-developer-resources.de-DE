---
description: Eigenschaften der Ansicht der Ebene.
seo-description: Eigenschaften der Ansicht der Ebene.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Scene7 Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 11%

---


# LayerViewInfo{#layerviewinfo}

Eigenschaften der Ansicht der Ebene.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`url`*` | `xsd:string` | Image-Server-URL, die die Vorlage darstellt. Kombiniert die Felder `urlModifier` und `urlPostAp- plyModifier`. |
| ` *`urlModifier`*` | `xsd:string` | Image Serving-Protokollbefehle, die vor der Anforderung oder den Befehlen `urlPostApplyModifier` angewendet werden sollen. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Image Serving-Protokollbefehle, die nach `urlModifier` angewendet werden, und Anforderungsbefehle. |

