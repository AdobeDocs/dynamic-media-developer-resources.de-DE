---
description: Cache-Einträge werden automatisch aktualisiert, indem entweder eine katalogbasierte oder eine ablaufbasierte Cache-Validierung verwendet wird, wie mit dem Attribut CacheValidationPolicy ausgewählt (in default.ini oder der .ini-Datei eines bestimmten Bildkatalogs).
solution: Experience Manager
title: Validierung des Antwort-Cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Validierung des Antwort-Cache{#response-cache-validation}

Cache-Einträge werden automatisch aktualisiert, indem entweder eine katalogbasierte oder eine ablaufbasierte Cache-Validierung verwendet wird, die mit dem Attribut::CacheValidationPolicy ausgewählt wurde (in default.ini oder der .ini-Datei eines bestimmten Bildkatalogs).

Bei katalogbasierter Validierung wird ein vorhandener Cache-Eintrag als veraltet betrachtet, wenn `catalog::LastModified` (oder `attribute::LastModified` oder die Dateiänderungszeit der [!DNL catalog.ini]-Datei kürzer ist als der Zeitpunkt, zu dem der Cache-Eintrag erstellt wurde.

Bei einer ablaufbasierten Validierung wird ein Cache-Eintrag nach 5 Minuten seit der letzten Validierung veraltet. In beiden Fällen validiert der Server veraltete Cache-Einträge, indem er die Dateidaten aller Bilddateien überprüft, die an der Erstellung der Anforderung beteiligt waren. Wenn sich die Dateidaten nicht geändert haben, wird der Zeitstempel des Cache-Eintrags aktualisiert und das zwischengespeicherte Datum als gültig betrachtet.

Für typische Anwendungen, die hauptsächlich Bilder betreffen, die in Bildkatalogen registriert sind, bietet eine Katalogbasierte Validierung einen Leistungsvorteil. Anwendungen, die keine Bildkataloge beinhalten, sollten die ablaufbasierte Cache-Validierung verwenden. Eine Möglichkeit, dies zu erreichen, besteht darin, `attribute::cacheValidationPolicy=0` in [!DNL default.ini] und `1` in allen spezifischen Bildkatalogdateien festzulegen.

Cache-Einträge werden ungültig und können neu generiert werden, wenn sich ein an der Anfrage beteiligter Katalogeintrag so ändert, dass das Antwortbild wahrscheinlich geändert wird. Beispielsweise ändert sich der Inhalt von `catalog::Modifier`.

>[!NOTE]
>
>Dynamic Media Pyramid TIFF (PTIFF)-Bilder behalten das Dateidatum intern im Dateiheader zu Überprüfungszwecken bei. Die vom Dateisystem gepflegte Dateiänderungszeit wird verwendet, um zu überprüfen, ob sich eine Nicht-PTIFF-Datei geändert hat.

Nur Bilddateien nehmen am Cache-Validierungsprozess teil. Änderungen an Schriftartendateien oder ICC-Profildateien führen nicht zur automatischen Invalidierung von Cache-Einträgen.
