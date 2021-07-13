---
description: Einbetten von Pfaddaten. Gibt an, ob Photoshop-Pfade aus der Quellbilddatei der Ebene 0 im Antwortbild enthalten sein sollen.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# pathEmbed{#pathembed}

Einbetten von Pfaddaten. Gibt an, ob Photoshop-Pfade aus der Quellbilddatei der Ebene 0 im Antwortbild enthalten sein sollen.

`pathEmbed=0|1`

## Eigenschaften {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Anforderungsattribut. Wird ignoriert, wenn das Quellbild keine Pfaddaten enthält. Die Pfaddaten werden wie die Bilddaten skaliert und gedreht. Es werden nur Pfade aus dem Quellbild von `layer=0` verarbeitet. Pfade von anderen Ebenenbildern werden ignoriert.

Wird ignoriert, wenn das Ausgabebildformat keine Pfadeinbettung unterstützt. Eine Liste der Ausgabebildformate, die die Pfadeinbettung unterstützen, finden Sie in der Beschreibung von `fmt=` .

## Einschränkungen {#section-697cddb79a1542bc8457d2f4f59eec69}

Offene Photoshop-Pfade (Pfade, die keine geschlossenen Schleifen bilden) werden derzeit nicht zum Einbetten in das Antwortbild unterstützt.

## Standard {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, damit keine Pfade in Ausgabebilder eingebettet werden.

## Verwandte Themen {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
