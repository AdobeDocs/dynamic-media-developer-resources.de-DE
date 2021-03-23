---
description: Lichtbildauswahl. Gibt die Beleuchtungskarte an, mit der dieses Material gerendert werden soll.
seo-description: Lichtbildauswahl. Gibt die Beleuchtungskarte an, mit der dieses Material gerendert werden soll.
seo-title: illum
solution: Experience Manager
title: illum
uuid: 16c7144f-7f16-47d1-8140-fd679e702660
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# illum{#illum}

Lichtbildauswahl. Gibt die Beleuchtungskarte an, mit der dieses Material gerendert werden soll.

`illum=-1|0|1|2`

Wenn die angegebene Beleuchtungskarte in der Vignette &quot;Zielgruppe&quot;nicht verfügbar ist, wird stattdessen die nächste verfügbare Karte verwendet.

`illum=-1` gibt an, dass die Beleuchtungszuordnung automatisch anhand des  `gloss=` Wertes ausgewählt wird.

## Eigenschaften {#section-aace8466566e4cf1a0c5a6c0167245c9}

Materialattribut. Wird ignoriert, wenn die Vignette keine mehrfachen Lichtkarten definiert.

## Standard {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Verwandte Themen {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
