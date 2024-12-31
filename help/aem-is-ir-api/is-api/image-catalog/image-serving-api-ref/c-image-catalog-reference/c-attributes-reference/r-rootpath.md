---
description: Stammverzeichnis der Source-Daten. Absoluter oder relativer Pfad für den Stammordner für die Quelldaten dieses Bildkatalogs.
solution: Experience Manager
title: rootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# rootPath{#rootpath}

Stammverzeichnis der Source-Daten. Absoluter oder relativer Pfad für den Stammordner für die Quelldaten dieses Bildkatalogs.

Der `RootPath` ist ein Text-Zeichenfolgenwert. Weitere [ zu Serverstammpfaden finden ](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) unter „Verwalten von Source-&quot;.

## Eigenschaften {#section-b41d7e0ea63143eb8034569706cad0c0}

Text-String Muss leer sein, ein gültiger relativer Ordnerpfad oder ein gültiger absoluter Pfad, auf den der Bildserver zugreifen kann.

## Standard {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Von `default::RootPath` geerbt, wenn nicht definiert. Wenn er definiert, aber leer ist, trägt er nicht zum Stammverzeichnis der Quelldatei bei.

## Verwandte Themen {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Verwalten von Source-Daten](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
