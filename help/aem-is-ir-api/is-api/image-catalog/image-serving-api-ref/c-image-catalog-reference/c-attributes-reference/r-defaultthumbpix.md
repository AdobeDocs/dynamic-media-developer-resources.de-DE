---
description: Standardgröße für Miniaturansichten. Wird anstelle des Attributs DefaultPix für Miniaturansichtsanforderungen (req=tmb) verwendet.
seo-description: Standardgröße für Miniaturansichten. Wird anstelle des Attributs DefaultPix für Miniaturansichtsanforderungen (req=tmb) verwendet.
seo-title: DefaultThumbPix
solution: Experience Manager
title: DefaultThumbPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b310aab-6d38-45f3-a3e7-b074a8e7a795
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultThumbPix{#defaultthumbpix}

Standardgröße für Miniaturansichten. Wird anstelle von attribute verwendet::DefaultPix für Miniaturansichtsanforderungen (req=tmb).

Der Server schränkt die Größe von Antwortbildern auf diese Breite und Höhe ein, wenn in einer Miniaturansicht-Anforderung ( `req=tmb`) nicht explizit angegeben ist, welche Ansicht nicht explizit mit `wid=`, `hei=`oder `scl=`angegeben wird.

## Eigenschaften {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Zwei ganzzahlige Zahlen, 0 oder größer, durch Kommas getrennt. Breite und Höhe in Pixel. Einer oder beide Werte können auf 0 gesetzt werden, damit sie nicht eingeschränkt werden.

Gilt nicht für verschachtelte/eingebettete Anforderungen.

## Standard {#section-2c4a4f14540449638822913513170ff1}

Vererbt von, `default::DefaultThumbPix` wenn nicht definiert oder leer.

## Verwandte Themen {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
