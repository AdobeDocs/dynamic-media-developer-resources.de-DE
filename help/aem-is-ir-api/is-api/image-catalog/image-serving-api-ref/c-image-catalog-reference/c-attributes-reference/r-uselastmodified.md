---
description: Zuletzt geänderte Antwort-Kopfzeilen aktivieren Aktiviert oder deaktiviert die Aufnahme des Headers Last-Modified in zwischenspeicherbaren HTTP-Antworten, die von Image Serving ausgegeben werden.
seo-description: Zuletzt geänderte Antwort-Kopfzeilen aktivieren Aktiviert oder deaktiviert die Aufnahme des Headers Last-Modified in zwischenspeicherbaren HTTP-Antworten, die von Image Serving ausgegeben werden.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

Zuletzt geänderte Antwort-Kopfzeilen aktivieren Aktiviert oder deaktiviert die Aufnahme des Headers Last-Modified in zwischenspeicherbaren HTTP-Antworten, die von Image Serving ausgegeben werden.

Der Server verwendet den neuesten `catalog::TimeStamp`-Wert aller Kataloge/Katalogeinträge, die an einer Antwort beteiligt sind, als Last-Modified-Header-Wert.

Sollte nur aktiviert sein, wenn ein verteiltes Cache-Netzwerk oder ein anderes Cache-System verwendet wird, das keine etag-Header unterstützt.

>[!NOTE]
>
>Bei der Verwendung von Last-Modified-Headern in einer Umgebung mit Lastenausgleich, bei der mehrere Image Serving-Hosts verwendet werden, ist Vorsicht geboten. Die Zwischenspeicherung im Client kann besiegt werden und die Serverlast wird erhöht, wenn die Server aus irgendeinem Grund unterschiedliche Zeitstempel für dieselben Katalogeinträge haben. Eine solche Situation kann wie folgt eintreten:
>
>* Weder `catalog::TimeStamp` noch `attribute::TimeStamp`, sodass die Änderungszeit der [!DNL catalog.ini]-Datei als Standard für `catalog::TimeStamp` verwendet wird.
   >
   >
* Anstatt die Bildkatalogdateien über eine Netzwerkbereitstellung freizugeben, verfügt jeder Server über eine eigene Instanz der Katalogdateien in einem lokalen Dateisystem.
>* Zwei oder mehr Instanzen der gleichen [!DNL catalog.ini]-Datei haben unterschiedliche Datumsangaben zur Dateiänderung, die möglicherweise durch fehlerhaftes Kopieren der Dateien verursacht werden.

>



## Eigenschaften {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Flag. 0 zur Deaktivierung, 1 zur Aktivierung der zuletzt geänderten HTTP-Header.

## Standard {#section-4eb47aadab8b41609bef296a4115f9f4}

Vererbt von `default::UseLastModified`, wenn nicht definiert oder leer.

## Verwandte Themen {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[Katalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
