---
title: pathEmbed
description: Einbetten von Datenpfaden. Gibt an, ob Photoshop-Pfade aus der Quellbilddatei der Ebene 0 in das Antwortbild aufgenommen werden sollen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
TQID: 'https://experienceleague.adobe.com/ES7nAoYjO6Y4naU2c5TIPotPUTjncwjRMLL7-4--XpE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 2%

---

# pathEmbed{#pathembed}

Einbetten von Datenpfaden. Gibt an, ob Photoshop-Pfade aus der Quellbilddatei der Ebene 0 in das Antwortbild aufgenommen werden sollen.

`pathEmbed=0|1`

## Eigenschaften {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Anforderungsattribut. Ignoriert, wenn das Quellbild keine Datenpfade enthält. Die Pfade werden wie die Bilddaten skaliert und gedreht. Nur Pfade aus dem Quellbild von `layer=0` werden verarbeitet. Pfade aus anderen Ebenenbildern werden ignoriert.

Wird ignoriert, wenn das Ausgabebildformat das Einbetten von Pfaden nicht unterstützt. Unter der Beschreibung von `fmt=` finden Sie eine Liste der Ausgabebildformate, die die Pfadeinbettung unterstützen.

## Einschränkungen {#section-697cddb79a1542bc8457d2f4f59eec69}

Offene Photoshop-Pfade (Pfade, die keine geschlossenen Schleifen bilden) werden derzeit nicht für das Einbetten in das Antwortbild unterstützt.

## Standard {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, für keine Einbettung von Pfaden in die Ausgabebilder.

## Verwandte Themen {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
