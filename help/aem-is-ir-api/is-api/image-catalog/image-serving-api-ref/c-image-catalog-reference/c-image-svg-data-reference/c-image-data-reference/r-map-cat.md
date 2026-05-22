---
description: Imagemap-Daten. Keine oder mehrere vollständige HTML <AREA>-Elemente, von vorn nach hinten sortiert.
solution: Experience Manager
title: Zuordnen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
TQID: 'https://experienceleague.adobe.com/JY0barcvbF72sTyYW4iIhjFE-8tfqtbI78PDccLcXV0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 2%

---

# Zuordnen{#map}

Imagemap-Daten. Keine oder mehrere vollständige HTML-`<AREA>`, sortiert von vorn nach hinten.

Der Server interpretiert die Attribute SHAPE und COORDS und kann sie ändern (SHAPE=CIRCLE wird in dieser Version nicht unterstützt). Alle anderen Attribute von `<AREA>` werden unverändert weitergeleitet. Mit dem COORDS-Attribut angegebene Koordinatenwerte müssen Pixel-Offsets von der linken oberen Ecke des unveränderten Quellbilds sein. (`%`-Koordinaten werden in dieser Version nicht unterstützt und können möglicherweise nicht korrekt verarbeitet werden.)

## Eigenschaften {#section-f52d89fd399b4356ac05277e6c12f956}

Text-Zeichenfolgenwert. Wenn angegeben, muss es sich um ein oder mehrere vollständige HTML-`<AREA>` handeln.

Dieses Feld ist an der Lokalisierung von Textzeichenfolgen beteiligt. Siehe [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz* für Details.

## Standard {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Keine.

## Verwandte Themen {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
