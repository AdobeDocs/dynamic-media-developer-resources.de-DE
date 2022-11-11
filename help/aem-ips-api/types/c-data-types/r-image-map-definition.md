---
description: Zieldefinition für eine Klickaktion im Browser.
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

Zieldefinition für eine Klickaktion im Browser.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| name | `xsd:string` | Der Name der Imagemap-Definition. |
| shapeType | `xsd:string` | Einer der Regionsformwerte. |
| Region | `xsd:string` | Imagemap-Koordinaten. Das Format basiert auf der HTML `<area>` Tag-Attribute. |
| Aktion | `xsd:string` | Andere Attribute, die in die HTML aufgenommen werden sollen `<area>` -Tag, einschließlich `href` URL. |
| aktiviert | `xsd:boolean` | True , wenn die Imagemap aktiviert ist. |
