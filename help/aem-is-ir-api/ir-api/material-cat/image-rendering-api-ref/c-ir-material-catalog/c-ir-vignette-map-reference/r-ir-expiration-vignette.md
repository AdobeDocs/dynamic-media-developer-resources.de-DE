---
description: Client-Cache-Zeit zum Live-Betrieb. Anzahl der Stunden bis zum Ablauf. Wird zur Verwaltung der Zwischenspeicherung von Client- und Proxyservern verwendet.
seo-description: Client-Cache-Zeit zum Live-Betrieb. Anzahl der Stunden bis zum Ablauf. Wird zur Verwaltung der Zwischenspeicherung von Client- und Proxyservern verwendet.
seo-title: Ablauf
solution: Experience Manager
title: Ablauf
uuid: fa267728-9a36-4705-97d6-d567148fc2d7
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# Ablauf{#expiration}

Client-Cache-Zeit zum Live-Betrieb. Anzahl der Stunden bis zum Ablauf. Wird zur Verwaltung der Zwischenspeicherung von Client- und Proxyservern verwendet.

Weitere Informationen finden Sie unter ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`.

## Eigenschaften {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Real number, -2, -1, 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Generierung des Antwortbilds. Auf 0 setzen, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Zwischenspeicherung des Clients effektiv deaktiviert wird. Auf -1 setzen, um als `never expire` zu markieren; in diesem Fall gibt der Server bei bedingten `GET`-Anforderungen immer den Status 403 zurück, ohne zu prüfen, ob die Datei tatsächlich geändert wurde. Auf -2 setzen, um den Standardwert von `attribute::Expiration` zu verwenden.

## Standard {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` wird verwendet, wenn das Feld nicht vorhanden ist, wenn der Wert -2 oder wenn das Feld leer ist.

## Verwandte Themen {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
