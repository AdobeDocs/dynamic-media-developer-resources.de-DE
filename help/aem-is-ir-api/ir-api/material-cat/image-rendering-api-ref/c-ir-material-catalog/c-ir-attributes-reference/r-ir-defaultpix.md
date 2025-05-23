---
title: DefaultPix
description: Standardgröße des Render-Bildes. Der Server schränkt Antwortbilder dahingehend ein, dass sie nicht größer sind als diese Breite und Höhe, wenn die Anfrage die Anzeigegröße nicht explizit mithilfe von wid= oder hei= angibt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# DefaultPix{#defaultpix}

Standardgröße des Render-Bildes. Der Server schränkt Antwortbilder dahingehend ein, dass sie nicht größer sind als diese Breite und Höhe, wenn die Anfrage die Anzeigegröße nicht explizit mithilfe von wid= oder hei= angibt.

## Eigenschaften {#section-9dc5474fc75842308796ab6440b29611}

Zwei ganze Zahlen, 0 oder höher, durch ein Komma getrennt. Breite und Höhe in Pixel. Einer oder beide Werte können auf 0 gesetzt werden, um sie nicht einzuschränken.

Gilt nicht für verschachtelte oder eingebettete Anforderungen.

## Standard {#section-1935781c561e4679aa87a5bcced8df90}

Von `default::DefaultPix` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
