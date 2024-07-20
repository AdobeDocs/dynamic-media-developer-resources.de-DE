---
description: IS-Server können so konfiguriert werden, dass sie bei Anforderungen, die ein Quellbild beinhalten, das nicht erfolgreich geöffnet oder gelesen werden kann, auf alternative Server umgestellt werden.
solution: Experience Manager
title: Weiterleitung bei Fehler
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Weiterleitung bei Fehler{#redirect-on-error}

IS-Server können so konfiguriert werden, dass sie bei Anforderungen, die ein Quellbild beinhalten, das nicht erfolgreich geöffnet oder gelesen werden kann, auf alternative Server umgestellt werden.

Die folgenden Anforderungstypen werden umgeleitet:

* IS Bilder, die sich im Katalog befinden, aber nicht auf der Festplatte.

  Wenn sich ein Bild nicht in einem Katalog befindet, sollte keine Fehlerumleitung erfolgen, wenn das Bild nicht gefunden werden kann.

* Beschädigte Bilder, Farbprofile oder Schriftarten.
* Statische Inhalte können nicht auf der Festplatte gefunden werden.

  Statische Inhaltsanforderungen werden umgeleitet, wenn sie nicht auf der Festplatte zu finden sind, selbst wenn der referenzierte statische Inhalt keinen Katalogdatensatz aufweist.

In keinem anderen Fall kommt es zu einer Fehler-Umleitung.

Wenn diese Option aktiviert ist und ein solcher Fehler während der Verarbeitung der Anfrage auftritt, sendet der primäre Server die Anfrage zur Verarbeitung an den sekundären Server. Die Antwort wird dann direkt an den Client weitergeleitet, unabhängig davon, ob sie auf Erfolg oder Fehler hinweist. Der primäre Server markiert Protokolleinträge solcher weitergeleiteter Anfragen mit dem Cache-Wert `REMOTE`. Die Antwortdaten werden vom primären Server nicht lokal zwischengespeichert.

Die Umleitung von Fehlern wird aktiviert, indem `PS::errorRedirect.rootUrl` auf den HTTP-Domänennamen und die Anschlussnummer des sekundären Servers gesetzt wird. Darüber hinaus wird das Verbindungs-Timeout mit `PS::errorRedirect.connectTimeout` konfiguriert und die maximale Zeit, die der primäre Server auf eine Antwort vom sekundären Server wartet, bevor ein Fehler an den Client zurückgegeben wird, mit `PS::errorRedirect.socketTimeout` konfiguriert.

>[!NOTE]
>
>Wenn der sekundäre Server nicht kontaktiert werden kann, wird eine Textfehlerantwort an den Client zurückgegeben, selbst wenn ein Standardbild oder ein Fehlerbild konfiguriert ist.

>[!NOTE]
>
>Pipeline-Zeichen (|) im Netzpfad werden für die Fehlerumleitung nicht unterstützt.

## Verwandte Themen {#section-2e8bfc128b944baf8108279d16492f3f}

[Fehlerumleitung](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
