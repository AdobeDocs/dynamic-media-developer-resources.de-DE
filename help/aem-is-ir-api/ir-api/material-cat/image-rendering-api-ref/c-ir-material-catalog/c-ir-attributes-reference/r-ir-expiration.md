---
description: Standardmäßige Client-Cache-Zeit für die Live-Schaltung. Bietet ein standardmäßiges Ablaufintervall für den Fall, dass ein bestimmter Katalogdatensatz keinen gültigen Katalogablaufwert oder Vignettenablaufwert enthält oder wenn direkt auf eine Vignettendatei oder Materialdatei zugegriffen wird, anstatt über einen Katalogdatensatz.
solution: Experience Manager
title: Ablauf
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---

# Ablauf{#expiration}

Standardmäßige Client-Cache-Zeit für die Live-Schaltung. Bietet ein standardmäßiges Ablaufintervall für den Fall, dass ein bestimmter Katalogdatensatz keinen gültigen Katalog enthält::Expiration or vignette::Expiration -Wert oder wenn direkt auf eine Vignettendatei oder Materialdatei zugegriffen wird, anstatt über einen Katalogdatensatz.

## Eigenschaften {#section-8e2bade105ec4905ae5c4911f500279f}

Real number, 0 oder höher. Anzahl der Stunden bis Ablauf seit der Erstellung der Antwortdaten. Auf 0 setzen, damit das Antwortbild immer sofort abläuft, wodurch das Client-Caching effektiv deaktiviert wird. Auf -1 setzen, um als *never expire* zu markieren.

## Standard {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Vererbt von Standard::Expiration , wenn nicht definiert oder wenn leer.

## Verwandte Themen {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
