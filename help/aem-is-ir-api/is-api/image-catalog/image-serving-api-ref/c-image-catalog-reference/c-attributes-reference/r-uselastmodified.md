---
description: Zuletzt geänderte Antwort-Header aktivieren. Aktiviert oder deaktiviert die Aufnahme des Headers „Last-Modified“ in zwischenspeicherbare HTTP-Antworten, die von Image Serving ausgegeben werden.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
TQID: 'https://experienceleague.adobe.com/jmwz9jThBnFtTZBRoI0kbKwoxf1MU7rn1CpKrSU4f04'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
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
