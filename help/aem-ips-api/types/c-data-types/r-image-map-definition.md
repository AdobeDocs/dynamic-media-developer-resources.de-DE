---
description: Zielgruppe für eine Klickaktion im Browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 11%

---


# ImageMapDefinition{#imagemapdefinition}

Zielgruppe für eine Klickaktion im Browser.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`name`*` | `xsd:string` | Der Name der Imagemap-Definition. |
| `*`shapeType`*` | `xsd:string` | Einer der Regionsformwerte. |
| `*`Region`*` | `xsd:string` | Imagemap-Koordinaten. Das Format basiert auf den HTML `<area>`-Tag-Attributen. |
| `*`Aktion`*` | `xsd:string` | Andere Attribute, die in das HTML `<area>`-Tag eingeschlossen werden sollen, einschließlich der `href`-URL. |
| `*`aktiviert`*` | `xsd:boolean` | True, wenn die Imagemap aktiviert ist. |

