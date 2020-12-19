---
description: Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Bildkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er feststellt, dass die Hauptkatalogattributdatei geändert wurde.
seo-description: Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Bildkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er feststellt, dass die Hauptkatalogattributdatei geändert wurde.
seo-title: Aktualisieren von Bildkatalogen
solution: Experience Manager
title: Aktualisieren von Bildkatalogen
topic: Scene7 Image Serving - Image Rendering API
uuid: 7e2557c4-1155-429b-a630-a2aff6725a3b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---


# Aktualisieren von Bildkatalogen{#updating-image-catalogs}

Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Bildkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er feststellt, dass die Hauptkatalogattributdatei geändert wurde.

Um Bildkataloge auf dem Server zu aktualisieren, ersetzen Sie zunächst alle Katalogdatendateien, die geändert werden müssen, und ersetzen Sie dann die Katalogattributdatei (bzw. &quot;touch&quot;, um das Dateidatum zu aktualisieren), um eine erneute Katalogladung auszulösen.

## Inkrementelle Updates {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Das Laden und Verarbeiten großer Bildkataloge kann den Server erheblich belasten und sich möglicherweise negativ auf Live-Serving-Vorgänge auswirken. Um diese Auswirkungen zu minimieren, wird empfohlen, einen inkrementellen Katalog-Aktualisierungsmechanismus zu implementieren, der wie folgt funktioniert:

Eine primäre Katalogdatei, die alle Bilder enthält, wird jeden Abend während der niedrigen Traffic-Stunden geladen. Wenn es während des Tages erforderlich ist, Datensätze im Bildkatalog hinzuzufügen oder zu ändern, wird eine weitere Bilddatendatei erstellt, die nur die neuen oder geänderten Datensätze enthält. Diese Datei ist als sekundäre Bilddatendatei in `attribute::CatalogFile` registriert. Der Server erkennt, dass sich die Katalogattributdatei geändert hat, und überprüft dann, welche Katalogdatendateien geändert wurden. Wenn die Hauptbilddatendatei nicht berührt wurde, lädt oder lädt der Server nur die inkrementelle Datendatei neu. Da diese Datei in der Regel viel kleiner ist als die Hauptkatalogdatei, sind die Auswirkungen auf den Server im Vergleich zum Neuladen des Hauptkatalogs erheblich geringer.

Inkrementelle Updates können die Auswirkungen auf den Server bei hohem Traffic erheblich reduzieren. Es wird empfohlen, die inkrementelle Katalogdatendatei regelmäßig während der Traffic-Zeit in die Hauptkatalogdatendatei einzufügen, um eine optimale Serverleistung zu gewährleisten.
