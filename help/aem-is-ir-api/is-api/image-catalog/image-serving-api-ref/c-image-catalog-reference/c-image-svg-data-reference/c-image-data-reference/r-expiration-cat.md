---
description: Ablauf
solution: Experience Manager
title: Ablauf
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee329834-a2a0-44fd-a0a5-7bf5a8e0a5a5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# Ablauf{#expiration}

Dient zum Verwalten der Zwischenspeicherung von Client- und Proxyservern. Der Server berechnet die Ablaufzeit/das Ablaufdatum der HTTP-Antwortdaten, indem er diesen Wert zum Übertragungszeitpunkt/Übertragungsdatum hinzufügt.

Browser verwalten Caches anhand der Ablaufzeiten von Dateien. Bevor eine Anforderung an den Server übergeben wird, prüft der Browser seinen Cache, um festzustellen, ob die Datei bereits heruntergeladen wurde. Wenn dies der Fall ist und die Datei noch nicht abgelaufen ist, sendet der Browser anstelle einer normalen GET-Anfrage eine bedingte GET (z. B. mit dem im Anfrageheader festgelegten Feld If-Modified-Since ). Der Server hat die Möglichkeit, mit dem Status &#39;304&#39; zu antworten und das Bild nicht zu senden. Der Browser lädt die Datei dann aus dem Cache. Dies kann die Gesamtleistung für häufig aufgerufene Daten erheblich erhöhen.

Für diese Antworttypen wird Ablauf verwendet:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Bestimmte Arten von Antworten (z. B. Fehlerantworten) werden immer für den sofortigen Ablauf markiert (oder als nicht zwischenspeicherbar markiert), während andere (z. B. Eigenschaften- oder Standard-Bildantworten) spezielle Ablaufeinstellungen ( `attribute::NonImgExpiration` und `attribute::DefaultExpiration`) verwenden.

## Eigenschaften {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Real number, -2, -1 oder 0 oder höher. Anzahl der Stunden bis Ablauf seit der Erstellung des Antwortbilds. Auf 0 setzen, damit das Antwortbild immer sofort abläuft, wodurch das Client-Caching effektiv deaktiviert wird. Auf -1 setzen, um als *`never expire`* zu markieren. In diesem Fall gibt der Server bei bedingten GET immer den Status 304 (nicht geändert) zurück, ohne zu überprüfen, ob sich die Datei tatsächlich geändert hat. Setzen Sie diese Einstellung auf -2, um den von `attribute::Expiration` bereitgestellten Standard zu verwenden.

## Standard {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` wird verwendet, wenn das Feld nicht vorhanden ist, wenn der Wert -2 ist oder wenn das Feld leer ist.

## Verwandte Themen {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
