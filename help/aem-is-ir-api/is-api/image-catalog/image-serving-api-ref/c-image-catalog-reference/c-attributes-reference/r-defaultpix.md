---
description: Standardgröße der Ansicht.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# DefaultPix{#defaultpix}

Standardgröße der Ansicht.

Der Server schränkt die Größe von Antwortbildern auf diese Breite und Höhe ein, wenn in der Anforderung nicht explizit die Größe der Ansicht mit `wid=`, `hei=` oder `scl=` angegeben wird.

## Eigenschaften {#section-c3e658cf82c540d986b118f74f0fe1b2}

Zwei ganzzahlige Zahlen, 0 oder größer, durch Kommas getrennt. Breite und Höhe in Pixel. Einer oder beide Werte können auf 0 gesetzt werden, damit sie nicht eingeschränkt werden.

Gilt nicht für verschachtelte/eingebettete Anforderungen.

## Standard {#section-b7338b2bf5114fff83b0714a57b20639}

Vererbt von `default::DefaultPix`, wenn nicht definiert oder leer.

## Verwandte Themen {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [Katalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
