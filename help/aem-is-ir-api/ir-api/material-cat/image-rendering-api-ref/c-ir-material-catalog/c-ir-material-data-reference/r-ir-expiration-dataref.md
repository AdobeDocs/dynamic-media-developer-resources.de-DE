---
title: Ablauf
description: Client-Cache-Lebensdauer. Anzahl der Stunden bis zum Ablauf. Wird für die Verwaltung der Zwischenspeicherung von Client- und Proxy-Servern verwendet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---

# Ablauf{#expiration}

Client-Cache-Lebensdauer. Anzahl der Stunden bis zum Ablauf. Wird für die Verwaltung der Zwischenspeicherung von Client- und Proxy-Servern verwendet.

Der Server berechnet die Ablaufzeit/das Ablaufdatum der NTP-Antwortdaten, indem er diesen Wert zu Übertragungszeit/Übertragungsdatum hinzufügt.

Browser verwalten Caches mit Gültigkeitsdauern von Dateien. Bevor eine Anfrage an den Server übergeben wird, prüft der Browser seinen Cache, um festzustellen, ob die Datei bereits heruntergeladen wurde. Wenn dies der Fall ist und die Datei noch nicht abgelaufen ist, sendet der Browser eine bedingte GET-Anfrage (z. B. mit dem If-Modified-Since HTTP-Anfrage-Header) anstelle einer normalen GET-Anfrage. Der Server hat die Möglichkeit, mit einem „304“-Status zu antworten und das Bild nicht zu übertragen. Der Browser lädt dann einfach die Datei aus dem Cache. Dies kann die Gesamtleistung für häufig aufgerufene Daten erheblich steigern.

Der Server legt den HTTP-Antwort-Header „Expire“ auf das aktuelle Datum/die aktuelle Uhrzeit plus den kleinsten Wert von „vignette::Expiration“ und alle „catalog::Expiration“-Werte für die Vignette und alle am Render-Vorgang beteiligten Materialien fest.

Die Gültigkeit wird hauptsächlich für Bilddatenantworten festgelegt. Bestimmte Arten von Antworten werden immer für den sofortigen Ablauf markiert (oder als nicht zwischenspeicherbar gekennzeichnet), einschließlich aller Fehlerantworten oder Eigenschaftsantworten.

## Eigenschaften {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Reelle Zahl, -2, -1, 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Erstellung des Antwortbildes. Auf 0 gesetzt, um das Antwortbild immer sofort ablaufen zu lassen, wodurch das Client-Caching effektiv deaktiviert wird. Auf -1 gesetzt, um als `never expire` zu markieren. In diesem Fall gibt der Server immer den Status 304 (Nicht geändert) als Reaktion auf bedingte `GET`-Anfragen zurück, ohne zu überprüfen, ob die Datei tatsächlich geändert wurde. Legen Sie dies auf -2 fest, um den von `attribute::Expiration` bereitgestellten Standardwert zu verwenden.

## Standard {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` wird verwendet, wenn das Feld nicht vorhanden ist, der Wert -2 ist oder das Feld leer ist.

## Verwandte Themen {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
