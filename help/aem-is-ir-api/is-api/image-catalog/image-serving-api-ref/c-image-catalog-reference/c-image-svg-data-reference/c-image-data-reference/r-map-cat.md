---
description: Imagemap-Daten. Keine oder mehr vollständige HTML <AREA>-Elemente, von vorne nach hinten sortiert.
seo-description: Imagemap-Daten. Keine oder mehr vollständige HTML <AREA>-Elemente, von vorne nach hinten sortiert.
seo-title: Map
solution: Experience Manager
title: Map
topic: Scene7 Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 5%

---


# Map{#map}

Imagemap-Daten. Keine oder mehr vollständige HTML `<AREA>`-Elemente, sortiert von vorne nach hinten.

Der Server interpretiert die Attribute SHAPE und COORDS und kann sie ändern. (SHAPE=CIRCLE wird in dieser Version nicht unterstützt.) Alle anderen Attribute von `<AREA>` werden ohne Änderung übergeben. Koordinatenwerte, die mit dem COORDS-Attribut angegeben werden, müssen Pixelversatz von der oberen linken Ecke des nicht geänderten Quellbilds sein. (`%`-Koordinaten werden in dieser Version nicht unterstützt und werden möglicherweise nicht korrekt verarbeitet.)

## Eigenschaften {#section-f52d89fd399b4356ac05277e6c12f956}

Textzeichenfolgenwert. Wenn angegeben, muss es sich um ein oder mehrere vollständige HTML `<AREA>`-Elemente handeln.

Dieses Feld nimmt an der lokale Anpassung der Textzeichenfolge teil. Weitere Informationen finden Sie unter [Textzeichenfolgen-Lokale Anpassung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz*.

## Standard {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Keine.

## Verwandte Themen {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md),  [Textzeichenfolgen-Lokale Anpassung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
