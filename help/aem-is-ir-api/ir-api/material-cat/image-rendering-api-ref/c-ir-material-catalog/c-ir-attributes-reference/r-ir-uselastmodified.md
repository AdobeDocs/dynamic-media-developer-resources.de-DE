---
title: UseLastModified
description: Zuletzt geänderte Antwort-Header aktivieren. Aktiviert oder deaktiviert die Aufnahme des Headers „Last-Modified“ in zwischenspeicherbare HTTP-Antworten, die vom Bild-Rendering ausgegeben werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
TQID: 'https://experienceleague.adobe.com/X-d-02WckbxVyDxRvZDIcOghkk8Z8yYbGOZ3Aigx4ts'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
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
