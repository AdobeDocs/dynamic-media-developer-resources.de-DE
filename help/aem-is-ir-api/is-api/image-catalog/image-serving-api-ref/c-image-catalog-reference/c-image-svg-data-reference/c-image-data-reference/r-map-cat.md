---
description: Imagemap-Daten. Keine oder mehrere vollständige HTML <AREA>-Elemente, von vorne nach hinten sortiert.
solution: Experience Manager
title: Map
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---

# Zuordnung{#map}

Imagemap-Daten. Keine oder mehrere vollständige HTML `<AREA>`-Elemente, von vorne nach hinten sortiert.

Der Server interpretiert die Attribute SHAPE und COORDS und kann sie ändern. (SHAPE=CIRCLE wird in dieser Version nicht unterstützt.) Alle anderen Attribute von `<AREA>` werden ohne Änderung übergeben. Die mit dem COORDS-Attribut angegebenen Koordinatenwerte müssen Pixelabweichungen aus der linken oberen Ecke des unveränderten Quellbilds sein. (`%` Koordinaten werden in dieser Version nicht unterstützt und werden möglicherweise nicht korrekt verarbeitet.)

## Eigenschaften {#section-f52d89fd399b4356ac05277e6c12f956}

Textzeichenfolgenwert. Wenn angegeben, muss es sich um ein oder mehrere vollständige HTML `<AREA>`-Elemente handeln.

Dieses Feld nimmt an der Lokalisierung von Textzeichenfolgen teil. Weitere Informationen finden Sie unter [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz* .

## Standard {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Keine.

## Verwandte Themen {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md),  [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
