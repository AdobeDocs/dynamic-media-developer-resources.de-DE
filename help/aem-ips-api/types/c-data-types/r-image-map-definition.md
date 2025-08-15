---
description: Zieldefinition für eine Klick-Aktion im Browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

Zieldefinition für eine Klick-Aktion im Browser.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| name | `xsd:string` | Der Name der Imagemap-Definition. |
| formType | `xsd:string` | Einer der Bereichsformwerte. |
| Region | `xsd:string` | Imagemap-Koordinaten. Das Format basiert auf den `<area>`-Tag-Attributen von HTML. |
| Aktion | `xsd:string` | Andere Attribute, die in das HTML-`<area>`-Tag aufgenommen werden sollen, einschließlich der `href`-URL. |
| aktiviert | `xsd:boolean` | True, wenn die Imagemap aktiviert ist. |
