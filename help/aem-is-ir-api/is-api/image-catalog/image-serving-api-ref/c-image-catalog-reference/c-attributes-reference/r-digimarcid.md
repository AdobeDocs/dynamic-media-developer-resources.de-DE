---
description: Digimarc-Benutzerinformationen. Gibt die Benutzerinformationen für die Digimarc-Einbettung an.
seo-description: Digimarc-Benutzerinformationen. Gibt die Benutzerinformationen für die Digimarc-Einbettung an.
seo-title: DigimarcId
solution: Experience Manager
title: DigimarcId
topic: Scene7 Image Serving - Image Rendering API
uuid: 23f1952f-71b7-4b2a-917d-8161ea855ac9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 3%

---


# DigimarcId{#digimarcid}

Digimarc-Benutzerinformationen. Gibt die Benutzerinformationen für die Digimarc-Einbettung an.

## Eigenschaften {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Fünf oder sechs kommagetrennte Ganzzahlen. Die dritte und vierte Zahl werden nicht mehr verwendet:

`creator-id, creator-pin, durability [ , chroma ]`

Die Variablen `creator-id` und `creator-pin` werden von Digimarc bereitgestellt, wenn der Dienst erworben wird. Die nicht verwendeten Werte sollten leer bleiben.

`durability` gibt die Einbettungsstärke des Digimarc-Wasserzeichens an. Es kann 1, 2, 3 oder 4 sein, wobei 1 die schwächste und 4 die stärkste Haltbarkeit angibt.

Setzen Sie `chroma` auf 1, um das Wasserzeichen in die Chrominanzdaten des Bildes zu kodieren, oder auf 0 (Standard), um es in die Luminanz zu kodieren. Diese Einstellung wird ignoriert, wenn Graustufenbilder ausgegeben werden.

## Standard {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Vererbt von `default::DigimarcId`, wenn nicht definiert oder leer.

## Beispiel {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Geben Sie eine Digimarc-Ersteller-ID mit einer Haltbarkeit von 4 an.

`DigimarcId= 404407,32,,,4`

## Verwandte Themen {#section-75d4d2afd1df4127b31b1a82f30079d8}

[Katalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
