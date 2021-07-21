---
description: Eigenschaften der Ebenenansicht.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 11%

---

# LayerViewInfo{#layerviewinfo}

Eigenschaften der Ebenenansicht.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`url`*` | `xsd:string` | Bildserver-URL, die die Vorlage darstellt. Kombiniert die Felder `urlModifier` und `urlPostAp- plyModifier` . |
| `*`urlModifier`*` | `xsd:string` | Image Serving-Protokollbefehle, die vor der Anfrage angewendet werden, oder `urlPostApplyModifier`-Befehle. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Image Serving-Protokollbefehle, die nach `urlModifier` angewendet werden und Befehle anfordern. |
