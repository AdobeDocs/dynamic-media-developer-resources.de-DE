---
description: Digimarc-Benutzerinformationen. Gibt die Benutzerinformationen für die Digimarc-Einbettung an.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Digimarc-Benutzerinformationen. Gibt die Benutzerinformationen für die Digimarc-Einbettung an.

## Eigenschaften {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Fünf oder sechs kommagetrennte Ganzzahlen. Die dritte und vierte Zahl werden nicht mehr verwendet:

`creator-id, creator-pin, durability [ , chroma ]`

Die `creator-id` und `creator-pin` werden von Digimarc bereitgestellt, wenn der Service erworben wird. Die nicht verwendeten Werte sollten leer gelassen werden.

`durability` gibt die Einbettungsstärke des Digimarc-Wasserzeichens an. Es kann 1, 2, 3 oder 4 sein, wobei 1 auf die schwächste und 4 auf die höchste Dauerhaftigkeit zeigt.

Setzen Sie `chroma` auf 1, um das Wasserzeichen in die Chrominanz-Daten des Bildes zu kodieren, oder auf 0 (Standard), um es in die Luminanz zu kodieren. Diese Einstellung wird bei der Ausgabe von Graustufenbildern ignoriert.

## Standard {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Wird von `default::DigimarcId` übernommen, wenn nicht definiert oder leer.

## Beispiel {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Geben Sie eine Test-Digimarc-Ersteller-ID mit einer Dauerhaftigkeit von 4 an.

`DigimarcId= 404407,32,,,4`

## Verwandte Themen {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog: DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
