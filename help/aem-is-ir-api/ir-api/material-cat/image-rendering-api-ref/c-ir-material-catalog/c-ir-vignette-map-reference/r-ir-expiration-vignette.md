---
description: Client-Cache-Lebensdauer. Anzahl der Stunden bis zum Ablauf. Wird für die Verwaltung der Zwischenspeicherung von Client- und Proxy-Servern verwendet.
solution: Experience Manager
title: Ablauf
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 3%

---

# Ablauf{#expiration}

Client-Cache-Lebensdauer. Anzahl der Stunden bis zum Ablauf. Wird für die Verwaltung der Zwischenspeicherung von Client- und Proxy-Servern verwendet.

Weitere Informationen [ Sie unter ](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md):Expiration.

## Eigenschaften {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Reelle Zahl, -2, -1, 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Erstellung des Antwortbildes. Auf 0 gesetzt, um das Antwortbild immer sofort ablaufen zu lassen, wodurch das Client-Caching effektiv deaktiviert wird. Auf -1 gesetzt, um als `never expire` zu markieren; in diesem Fall gibt der Server als Antwort auf bedingte `GET` immer den Status 403 zurück, ohne zu überprüfen, ob die Datei tatsächlich geändert wurde. Legen Sie dies auf -2 fest, um den von `attribute::Expiration` bereitgestellten Standardwert zu verwenden.

## Standard {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` wird verwendet, wenn das Feld nicht vorhanden ist, der Wert -2 ist oder das Feld leer ist.

## Verwandte Themen {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
