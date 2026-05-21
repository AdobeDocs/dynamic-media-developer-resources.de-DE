---
description: Bildanker. Ausgangspunkt, wenn dieses Bild als Ebene in einer Vorlage oder einem zusammengesetzten Bild verwendet wird.
solution: Experience Manager
title: Anker
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
TQID: 'https://experienceleague.adobe.com/OKTbXTF3uzVcQeLQIGIJhCukQFzdW5gZMzatSdWP7yY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 4%

---

# Anker{#anchor}

Bildanker. Ausgangspunkt, wenn dieses Bild als Ebene in einer Vorlage oder einem zusammengesetzten Bild verwendet wird.

Definiert auch den Standardmittelpunkt für die Drehung.

## Eigenschaften {#section-95740f14160744e7bc763094b8be40d8}

Zwei ganze Zahlen, durch ein Komma getrennt. Pixel-Versatz relativ zur oberen linken Ecke des Bildes mit voller Auflösung.

Von `anchor=` überschrieben (was wiederum mit `origin=` überschrieben werden kann).

## Standard {#section-ca3a4cc837d643519eff15951f2b47a1}

Der Mittelpunkt des Bildes wird verwendet, wenn dieses Feld nicht vorhanden oder leer ist und wenn es sich um einen gültigen Bilddatensatz handelt (d. h. wenn `catalog::Path` gültig ist).

## Verwandte Themen {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
