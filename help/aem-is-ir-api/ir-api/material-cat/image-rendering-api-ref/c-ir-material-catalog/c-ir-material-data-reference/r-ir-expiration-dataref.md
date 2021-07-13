---
description: Client-Cache-Zeit bis zur Live-Schaltung. Anzahl der Stunden bis zum Ablauf. Dient zum Verwalten der Zwischenspeicherung von Client- und Proxyservern.
solution: Experience Manager
title: Ablauf
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%

---

# Ablauf{#expiration}

Client-Cache-Zeit bis zur Live-Schaltung. Anzahl der Stunden bis zum Ablauf. Dient zum Verwalten der Zwischenspeicherung von Client- und Proxyservern.

Der Server berechnet die Ablaufzeit/das Ablaufdatum der NTTP-Antwortdaten, indem er diesen Wert zum Übertragungszeitpunkt/Übertragungsdatum hinzufügt.

Browser verwalten Caches anhand der Ablaufzeiten von Dateien. Bevor eine Anforderung an den Server übergeben wird, prüft der Browser seinen Cache, um festzustellen, ob die Datei bereits heruntergeladen wurde. Wenn dies der Fall ist und die Datei noch nicht abgelaufen ist, sendet der Browser eine bedingte GET (z. B. mit dem HTTP-Anforderungsheader If-Modified-Since ) und keine normale GET-Anfrage. Der Server hat die Möglichkeit, mit dem Status &#39;304&#39; zu antworten und das Bild nicht zu senden. Der Browser lädt dann einfach die Datei aus dem Cache. Dies kann die Gesamtleistung für häufig aufgerufene Daten erheblich erhöhen.

Der Server setzt den HTTP-Antwort-Header expires auf den aktuellen Datums-/Uhrzeitwert sowie den kleinsten Vignettenwert::Expiration und alle catalog::Expiration -Werte für die Vignette und alle am Rendervorgang beteiligten Materialien.

Die Gültigkeit wird hauptsächlich für Bilddatenantworten festgelegt. Bestimmte Arten von Antworten werden immer für einen sofortigen Ablauf markiert (oder als nicht zwischenspeicherbar markiert), einschließlich aller Fehlerantworten oder Eigenschaftsantworten.

## Eigenschaften {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Real number, -2, -1, 0 oder höher. Anzahl der Stunden bis Ablauf seit der Erstellung des Antwortbilds. Auf 0 setzen, damit das Antwortbild immer sofort abläuft, wodurch das Client-Caching effektiv deaktiviert wird. Auf -1 setzen, um als `never expire` zu markieren. In diesem Fall gibt der Server immer den Status 304 (nicht geändert) als Antwort auf bedingte `GET` -Anfragen zurück, ohne zu überprüfen, ob die Datei tatsächlich geändert wurde. Setzen Sie diese Einstellung auf -2, um den von `attribute::Expiration` bereitgestellten Standard zu verwenden.

## Standard {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` wird verwendet, wenn das Feld nicht vorhanden ist, wenn der Wert -2 ist oder wenn das Feld leer ist.

## Verwandte Themen {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
