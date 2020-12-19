---
description: Stamm-URL für relative Bild-URLs. Gibt die Stamm-URL für relative Bild-URLs an.
seo-description: Stamm-URL für relative Bild-URLs. Gibt die Stamm-URL für relative Bild-URLs an.
seo-title: RootUrl
solution: Experience Manager
title: RootUrl
topic: Scene7 Image Serving - Image Rendering API
uuid: 173ce99a-f87e-4700-a28a-1a87b8c55b85
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# RootUrl{#rooturl}

Stamm-URL für relative Bild-URLs. Gibt die Stamm-URL für relative Bild-URLs an.

`attribute::RootUrl` wird verwendet, anstatt  `attribute::RootPath` wenn ein  `src=` oder ein  `mask=` Wert durch {geschweifte Klammern} oder (Klammern) eingeschlossen ist.

## Eigenschaften {#section-fe02269b4b724319a5d1f2cfcae31cba}

Textzeichenfolgenwert. Absoluter URL-Stammpfad, einschließlich der führenden Protokollkennung. Die folgenden Protokolle werden unterstützt: HTTP, HTTPS und FTP.

## Standard {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Vererbt von `default::RootUrl`, wenn nicht definiert. Wenn definiert, aber leer, werden relative URLs von diesem Bildkatalog nicht unterstützt.

## Verwandte Themen {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [ruleSet::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
