---
description: IS-Server können so konfiguriert werden, dass sie bei Anforderungen, die ein Quellbild beinhalten, das nicht erfolgreich geöffnet oder gelesen werden kann, auf andere Server wechseln.
seo-description: IS-Server können so konfiguriert werden, dass sie bei Anforderungen, die ein Quellbild beinhalten, das nicht erfolgreich geöffnet oder gelesen werden kann, auf andere Server wechseln.
seo-title: Bei Fehler umleiten
solution: Experience Manager
title: Bei Fehler umleiten
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 894babe9-9c3c-4972-ae8f-387d65b4167d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---


# Bei Fehler umleiten{#redirect-on-error}

IS-Server können so konfiguriert werden, dass sie bei Anforderungen, die ein Quellbild beinhalten, das nicht erfolgreich geöffnet oder gelesen werden kann, auf andere Server wechseln.

Die folgenden Anforderungstypen werden umgeleitet:

* IS Images that are in the catalog, but not on disk.

   Wenn sich ein Bild nicht in einem Katalog befindet, sollte keine Fehlerumleitung erfolgen, wenn das Bild nicht gefunden werden kann.

* Korrigiert Bilder, Profile oder Schriftarten.
* Statische Inhalte können nicht auf der Festplatte gefunden werden.

   Statische Inhaltsanforderungen werden umgeleitet, wenn sie nicht auf der Festplatte gefunden werden können, selbst wenn der referenzierte statische Inhalt keinen Katalogdatensatz hat.

Fehler-Umleitung findet in keinem anderen Fall statt.

Wenn diese Option aktiviert ist und während der Verarbeitung der Anforderung ein solcher Fehler auftritt, sendet der primäre Server die Anforderung zur Verarbeitung an den sekundären Server. Die Antwort wird dann direkt an den Kunden weitergeleitet, unabhängig davon, ob sie auf Erfolg oder Misserfolg hinweist. Der primäre Server markiert Protokolleinträge solcher weitergeleiteten Anforderungen mit Cache-Verwendung von `REMOTE`. Die Antwortdaten werden vom primären Server nicht lokal zwischengespeichert.

Die Fehlerumleitung wird aktiviert, indem `PS::errorRedirect.rootUrl` auf den HTTP-Domänennamen und die Anschlussnummer des sekundären Servers eingestellt wird. Darüber hinaus wird die Zeitüberschreitung der Verbindung mit `PS::errorRedirect.connectTimeout` konfiguriert und die maximale Zeit, die der primäre Server auf eine Antwort vom sekundären Server wartet, bevor ein Fehler an den Client zurückgegeben wird, mit `PS::errorRedirect.socketTimeout` konfiguriert wird.

>[!NOTE]
>
>Wenn der sekundäre Server nicht kontaktiert werden kann, wird eine Textfehlermeldung an den Client zurückgegeben, auch wenn ein Standardbild oder ein Fehlerbild konfiguriert ist.

>[!NOTE]
>
>Pipe-Zeichen (|) im Netzpfad werden für die Fehlerumleitung nicht unterstützt.

## Verwandte Themen {#section-2e8bfc128b944baf8108279d16492f3f}

[Fehler-Umleitung](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
