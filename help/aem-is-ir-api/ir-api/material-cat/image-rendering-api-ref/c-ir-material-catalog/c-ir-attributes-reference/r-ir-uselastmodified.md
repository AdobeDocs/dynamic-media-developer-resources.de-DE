---
description: Zuletzt geänderte Antwort-Kopfzeilen aktivieren Aktiviert bzw. deaktiviert die Aufnahme des Headers Last-Modified in Cache-fähige HTTP-Antworten, die vom Image Rendering ausgestrahlt werden.
seo-description: Zuletzt geänderte Antwort-Kopfzeilen aktivieren Aktiviert bzw. deaktiviert die Aufnahme des Headers Last-Modified in Cache-fähige HTTP-Antworten, die vom Image Rendering ausgestrahlt werden.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

Zuletzt geänderte Antwort-Kopfzeilen aktivieren Aktiviert bzw. deaktiviert die Aufnahme des Headers Last-Modified in Cache-fähige HTTP-Antworten, die vom Image Rendering ausgestrahlt werden.

Der Server verwendet den neuesten `vignette::TimeStamp`- und `catalog::TimeStamp`-Wert aller Vignetten- und Materialkataloge/Katalogeinträge, die an einer Antwort beteiligt sind, als Last-Modified-Header-Wert.

Sollte nur aktiviert sein, wenn ein verteiltes Cache-Netzwerk wie Akamai verwendet wird, das keine Tag-Header unterstützt.

>[!NOTE]
>
>Bei der Verwendung von Last-Modified-Headern in einer Umgebung mit Lastenausgleich, bei der mehrere Image Serving/Rendering-Hosts verwendet werden, ist Vorsicht geboten. Die Zwischenspeicherung im Client kann besiegt werden und die Serverlast wird erhöht, wenn die Server aus irgendeinem Grund unterschiedliche Zeitstempel für dieselben Katalogeinträge haben. Eine solche Situation kann wie folgt eintreten:

* Weder `catalog::TimeStamp`, `vignette::TimeStamp` noch `attribute::TimeStamp` sind definiert, sodass die Änderungszeit der [!DNL catalog.ini]-Datei als Standard für `catalog::TimeStamp` verwendet wird.

* Anstatt die Materialkatalogdateien über eine Netzwerkbereitstellung freizugeben, verfügt jeder Server über eine eigene Instanz der Katalogdateien in einem lokalen Dateisystem.
* Zwei oder mehr Instanzen der gleichen [!DNL catalog.ini]-Datei haben unterschiedliche Datumsangaben zur Dateiänderung, die möglicherweise durch fehlerhaftes Kopieren der Dateien verursacht werden.

## Eigenschaften {#section-453952244193452caccfaf7f601007c1}

Flag. 0 zur Deaktivierung, 1 zur Aktivierung der zuletzt geänderten HTTP-Header.

## Standard {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Vererbt von `default::UseLastModified`, wenn nicht definiert oder leer.

## Verwandte Themen {#section-1536715169da48b0aecc4ab7326c86db}

[Katalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [Vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
