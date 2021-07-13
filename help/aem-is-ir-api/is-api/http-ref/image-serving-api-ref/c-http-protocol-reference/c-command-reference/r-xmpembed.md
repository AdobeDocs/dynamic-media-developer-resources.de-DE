---
description: Betten Sie XMP Metadaten ein. Gibt an, ob XMP Metadaten im Antwortbild enthalten sein sollen.
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# xmpEmbed{#xmpembed}

Betten Sie XMP Metadaten ein. Gibt an, ob XMP Metadaten im Antwortbild enthalten sein sollen.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP Daten werden vom Quellbild ohne Änderung an das Antwortbild übergeben. Dies kann dazu führen, dass falsche Daten in das Antwortbild eingebettet werden.

## Eigenschaften {#section-27024c4272f44d9a8c264a0629193af2}

Anforderungsattribut. Wird ignoriert, wenn das Quellbild keine XMP Daten enthält. Nur XMP Daten aus dem Quellbild von `layer=0` werden verarbeitet. XMP Daten aus anderen Ebenenbildern werden ignoriert.

Wird ignoriert, wenn das Ausgabebildformat das Einbetten XMP nicht unterstützt. Eine Liste der Ausgabebildformate, die XMP Einbetten unterstützen, finden Sie in der Beschreibung von `fmt=` .

## Standard {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, damit keine Pfade in Ausgabebilder eingebettet werden.

## Verwandte Themen {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
