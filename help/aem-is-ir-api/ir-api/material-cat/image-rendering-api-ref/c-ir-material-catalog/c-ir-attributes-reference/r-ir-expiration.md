---
description: Standardmäßige Clientcache-Zeit bis zum Live-Betrieb. Bietet ein Standardablaufintervall, wenn ein bestimmter Katalogeintrag keinen gültigen Wert für den Ablauf oder Ablauf eines Katalogs enthält oder wenn direkt auf eine Vignettendatei oder eine Materialdatei zugegriffen wird, anstatt über einen Katalogeintrag.
seo-description: Standardmäßige Clientcache-Zeit bis zum Live-Betrieb. Bietet ein Standardablaufintervall, wenn ein bestimmter Katalogeintrag keinen gültigen Wert für den Ablauf oder Ablauf eines Katalogs enthält oder wenn direkt auf eine Vignettendatei oder eine Materialdatei zugegriffen wird, anstatt über einen Katalogeintrag.
seo-title: Ablauf
solution: Experience Manager
title: Ablauf
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2b56f9ec-2b25-4e6a-aead-6dad3d2df975
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---


# Ablauf{#expiration}

Standardmäßige Clientcache-Zeit bis zum Live-Betrieb. Bietet ein Standardablaufintervall, wenn ein bestimmter Katalogeintrag keinen gültigen Katalog enthält::Expiration or vignette::Expiration value oder wenn direkt auf eine Vignettendatei oder eine Materialdatei zugegriffen wird, anstatt über einen Katalogeintrag.

## Eigenschaften {#section-8e2bade105ec4905ae5c4911f500279f}

Reale Zahl, 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Generierung der Antwortdaten. Auf 0 setzen, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Zwischenspeicherung des Clients effektiv deaktiviert wird. Auf -1 setzen, um als *nie ablaufen* zu markieren.

## Standard {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Von Standard übernommen::Ablauf, wenn nicht definiert oder leer.

## Verwandte Themen {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[Katalog::Ablauf](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [Vignette::Ablauf](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
