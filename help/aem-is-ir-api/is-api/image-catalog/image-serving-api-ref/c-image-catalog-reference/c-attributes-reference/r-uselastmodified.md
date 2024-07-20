---
description: Zuletzt geänderte Antwortheader aktivieren. Aktiviert oder deaktiviert die Einbeziehung des Headers "Zuletzt geändert"in zwischenspeicherbaren HTTP-Antworten, die von Image Serving ausgegeben werden.
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

Zuletzt geänderte Antwortheader aktivieren. Aktiviert oder deaktiviert die Einbeziehung des Headers &quot;Zuletzt geändert&quot;in zwischenspeicherbaren HTTP-Antworten, die von Image Serving ausgegeben werden.

Der Server verwendet den neuesten `catalog::TimeStamp` -Wert aller Kataloge/Katalogdatensätze, die an einer Antwort beteiligt sind, als Header-Wert der letzten Änderung.

Sollte nur aktiviert sein, wenn ein verteiltes Caching-Netzwerk oder ein anderes Caching-System verwendet wird, das keine eTag-Header unterstützt.

>[!NOTE]
>
>Bei der Verwendung von Last-Modified-Headern in einer lastausgeglichenen Umgebung mit mehreren Image Serving-Hosts ist Vorsicht geboten. Die Zwischenspeicherung auf dem Client kann besiegt werden und die Server-Last steigt, wenn die Server aus irgendeinem Grund unterschiedliche Zeitstempel für dieselben Katalogeinträge haben. Eine solche Situation kann wie folgt eintreten:
>
>* Weder `catalog::TimeStamp` noch `attribute::TimeStamp`, sodass die Änderungszeit der [!DNL catalog.ini]-Datei als Standard für `catalog::TimeStamp` verwendet wird.
>
>* Anstatt die Bildkatalogdateien über eine Netzwerkbereitstellung freizugeben, verfügt jeder Server über eine eigene Instanz der Katalogdateien in einem lokalen Dateisystem.
>* Zwei oder mehr Instanzen derselben [!DNL catalog.ini]-Datei haben unterschiedliche Datumsangaben für die Dateiänderung, die möglicherweise durch unzulässiges Kopieren der Dateien verursacht werden.
>

## Eigenschaften {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Flag. 0 zur Deaktivierung, 1 zur Aktivierung der zuletzt geänderten HTTP-Header.

## Standard {#section-4eb47aadab8b41609bef296a4115f9f4}

Wird von `default::UseLastModified` übernommen, wenn nicht definiert oder leer.

## Verwandte Themen {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
