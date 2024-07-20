---
title: pathEmbed
description: Betten Sie Pfade mit Daten ein. Gibt an, ob Photoshop-Pfade aus der Quellbilddatei der Ebene 0 im Antwortbild enthalten sein sollen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# pathEmbed{#pathembed}

Betten Sie Pfade mit Daten ein. Gibt an, ob Photoshop-Pfade aus der Quellbilddatei der Ebene 0 im Antwortbild enthalten sein sollen.

`pathEmbed=0|1`

## Eigenschaften {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Anforderungsattribut. Wird ignoriert, wenn das Quellbild keine Pfaddaten enthält. Die Pfaddaten werden wie die Bilddaten skaliert und gedreht. Nur Pfade aus dem Quellbild von `layer=0` werden verarbeitet; Pfade aus anderen Ebenenbildern werden ignoriert.

Wird ignoriert, wenn das Ausgabebildformat keine Pfadeinbettung unterstützt. Eine Liste der Ausgabebildformate, die die Pfadeinbettung unterstützen, finden Sie in der Beschreibung von `fmt=` .

## Einschränkungen {#section-697cddb79a1542bc8457d2f4f59eec69}

Offene Photoshop-Pfade (Pfade, die keine geschlossenen Schleifen bilden) werden derzeit nicht zum Einbetten in das Antwortbild unterstützt.

## Standard {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, um keine Pfade in Ausgabebilder einzubetten.

## Verwandte Themen {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
