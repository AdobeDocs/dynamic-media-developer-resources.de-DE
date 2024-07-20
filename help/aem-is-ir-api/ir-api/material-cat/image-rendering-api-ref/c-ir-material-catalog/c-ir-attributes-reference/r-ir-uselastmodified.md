---
title: UseLastModified
description: Zuletzt geänderte Antwortheader aktivieren. Aktiviert oder deaktiviert die Einbeziehung des Headers "Zuletzt geändert"in zwischenspeicherbaren HTTP-Antworten, die vom Bild-Rendering ausgegeben werden.
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

Zuletzt geänderte Antwortheader aktivieren. Aktiviert oder deaktiviert die Einbeziehung des Headers &quot;Zuletzt geändert&quot;in zwischenspeicherbaren HTTP-Antworten, die vom Bild-Rendering ausgegeben werden.

Der Server verwendet den neuesten `vignette::TimeStamp` - und `catalog::TimeStamp` -Wert aller Vignetten- und Materialkataloge/Katalogdatensätze, die an einer Antwort beteiligt sind, als Header-Wert der letzten Änderung.

Sollte nur aktiviert sein, wenn ein verteiltes Caching-Netzwerk wie Akamai verwendet wird, das keine eTag-Header unterstützt.

>[!NOTE]
>
>Bei der Verwendung von Last-Modified-Headern in einer lastausgeglichenen Umgebung mit mehreren Image Serving/Rendering-Hosts ist Vorsicht geboten. Die Zwischenspeicherung auf dem Client kann besiegt werden und die Server-Last steigt, wenn die Server aus irgendeinem Grund unterschiedliche Zeitstempel für dieselben Katalogeinträge haben. Eine solche Situation kann wie folgt eintreten:

* `catalog::TimeStamp`, `vignette::TimeStamp` oder `attribute::TimeStamp` ist nicht definiert, sodass die Änderungszeit der [!DNL catalog.ini]-Datei als Standard für `catalog::TimeStamp` verwendet wird.

* Anstatt die Materialkatalogdateien über eine Netzwerkbereitstellung freizugeben, verfügt jeder Server über eine eigene Instanz der Katalogdateien in einem lokalen Dateisystem.
* Zwei oder mehr Instanzen derselben [!DNL catalog.ini]-Datei haben unterschiedliche Datumsangaben für die Dateiänderung, die möglicherweise durch unzulässiges Kopieren der Dateien verursacht werden.

## Eigenschaften {#section-453952244193452caccfaf7f601007c1}

Flag. 0 zur Deaktivierung, 1 zur Aktivierung der zuletzt geänderten HTTP-Header.

## Standard {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Wird von `default::UseLastModified` übernommen, wenn nicht definiert oder leer.

## Verwandte Themen {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
