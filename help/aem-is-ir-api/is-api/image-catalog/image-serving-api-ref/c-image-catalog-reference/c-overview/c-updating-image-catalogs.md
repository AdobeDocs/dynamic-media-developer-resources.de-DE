---
description: Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Bildkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er feststellt, dass die Hauptkatalogattributdatei geändert wurde.
solution: Experience Manager
title: Aktualisieren von Bildkatalogen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Aktualisieren von Bildkatalogen{#updating-image-catalogs}

Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Bildkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er feststellt, dass die Hauptkatalogattributdatei geändert wurde.

Um Bildkataloge auf dem Server zu aktualisieren, ersetzen Sie zunächst alle Katalogdatendateien, die geändert werden müssen, und ersetzen Sie dann die Katalogattributdatei (bzw. &quot;berühren&quot;, um das Dateidatum zu aktualisieren), sodass sie Trigger wird, dass der Katalog neu geladen wird.

## Inkrementelle Aktualisierungen {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Das Laden und Verarbeiten großer Bildkataloge kann den Server erheblich belasten und sich negativ auf Live-Serving-Vorgänge auswirken. Um diese Auswirkungen zu minimieren, wird empfohlen, einen inkrementellen Katalogaktualisierungsmechanismus zu implementieren, der wie folgt funktioniert:

Eine primäre Katalogdatei, die alle Bilder enthält, wird nächtlich während geringer Traffic-Zeiten geladen. Wenn es tagsüber erforderlich ist, Datensätze im Bildkatalog hinzuzufügen oder zu ändern, wird eine weitere Bilddatendatei erstellt, die nur die neuen oder geänderten Datensätze enthält. Diese Datei wird als sekundäre Bilddatendatei in `attribute::CatalogFile` registriert. Der Server erkennt, dass sich die Katalogattributdatei geändert hat, und überprüft dann, welche Katalogdatendateien sich geändert haben. Wenn die Hauptbilddatendatei nicht berührt wurde, lädt oder lädt der Server nur die inkrementelle Datendatei neu. Da diese Datei in der Regel viel kleiner ist als die Hauptkatalogdatei, sind die Auswirkungen auf den Server im Vergleich zum Neuladen des Hauptkatalogs erheblich geringer.

Inkrementelle Aktualisierungen können die Auswirkungen auf den Server bei hohem Traffic erheblich reduzieren. Es wird empfohlen, die inkrementelle Katalogdatendatei regelmäßig während wenig Traffic-Stunden in der Hauptkatalogdatendatei zusammenzuführen, um eine optimale Serverleistung zu gewährleisten.
