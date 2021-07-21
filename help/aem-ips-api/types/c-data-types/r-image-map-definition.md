---
description: Zieldefinition für eine Klickaktion im Browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 11%

---

# ImageMapDefinition{#imagemapdefinition}

Zieldefinition für eine Klickaktion im Browser.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`name`*` | `xsd:string` | Der Name der Imagemap-Definition. |
| `*`shapeType`*` | `xsd:string` | Einer der Regionsformwerte. |
| `*`Region`*` | `xsd:string` | Imagemap-Koordinaten. Das Format basiert auf den HTML-Tag-Attributen `<area>` . |
| `*`Aktion`*` | `xsd:string` | Andere Attribute, die in das HTML-Tag `<area>` aufgenommen werden sollen, einschließlich der URL `href` . |
| `*`aktiviert`*` | `xsd:boolean` | True , wenn die Imagemap aktiviert ist. |
