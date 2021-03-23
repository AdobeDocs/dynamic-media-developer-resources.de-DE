---
description: Eigenschaften der Ansicht der Ebene.
seo-description: Eigenschaften der Ansicht der Ebene.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 10%

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

