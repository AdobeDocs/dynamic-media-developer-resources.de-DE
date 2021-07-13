---
description: Client-Cache-Zeit bis zur Live-Schaltung. Anzahl der Stunden bis zum Ablauf. Dient zum Verwalten der Zwischenspeicherung von Client- und Proxyservern.
solution: Experience Manager
title: Ablauf
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# Ablauf{#expiration}

Client-Cache-Zeit bis zur Live-Schaltung. Anzahl der Stunden bis zum Ablauf. Dient zum Verwalten der Zwischenspeicherung von Client- und Proxyservern.

Weitere Informationen finden Sie unter ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` .

## Eigenschaften {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Real number, -2, -1, 0 oder höher. Anzahl der Stunden bis Ablauf seit der Erstellung des Antwortbilds. Auf 0 setzen, damit das Antwortbild immer sofort abläuft, wodurch das Client-Caching effektiv deaktiviert wird. Auf -1 setzen, um als `never expire` zu markieren; In diesem Fall gibt der Server immer den Status 403 als Antwort auf bedingte `GET` -Anfragen zurück, ohne zu überprüfen, ob die Datei tatsächlich geändert wurde. Setzen Sie diese Einstellung auf -2, um den von `attribute::Expiration` bereitgestellten Standard zu verwenden.

## Standard {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` wird verwendet, wenn das Feld nicht vorhanden ist, wenn der Wert -2 ist oder wenn das Feld leer ist.

## Verwandte Themen {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
