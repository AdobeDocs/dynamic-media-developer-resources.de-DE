---
title: illum
description: Beleuchtungszuordnungsauswahl. Gibt die Beleuchtungskarte an, mit der dieses Material gerendert werden soll.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# illum{#illum}

Beleuchtungszuordnungsauswahl. Gibt die Beleuchtungskarte an, mit der dieses Material gerendert werden soll.

`illum=-1|0|1|2`

Wenn die angegebene Beleuchtungskarte in der Zielvignette nicht verfügbar ist, wird stattdessen die nächstverfügbare Karte verwendet.

`illum=-1` Gibt an, dass die Beleuchtungskarte automatisch auf der Grundlage der `gloss=` -Wert.

## Eigenschaften {#section-aace8466566e4cf1a0c5a6c0167245c9}

Materialattribut. Wird ignoriert, wenn die Vignette nicht mehrere Beleuchtungskarten definiert.

## Standard {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Verwandte Themen {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
