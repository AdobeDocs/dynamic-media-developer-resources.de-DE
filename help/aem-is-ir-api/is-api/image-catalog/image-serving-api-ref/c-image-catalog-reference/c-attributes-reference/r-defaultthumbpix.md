---
description: Standardgröße für Miniaturen. Wird anstelle des Attributs DefaultPix für Anfragen von Miniaturen verwendet (req=tmb).
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 2%

---

# DefaultThumbPix{#defaultthumbpix}

Standardgröße für Miniaturen. Wird anstelle von „attribute::DefaultPix“ für Anfragen von Miniaturen verwendet (req=tmb).

Der Server schränkt Antwortbilder dahingehend ein, dass sie nicht größer sind als diese Breite und Höhe, wenn eine Miniaturbildanforderung ( `req=tmb`) die Größe nicht explizit angibt, nicht explizit die Anzeigegröße mithilfe von `wid=`, `hei=` oder `scl=`.

## Eigenschaften {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Zwei ganze Zahlen, 0 oder höher, durch ein Komma getrennt. Breite und Höhe in Pixel. Einer oder beide Werte können auf 0 gesetzt werden, um sie nicht einzuschränken.

Gilt nicht für verschachtelte oder eingebettete Anforderungen.

## Standard {#section-2c4a4f14540449638822913513170ff1}

Von `default::DefaultThumbPix` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
