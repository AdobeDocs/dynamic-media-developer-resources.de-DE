---
description: Client-Cache-Zeit zum Live-Betrieb. Anzahl der Stunden bis zum Ablauf. Wird zur Verwaltung der Zwischenspeicherung von Client- und Proxyservern verwendet.
seo-description: Client-Cache-Zeit zum Live-Betrieb. Anzahl der Stunden bis zum Ablauf. Wird zur Verwaltung der Zwischenspeicherung von Client- und Proxyservern verwendet.
seo-title: Ablauf
solution: Experience Manager
title: Ablauf
topic: Scene7 Image Serving - Image Rendering API
uuid: 6dbd7d43-727c-42fc-8953-dba112209a45
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---


# Ablauf{#expiration}

Client-Cache-Zeit zum Live-Betrieb. Anzahl der Stunden bis zum Ablauf. Wird zur Verwaltung der Zwischenspeicherung von Client- und Proxyservern verwendet.

Der Server berechnet die Ablaufzeit/das Datum der NTTP-Antwortdaten, indem er diesen Wert zum Datum/Datum der Übertragung hinzufügt.

Browser verwalten Caches mit Ablaufzeiten von Dateien. Bevor eine Anforderung an den Server weitergeleitet wird, prüft der Browser den Cache, um festzustellen, ob die Datei bereits heruntergeladen wurde. Wenn dies der Fall ist und die Datei noch nicht abgelaufen ist, sendet der Browser anstelle einer normalen GET eine bedingte GET (z. B. mit dem HTTP-Anforderungsheader &quot;If-Modified-Since&quot;). Der Server hat die Möglichkeit, mit dem Status &#39;304&#39; zu antworten und das Bild nicht zu senden. Der Browser lädt dann die Datei einfach aus dem Cache. Dies kann die Gesamtleistung für häufig aufgerufene Daten deutlich erhöhen.

Der Server stellt den abgelaufenen HTTP-Antwortheader auf das aktuelle Datum/die aktuelle Uhrzeit sowie die kleinste Vignette ein::Expiration und alle catalog::Expiration-Werte für die Vignette und alle Materialien, die am Rendervorgang beteiligt sind.

Der Ablauf wird hauptsächlich für Bilddatenantworten festgelegt. Bestimmte Arten von Antworten werden immer für einen sofortigen Ablauf markiert (oder als nicht speicherbar markiert), einschließlich aller Fehlerantworten oder Antworten auf Eigenschaften.

## Eigenschaften {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Real number, -2, -1, 0 oder höher. Anzahl der Stunden bis zum Ablauf seit der Generierung des Antwortbilds. Auf 0 setzen, um das Antwortbild immer sofort ablaufen zu lassen, wodurch die Zwischenspeicherung des Clients effektiv deaktiviert wird. Auf -1 setzen, um als `never expire` zu markieren. In diesem Fall gibt der Server bei bedingten `GET`-Anforderungen immer den Status 304 (nicht modifiziert) zurück, ohne zu überprüfen, ob die Datei tatsächlich geändert wurde. Auf -2 setzen, um den Standardwert von `attribute::Expiration` zu verwenden.

## Standard {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` wird verwendet, wenn das Feld nicht vorhanden ist, wenn der Wert -2 oder wenn das Feld leer ist.

## Verwandte Themen {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [Vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
