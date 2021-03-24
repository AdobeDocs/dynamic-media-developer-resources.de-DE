---
description: Katalog-ID. Das HTTP-Pfadelement, mit dem dieser Katalog in der Vignette-, Material- oder ICC-Profil-Objektspezifikation in HTTP-Anforderungen identifiziert werden soll.
solution: Experience Manager
title: RootId
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---


# RootId{#rootid}

Katalog-ID. Das HTTP-Pfadelement, mit dem dieser Katalog in der Vignette-, Material- oder ICC-Profil-Objektspezifikation in HTTP-Anforderungen identifiziert werden soll.

## Eigenschaften {#section-c33266223d5b47029df756caa4e0df0c}

Textzeichenfolgenwert. Kann alle Zeichen enthalten, die in HTTP-Pfaden gültig sind.

## Standard {#section-e0ed902557684345850b86672b5dbe5b}

Keine. Jeder Katalog muss einen eindeutigen `catalog::RootId`-Wert haben. default.ini hat normalerweise ein leeres `catalog::RootId`.

## Verwandte Themen {#section-4670832574f54f9080bb485b047efd5b}

[Katalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85) ,  [Vignette::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-id-vignette.md#reference-2a7ba758924b4757b3234942304db7fd),  [profile::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-macro-definition-reference/r-ir-name.md#reference-63b663d2052545ffab030a23e7060b1e),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
