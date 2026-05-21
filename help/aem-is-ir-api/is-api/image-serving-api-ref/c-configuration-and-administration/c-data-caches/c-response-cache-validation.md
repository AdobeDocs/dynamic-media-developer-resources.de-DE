---
description: Cache-Einträge werden automatisch entweder mit katalogbasierter oder ablaufbasierter Cache-Validierung aktualisiert, wie mit dem Attribut CacheValidationPolicy ausgewählt (in default.ini oder der .ini-Datei eines bestimmten Bildkatalogs).
solution: Experience Manager
title: Validierung des Antwort-Caches
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
TQID: 'https://experienceleague.adobe.com/VnvYNkc3yijayG8tnJKHsp94Qto8VZj9OkIgfIv1Kc0'
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
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 311
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
