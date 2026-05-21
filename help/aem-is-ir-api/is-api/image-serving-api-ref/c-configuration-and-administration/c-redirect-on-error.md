---
description: ISS-Server können so konfiguriert werden, dass für Anfragen, die ein Quellbild betreffen, das nicht erfolgreich geöffnet oder gelesen werden kann, ein Failover zu alternativen Servern durchgeführt wird.
solution: Experience Manager
title: Bei Fehler umleiten
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
TQID: 'https://experienceleague.adobe.com/jNvJP4nJ7W1thf-ZDbSCzry54H8wI4DVGK8FW6koNCw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# Bei Fehler umleiten{#redirect-on-error}

ISS-Server können so konfiguriert werden, dass für Anfragen, die ein Quellbild betreffen, das nicht erfolgreich geöffnet oder gelesen werden kann, ein Failover zu alternativen Servern durchgeführt wird.

Die folgenden Arten von Anfragen werden umgeleitet:

* IS: Bilder, die sich im Katalog, aber nicht auf der Festplatte befinden.

  Wenn sich ein Bild nicht in einem Katalog befindet, sollte keine Fehlerumleitung erfolgen, wenn das Bild nicht gefunden werden kann.

* Beschädigte Bilder, Farbprofile oder Schriftarten.
* Statischer Inhalt kann nicht auf der Festplatte gefunden werden.

  Statische Inhaltsanfragen werden umgeleitet, wenn sie nicht auf der Festplatte gefunden werden können, selbst wenn der referenzierte statische Inhalt keinen Katalogdatensatz hat.

Die Fehlerumleitung findet in keinem anderen Fall statt.

Wenn diese Option aktiviert ist und während der Verarbeitung der Anfrage ein solcher Fehler auftritt, sendet der primäre Server die Anfrage zur Verarbeitung an den sekundären Server. Die Antwort wird dann direkt an den Client weitergeleitet, unabhängig davon, ob sie auf Erfolg oder Misserfolg hinweist. Der primäre Server markiert Protokolleinträge solcher weitergeleiteter Anfragen mit Cache-`REMOTE`. Die Antwortdaten werden nicht lokal vom primären Server zwischengespeichert.

Die Fehlerumleitung wird aktiviert, indem `PS::errorRedirect.rootUrl` auf den HTTP-Domain-Namen und die Port-Nummer des sekundären Servers festgelegt wird. Darüber hinaus wird das Verbindungs-Timeout mit `PS::errorRedirect.connectTimeout` konfiguriert. Die maximale Zeit, die der primäre Server auf eine Antwort vom sekundären Server wartet, bevor ein Fehler an den Client zurückgegeben wird, wird mit `PS::errorRedirect.socketTimeout` konfiguriert.

>[!NOTE]
>
>Wenn der sekundäre Server nicht kontaktiert werden kann, wird eine Textfehlerantwort an den Client zurückgegeben, auch wenn ein Standardbild oder ein Fehlerbild konfiguriert ist.

>[!NOTE]
>
>Pipe-Zeichen (|) im nächsten Pfad werden für die Fehlerumleitung nicht unterstützt.

## Verwandte Themen {#section-2e8bfc128b944baf8108279d16492f3f}

[Fehlerumleitung](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
