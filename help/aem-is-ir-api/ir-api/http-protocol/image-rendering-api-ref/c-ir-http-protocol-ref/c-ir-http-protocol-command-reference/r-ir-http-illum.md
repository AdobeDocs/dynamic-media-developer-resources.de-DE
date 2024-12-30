---
title: Illum
description: Beleuchtungskartenwähler. Gibt die Beleuchtungszuordnung an, mit der dieses Material gerendert werden soll.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Illum{#illum}

Beleuchtungskartenwähler. Gibt die Beleuchtungszuordnung an, mit der dieses Material gerendert werden soll.

`illum=-1|0|1|2`

Ist die angegebene Beleuchtungskarte nicht in der Zielvignette verfügbar, wird stattdessen die nächstgelegene verfügbare Karte verwendet.

`illum=-1` Gibt an, dass die Beleuchtungszuordnung automatisch auf der Grundlage des `gloss=` ausgewählt wird.

## Eigenschaften {#section-aace8466566e4cf1a0c5a6c0167245c9}

Materialattribut. Ignoriert, wenn die Vignette nicht mehrere Beleuchtungszuordnungen definiert.

## Standard {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Verwandte Themen {#section-9132e60381c64aa3a8ed1319690db55e}

[Glanz=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
