---
title: Ablauf
description: Standardmäßige Client-Cache-Zeit für die Live-Schaltung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 5%

---

# Ablauf{#expiration}

Standardmäßige Client-Cache-Zeit für die Live-Schaltung. Bietet ein standardmäßiges Ablaufintervall für den Fall, dass ein bestimmter Katalogdatensatz keine gültige `catalog::Expiration` oder `vignette::Expiration` -Wert. Oder, wenn direkt auf eine Vignettendatei oder eine Materialdatei zugegriffen wird, anstatt über einen Katalogdatensatz.

## Eigenschaften {#section-8e2bade105ec4905ae5c4911f500279f}

reale Nummer, `0` oder höher. Anzahl der Stunden bis Ablauf seit der Erstellung der Antwortdaten. Legen Sie fest auf `0` immer das Antwortbild sofort ablaufen lassen, wodurch das Client-Caching effektiv deaktiviert wird. Legen Sie fest auf `-1` zum Markieren als *niemals ablaufen*.

## Standard {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Vererbt von `default::Expiration` wenn nicht definiert oder leer ist.

## Verwandte Themen {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
