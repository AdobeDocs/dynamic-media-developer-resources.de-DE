---
description: Cache-Einträge werden automatisch entweder mit katalogbasierter oder ablaufbasierter Cache-Validierung aktualisiert, wie mit dem Attribut CacheValidationPolicy ausgewählt (in default.ini oder der .ini-Datei eines bestimmten Bildkatalogs).
solution: Experience Manager
title: Validierung des Antwort-Caches
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Validierung des Antwort-Caches{#response-cache-validation}

Cache-Einträge werden automatisch entweder mit katalogbasierter oder ablaufbasierter Cache-Validierung aktualisiert, wie mit dem Attribut::CacheValidationPolicy ausgewählt (in default.ini oder der .ini-Datei eines bestimmten Bildkatalogs).

Bei der katalogbasierten Validierung gilt ein vorhandener Cache-Eintrag als veraltet, wenn `catalog::LastModified` (oder `attribute::LastModified` oder die Dateiänderungszeit der [!DNL catalog.ini]-Datei) aktueller ist als die Zeit, zu der der Cache-Eintrag erstellt wurde.

Bei der ablaufbasierten Validierung veraltet ein Cache-Eintrag nach 5 Minuten seit der letzten Validierung. In beiden Fällen validiert der Server veraltete Cache-Einträge, indem er die Dateidaten aller Bilddateien prüft, die an der Erstellung der Anfrage beteiligt waren. Wenn sich die Dateidaten nicht geändert haben, wird der Zeitstempel des Cache-Eintrags aktualisiert und das zwischengespeicherte Datum als gültig betrachtet.

Für typische Anwendungen, bei denen Bilder hauptsächlich in Bildkatalogen registriert sind, bietet die katalogbasierte Validierung einen Leistungsvorteil. Anwendungen, die keine Bildkataloge beinhalten, sollten eine ablaufbasierte Cache-Validierung verwenden. Eine Möglichkeit, dies zu erreichen, besteht darin, `attribute::cacheValidationPolicy=0` in [!DNL default.ini] festzulegen und in allen spezifischen Bildkatalogdateien zu `1`.

Cache-Einträge werden ungültig und können neu generiert werden, wenn sich ein in der Anfrage involvierter Katalogeintrag in einer Weise ändert, die wahrscheinlich zu einer Änderung des Antwortbildes führen würde. Beispielsweise ändert sich der Inhalt von `catalog::Modifier`.

>[!NOTE]
>
>Dynamic Media Pyramid TIFF (PTIFF)-Bilder behalten das Dateidatum intern in der Dateikopfzeile zu Validierungszwecken bei. Die vom Dateisystem verwaltete Dateiänderungszeit wird verwendet, um zu überprüfen, ob eine Nicht-PTIFF-Datei geändert wurde.

Nur Bilddateien nehmen am Cache-Validierungsprozess teil. Änderungen an Schriftarten oder ICC-Profildateien führen nicht zu einer automatischen Invalidierung der Cache-Einträge.
