---
title: Ablauf
description: Wird für die Verwaltung der Zwischenspeicherung von Client- und Proxy-Servern verwendet. Der Server berechnet die Ablaufzeit/das Ablaufdatum der HTTP-Antwortdaten, indem er diesen Wert zu Übertragungszeit/Übertragungsdatum hinzufügt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 064dab12-5f58-4e19-a6b1-fbd20182e3aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 1%

---

# Ablauf{#expiration}

Wird für die Verwaltung der Zwischenspeicherung von Client- und Proxy-Servern verwendet. Der Server berechnet die Ablaufzeit/das Ablaufdatum der HTTP-Antwortdaten, indem er diesen Wert zu Übertragungszeit/Übertragungsdatum hinzufügt.

Browser verwalten Caches mit Gültigkeitsdauern von Dateien. Bevor eine Anfrage an den Server übergeben wird, prüft der Browser seinen Cache, um festzustellen, ob die Datei bereits heruntergeladen wurde. Wenn dies der Fall ist und die Datei noch nicht abgelaufen ist, sendet der Browser eine bedingte GET-Anfrage (z. B. mit dem in der Anfragekopfzeile festgelegten Feld If-Modified-Since ) anstelle einer normalen GET-Anfrage. Der Server hat die Möglichkeit, mit einem „304“-Status zu antworten und das Bild nicht zu übertragen. Der Browser lädt dann die Datei aus dem Cache. Dies kann die Gesamtleistung für häufig aufgerufene Daten erheblich steigern.

Die Gültigkeit wird für die folgenden Antworttypen verwendet:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Bestimmte Antworttypen (z. B. Fehlerantworten) sind immer für den sofortigen Ablauf markiert (oder als nicht zwischenspeicherbar getaggt), während andere (z. B. Eigenschafts- oder Standardbildantworten) spezielle Ablaufeinstellungen verwenden ( `attribute::NonImgExpiration` und `attribute::DefaultExpiration`).

## Eigenschaften {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Reelle Zahl, -2, -1 oder 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Erstellung des Antwortbildes. Auf 0 gesetzt, um das Antwortbild immer sofort ablaufen zu lassen, wodurch das Client-Caching effektiv deaktiviert wird. Auf -1 gesetzt, um als *`never expire`* zu markieren. In diesem Fall gibt der Server als Reaktion auf bedingte GET-Anfragen immer den Status 304 (Nicht geändert) zurück, ohne zu überprüfen, ob die Datei tatsächlich geändert wurde. Legen Sie dies auf -2 fest, um den von `attribute::Expiration` bereitgestellten Standardwert zu verwenden.

## Standard {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` wird verwendet, wenn das Feld nicht vorhanden ist, der Wert -2 ist oder das Feld leer ist.

## Verwandte Themen {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
