---
description: Betten Sie XMP Metadaten ein. Gibt an, ob XMP Metadaten im Antwortbild enthalten sein sollen.
seo-description: Betten Sie XMP Metadaten ein. Gibt an, ob XMP Metadaten im Antwortbild enthalten sein sollen.
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---


# xmpEmbed{#xmpembed}

Betten Sie XMP Metadaten ein. Gibt an, ob XMP Metadaten im Antwortbild enthalten sein sollen.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP Daten werden ohne Änderung vom Quellbild an das Antwortbild übergeben. Dies kann dazu führen, dass falsche Daten in das Antwortbild eingebettet werden.

## Eigenschaften {#section-27024c4272f44d9a8c264a0629193af2}

Anforderungsattribut. Wird ignoriert, wenn das Quellbild keine XMP Daten enthält. Nur XMP Daten aus dem Quellbild von `layer=0` werden verarbeitet. XMP Daten aus anderen Ebenenbildern werden ignoriert.

Wird ignoriert, wenn das Bildformat der Ausgabe XMP Einbettung nicht unterstützt. Eine Liste der Ausgabebildformate, die XMP Einbettung unterstützen, finden Sie in der Beschreibung von `fmt=`.

## Standard {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, damit keine Pfade in Ausgabebilder einbettet werden.

## Verwandte Themen {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
