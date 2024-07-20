---
description: Eigenschaften der Ebenenansicht.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 13%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Eigenschaften der Ebenenansicht.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| url | `xsd:string` | Bildserver-URL, die die Vorlage darstellt. Kombiniert die Felder `urlModifier` und `urlPostAp- plyModifier` . |
| urlModifier | `xsd:string` | Image Serving-Protokollbefehle, die vor der Anfrage angewendet werden, oder `urlPostApplyModifier`-Befehle. |
| urlPostApplyModifier | `xsd:string` | Image Serving-Protokollbefehle, die nach `urlModifier` angewendet werden und Befehle anfordern. |
