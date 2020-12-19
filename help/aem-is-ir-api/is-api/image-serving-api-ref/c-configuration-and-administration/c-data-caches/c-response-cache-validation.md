---
description: Cache-Einträge werden automatisch aktualisiert, indem entweder katalogbasierte oder ablaufbasierte Cache-Validierung verwendet wird, wie mit dem Attribut CacheValidationPolicy (in default.ini oder der .ini-Datei eines bestimmten Bildkatalogs) ausgewählt.
seo-description: Cache-Einträge werden automatisch aktualisiert, indem entweder katalogbasierte oder ablaufbasierte Cache-Validierung verwendet wird, wie mit dem Attribut CacheValidationPolicy (in default.ini oder der .ini-Datei eines bestimmten Bildkatalogs) ausgewählt.
seo-title: Validierung des Antwortcache
solution: Experience Manager
title: Validierung des Antwortcache
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# Validierung des Antwortcache{#response-cache-validation}

Cache-Einträge werden automatisch aktualisiert, indem entweder katalogbasierte oder ablaufbasierte Cache-Validierung verwendet wird, wie mit attribute::CacheValidationPolicy ausgewählt (in default.ini oder der .ini-Datei eines bestimmten Bildkatalogs).

Bei katalogbasierter Validierung wird ein vorhandener Cache-Eintrag als &quot;statisch&quot;betrachtet, wenn `catalog::LastModified` (oder `attribute::LastModified` oder die Dateiänderungszeit der [!DNL catalog.ini]-Datei) kürzer ist als der Zeitpunkt, zu dem der Cache-Eintrag erstellt wurde.

Bei einer ablaufbasierten Validierung wird ein Cache-Eintrag nach 5 Minuten seit der letzten Validierung statisch. In beiden Fällen validiert der Server statische Cache-Einträge, indem er die Dateidaten aller Bilddateien überprüft, die mit der Erstellung der Anforderung befasst waren. Wenn sich die Dateidaten nicht geändert haben, wird der Zeitstempel des Cache-Eintrags aktualisiert und das zwischengespeicherte Datum als gültig betrachtet.

Für typische Anwendungen, bei denen es sich hauptsächlich um in Bildkatalogen registrierte Bilder handelt, bietet eine katalogbasierte Validierung einen Leistungsvorteil. Anwendungen, die keine Bildkataloge beinhalten, sollten eine ablaufbasierte Cache-Validierung verwenden. Eine Möglichkeit, dies zu erreichen, besteht darin, `attribute::cacheValidationPolicy=0` in [!DNL default.ini] und `1` in allen Bildkatalogdateien einzustellen.

Cache-Einträge werden ungültig und können erneut generiert werden, wenn sich ein an der Anforderung beteiligter Katalogeintrag so ändert, dass das Antwortbild wahrscheinlich geändert wird. Beispielsweise ändert sich der Inhalt von `catalog::Modifier`.

>[!NOTE]
>
>Scene7 Pyramid TIFF-(PTIFF-)Bilder behalten das Dateidatum intern im Dateikopf zu Überprüfungszwecken bei. Die Dateiänderungszeit, die vom Dateisystem beibehalten wird, dient zur Überprüfung, ob sich eine Nicht-PTIFF-Datei geändert hat.

Nur Bilddateien nehmen am Cache-Validierungsprozess teil. Änderungen an Schriftartdateien oder ICC-Profil-Dateien führen nicht zur automatischen Ungültigmachung von Cache-Einträgen.
