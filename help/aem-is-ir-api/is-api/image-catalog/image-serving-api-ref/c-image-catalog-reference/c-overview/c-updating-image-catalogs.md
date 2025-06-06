---
description: Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Bildkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er erkennt, dass die Hauptkatalogattributdatei geändert wurde.
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

Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Bildkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er erkennt, dass die Hauptkatalogattributdatei geändert wurde.

Um die Bildkataloge auf dem Server zu aktualisieren, ersetzen Sie zunächst alle zu ändernden Katalogdatendateien und ersetzen Sie dann die Katalogattributdatei, um das Katalogdatum zu aktualisieren (bzw. berühren Sie diese, um sie zu aktualisieren), sodass der Trigger den Katalog neu lädt.

## Inkrementelle Aktualisierungen {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Das Laden und Verarbeiten großer Bildkataloge kann den Server erheblich belasten und sich negativ auf die Live-Serving-Vorgänge auswirken. Um diese Auswirkungen zu minimieren, wird empfohlen, einen inkrementellen Katalogaktualisierungsmechanismus zu implementieren, der wie folgt funktioniert:

Eine primäre Katalogdatei, die alle Bilder enthält, wird jede Nacht während der Stunden mit geringem Traffic geladen. Wenn es tagsüber erforderlich ist, Datensätze im Bildkatalog hinzuzufügen oder zu ändern, wird eine andere Bilddatendatei erstellt, die nur die neuen oder geänderten Datensätze enthält. Diese Datei wird in `attribute::CatalogFile` als sekundäre Bilddatendatei registriert. Der Server erkennt, dass die Katalogattributdatei geändert wurde, und prüft dann, welche Katalogdatendateien geändert wurden. Wenn die Hauptbilddatendatei nicht berührt wurde, lädt der Server nur die inkrementelle Datendatei oder lädt sie neu. Da diese Datei in der Regel viel kleiner ist als die Hauptkatalogdatei, sind die Auswirkungen auf den Server viel geringer, verglichen mit dem Neuladen des Hauptkatalogs.

Inkrementelle Aktualisierungen können die Auswirkungen auf den Server bei starkem Traffic erheblich reduzieren. Es wird empfohlen, die inkrementelle Katalogdatendatei während verkehrsarmer Stunden regelmäßig mit der Hauptkatalogdatendatei zusammenzuführen, um eine optimale Server-Leistung zu gewährleisten.
