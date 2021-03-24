---
description: Auflösung von Miniaturbildern. Gibt die Objektauflösung für das Miniaturbild an.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---


# ThumbRes{#thumbres}

Auflösung von Miniaturbildern. Gibt die Objektauflösung für das Miniaturbild an.

Wird nur verwendet, wenn `catalog::ThumbType=3`.

## Eigenschaften {#section-ee5cae086a3d4875805fa8a08756a586}

Wert der tatsächlichen Zahl größer als 0. Muss die gleichen Einheiten wie `catalog::Resolution` haben.

## Standard {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` wird verwendet, wenn das Feld nicht vorhanden ist, wenn der Wert 0 ist oder wenn das Feld leer ist.

## Verwandte Themen {#section-eb716bf647614db083020fe8ce453751}

[Katalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [Katalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1),  [Attribut::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [Miniaturansicht](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
