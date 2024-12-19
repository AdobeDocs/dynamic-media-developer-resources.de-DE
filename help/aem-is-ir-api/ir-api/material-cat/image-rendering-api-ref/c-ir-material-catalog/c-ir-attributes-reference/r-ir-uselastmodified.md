---
title: UseLastModified
description: Zuletzt geänderte Antwort-Header aktivieren. Aktiviert oder deaktiviert die Aufnahme des Headers „Last-Modified“ in zwischenspeicherbare HTTP-Antworten, die vom Bild-Rendering ausgegeben werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Zuletzt geänderte Antwort-Header aktivieren. Aktiviert oder deaktiviert die Aufnahme des Headers „Last-Modified“ in zwischenspeicherbare HTTP-Antworten, die vom Bild-Rendering ausgegeben werden.

Der Server verwendet den neuesten `vignette::TimeStamp`- und `catalog::TimeStamp` aller an einer Antwort beteiligten Vignetten- und Materialkataloge/Katalogdatensätze als den zuletzt geänderten Header-Wert.

Sollte nur aktiviert werden, wenn ein verteiltes Caching-Netzwerk wie Akamai verwendet wird, das keine eTag-Kopfzeilen unterstützt.

>[!NOTE]
>
>Bei der Verwendung von Headern des Typs „Letzte Änderung“ in einer Umgebung mit Lastenausgleich, die mehrere Image-Serving-/Rendering-Hosts umfasst, ist Vorsicht geboten. Die Client-Zwischenspeicherung kann entfallen und die Server-Last kann zunehmen, wenn die Server aus irgendeinem Grund unterschiedliche Zeitstempel für dieselben Katalogeinträge haben. Eine solche Situation kann wie folgt eintreten:

* `catalog::TimeStamp`, `vignette::TimeStamp` oder `attribute::TimeStamp` ist nicht definiert, sodass die Änderungszeit der [!DNL catalog.ini]-Datei als Standard für `catalog::TimeStamp` verwendet wird.

* Anstatt die Materialkatalogdateien über eine Netzwerkbereitstellung freizugeben, hat jeder Server seine eigene Instanz der Katalogdateien auf einem lokalen Dateisystem.
* Zwei oder mehr Instanzen derselben [!DNL catalog.ini]-Datei haben unterschiedliche Dateiänderungsdaten, die möglicherweise durch unsachgemäßes Kopieren der Dateien verursacht werden.

## Eigenschaften {#section-453952244193452caccfaf7f601007c1}

Markierung. 0 zum Deaktivieren, 1 zum Aktivieren der HTTP-Kopfzeilen der letzten Änderung.

## Standard {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Von `default::UseLastModified` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
