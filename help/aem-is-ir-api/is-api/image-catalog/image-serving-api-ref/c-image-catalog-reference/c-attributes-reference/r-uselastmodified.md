---
description: Zuletzt geänderte Antwort-Header aktivieren. Aktiviert oder deaktiviert die Aufnahme des Headers „Last-Modified“ in zwischenspeicherbare HTTP-Antworten, die von Image Serving ausgegeben werden.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Zuletzt geänderte Antwort-Header aktivieren. Aktiviert oder deaktiviert die Aufnahme des Headers „Last-Modified“ in zwischenspeicherbare HTTP-Antworten, die von Image Serving ausgegeben werden.

Der Server verwendet den neuesten `catalog::TimeStamp` aller an einer Antwort beteiligten Kataloge/Katalogdatensätze als den Wert der zuletzt geänderten Kopfzeile.

Sollte nur aktiviert werden, wenn ein verteiltes Caching-Netzwerk oder ein anderes Caching-System verwendet wird, das eTag-Kopfzeilen nicht unterstützt.

>[!NOTE]
>
>Bei der Verwendung von Last-Modified-Headern in einer Umgebung mit Lastenausgleich, die mehrere Image-Serving-Hosts umfasst, ist Vorsicht geboten. Die Client-Zwischenspeicherung kann entfallen und die Server-Last kann zunehmen, wenn die Server aus irgendeinem Grund unterschiedliche Zeitstempel für dieselben Katalogeinträge haben. Eine solche Situation kann wie folgt eintreten:
>
>* Weder `catalog::TimeStamp` noch `attribute::TimeStamp`, sodass die Änderungszeit der [!DNL catalog.ini]-Datei als Standard für die `catalog::TimeStamp` verwendet wird.
>
>* Anstatt die Bildkatalogdateien über eine Netzwerkbereitstellung freizugeben, verfügt jeder Server über eine eigene Instanz der Katalogdateien in einem lokalen Dateisystem.
>* Zwei oder mehr Instanzen derselben [!DNL catalog.ini]-Datei haben unterschiedliche Dateiänderungsdaten, die möglicherweise durch unsachgemäßes Kopieren der Dateien verursacht werden.
>

## Eigenschaften {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Markierung. 0 zum Deaktivieren, 1 zum Aktivieren der HTTP-Kopfzeilen der letzten Änderung.

## Standard {#section-4eb47aadab8b41609bef296a4115f9f4}

Von `default::UseLastModified` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog:TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
