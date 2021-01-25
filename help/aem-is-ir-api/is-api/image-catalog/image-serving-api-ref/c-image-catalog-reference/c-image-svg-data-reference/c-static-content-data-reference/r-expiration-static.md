---
description: Ablauf
solution: Experience Manager
title: Ablauf
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a727bbfc-940b-4d65-96d6-b2159b70bac1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%

---


# Ablauf{#expiration}

Wird zur Verwaltung der Zwischenspeicherung von Client- und Proxyservern verwendet. Der Server berechnet die Ablaufzeit/das Datum der HTTP-Antwortdaten, indem er diesen Wert zum Datum/Datum der Übertragung hinzufügt.

Browser verwalten Caches mit Ablaufzeiten von Dateien. Bevor eine Anforderung an den Server übergeben wird, prüft der Browser den Cache, ob die Datei bereits heruntergeladen wurde. Wenn dies der Fall ist und die Datei noch nicht abgelaufen ist, sendet der Browser anstelle einer normalen GET eine bedingte GET (z. B. mit dem im Anforderungsheader festgelegten Feld &quot;If-Modified-Since&quot;). Der Server hat die Möglichkeit, mit dem Status &#39;304&#39; zu antworten und das Bild nicht zu senden. Der Browser lädt die Datei dann aus dem Cache. Dies kann die Gesamtleistung für häufig aufgerufene Daten deutlich erhöhen.

Für diese Antworttypen wird Ablauf verwendet:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Bestimmte Arten von Antworten (z. B. Fehlerantworten) werden immer für einen sofortigen Ablauf markiert (oder als nicht-speicherbar markiert), während andere (z. B. Eigenschaften- oder Standard-Bildantworten) spezielle Ablaufeinstellungen ( `attribute::NonImgExpiration` und `attribute::DefaultExpiration`) verwenden.

## Eigenschaften {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Real number, -2, -1 oder 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Generierung des Antwortbilds. Auf 0 setzen, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Zwischenspeicherung des Clients effektiv deaktiviert wird. Auf -1 setzen, um als *`never expire`* zu markieren. In diesem Fall gibt der Server bei Anforderung von bedingten GET immer den Status 304 (nicht modifiziert) zurück, ohne zu prüfen, ob die Datei tatsächlich geändert wurde. Auf -2 setzen, um den Standardwert von `attribute::Expiration` zu verwenden.

## Standard {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` wird verwendet, wenn das Feld nicht vorhanden ist, wenn der Wert -2 oder wenn das Feld leer ist.

## Verwandte Themen {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
