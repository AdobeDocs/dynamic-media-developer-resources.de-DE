---
description: Bild-Anker. Ausgangspunkt, wenn dieses Bild als Ebene in einer Vorlage oder einem zusammengesetzten Bild verwendet wird.
solution: Experience Manager
title: Anker
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# Anker{#anchor}

Bild-Anker. Ausgangspunkt, wenn dieses Bild als Ebene in einer Vorlage oder einem zusammengesetzten Bild verwendet wird.

Definiert auch den standardmäßigen Mittelpunkt für die Drehung.

## Eigenschaften {#section-95740f14160744e7bc763094b8be40d8}

Zwei Ganzzahlen, durch Kommas getrennt. Pixel-Versatz relativ zur oberen linken Ecke des Vollbildbilds.

Überschrieben durch `anchor=` (was wiederum mit `origin=` überschrieben werden kann).

## Standard {#section-ca3a4cc837d643519eff15951f2b47a1}

Der Mittelpunkt des Bildes wird verwendet, wenn dieses Feld nicht vorhanden oder leer ist und es ein gültiger Bilddatensatz ist (d. h. wenn `catalog::Path` gültig ist).

## Verwandte Themen {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
