---
description: Imagemap-Daten. Keine oder mehr vollständige HTML <AREA>-Elemente, sortiert von vorn nach hinten.
solution: Experience Manager
title: Zuordnen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# Zuordnen{#map}

Imagemap-Daten. Keine oder mehrere vollständige HTML-`<AREA>`, sortiert von vorn nach hinten.

Der Server interpretiert die Attribute SHAPE und COORDS und kann sie ändern (SHAPE=CIRCLE wird in dieser Version nicht unterstützt). Alle anderen Attribute von `<AREA>` werden unverändert weitergeleitet. Mit dem COORDS-Attribut angegebene Koordinatenwerte müssen Pixel-Offsets von der linken oberen Ecke des unveränderten Quellbilds sein. (`%`-Koordinaten werden in dieser Version nicht unterstützt und können möglicherweise nicht korrekt verarbeitet werden.)

## Eigenschaften {#section-f52d89fd399b4356ac05277e6c12f956}

Text-Zeichenfolgenwert. Falls angegeben, muss es sich um ein oder mehrere vollständige HTML-`<AREA>` handeln.

Dieses Feld ist an der Lokalisierung von Textzeichenfolgen beteiligt. Siehe [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz* für Details.

## Standard {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Keine.

## Verwandte Themen {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
