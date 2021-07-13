---
description: Quelldaten-Stammpfad. Absoluter oder relativer Pfad für den Stammordner für die Quelldaten dieses Bildkatalogs.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# RootPath{#rootpath}

Quelldaten-Stammpfad. Absoluter oder relativer Pfad für den Stammordner für die Quelldaten dieses Bildkatalogs.

`RootPath` ist ein Textstring-Wert. Weitere Informationen zu Serverstammpfaden finden Sie unter [Verwalten von Quelldaten](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) .

## Eigenschaften {#section-b41d7e0ea63143eb8034569706cad0c0}

Textzeichenfolge. Muss leer oder ein gültiger relativer Ordnerpfad oder ein gültiger absoluter Pfad sein, auf den der Image-Server zugreifen kann.

## Standard {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Vererbt von `default::RootPath` , falls nicht definiert. Wenn definiert, aber leer, trägt nicht zum Stammverzeichnis der Quelldatei bei.

## Verwandte Themen {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),   [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [Verwalten von Quelldaten](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
