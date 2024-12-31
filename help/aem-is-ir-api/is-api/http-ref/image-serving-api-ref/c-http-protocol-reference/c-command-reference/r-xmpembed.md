---
title: xmpEmbed
description: XMP-Metadaten einbetten. Gibt an, ob XMP-Metadaten in das Antwortbild aufgenommen werden sollen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

XMP-Metadaten einbetten. Gibt an, ob XMP-Metadaten in das Antwortbild aufgenommen werden sollen.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP-Daten werden ohne Änderung vom Quellbild an das Antwortbild übergeben. Dies kann dazu führen, dass falsche Daten in das Antwortbild eingebettet werden.

## Eigenschaften {#section-27024c4272f44d9a8c264a0629193af2}

Anforderungsattribut. Ignoriert, wenn das Quellbild keine XMP-Daten enthält. Es werden nur XMP-Daten aus dem Quellbild von `layer=0` verarbeitet. XMP-Daten aus anderen Ebenenbildern werden ignoriert.

Wird ignoriert, wenn das Ausgabebildformat keine XMP-Einbettung unterstützt. Unter der Beschreibung von `fmt=` finden Sie eine Liste der Ausgabebildformate, die die XMP-Einbettung unterstützen.

## Standard {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, für keine Einbettung von Pfaden in die Ausgabebilder.

## Verwandte Themen {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
