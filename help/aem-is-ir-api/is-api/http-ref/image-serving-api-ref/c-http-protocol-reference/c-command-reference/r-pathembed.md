---
description: Pfaddaten einbetten. Gibt an, ob Photoshop-Pfade aus der Quellbilddatei der Ebene 0 in das Antwortbild einbezogen werden sollen.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# pathEmbed{#pathembed}

Pfaddaten einbetten. Gibt an, ob Photoshop-Pfade aus der Quellbilddatei der Ebene 0 in das Antwortbild einbezogen werden sollen.

`pathEmbed=0|1`

## Eigenschaften {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Anforderungsattribut. Wird ignoriert, wenn das Quellbild keine Pfaddaten enthält. Die Pfaddaten werden wie die Bilddaten skaliert und gedreht. Es werden nur Pfade aus dem Quellbild von `layer=0` verarbeitet. Pfade aus anderen Ebenenbildern werden ignoriert.

Wird ignoriert, wenn das Ausgabebildformat keine Pfadeinbettung unterstützt. Eine Liste der Ausgabebildformate, die die Pfadeinbettung unterstützen, finden Sie in der Beschreibung von `fmt=`.

## Einschränkungen {#section-697cddb79a1542bc8457d2f4f59eec69}

Offene Photoshop-Pfade (Pfade, die keine geschlossenen Schleifen bilden) werden derzeit nicht zum Einbetten in das Antwortbild unterstützt.

## Standard {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, damit keine Pfade in Ausgabebilder einbettet werden.

## Verwandte Themen {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
