---
description: Verwenden Sie diese Servereinstellungen für den Bildkatalogdienst.
solution: Experience Manager
title: Bildkatalogdienst
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Bildkatalogdienst{#image-catalog-service}

Verwenden Sie diese Servereinstellungen für den Bildkatalogdienst.

## CS::catalog.rootPath - Bildkatalogordner {#section-02d107f157384b18835f884f24fea3aa}

Speicherort des Bildkatalogordners (in dem sich alle [!DNL catalog.ini]-Dateien befinden müssen). Kann ein absoluter Dateipfad oder ein Pfad relativ zum *[!DNL install_folder]* sein. Der Server überwacht diesen Ordner kontinuierlich und lädt Kataloge, wenn eine neue Hauptkatalogdatei (mit dem Suffix [!DNL .ini]) erkannt wird oder sich die letzte geänderte Zeit einer vorhandenen Hauptkatalogdatei geändert hat.

## CS::catalog.cacheRoot - Katalog-Cache-Ordner {#section-73e499c3a5974f1aa4251e70272ff503}

Der Stammordner für den Cache des Katalogsystems. Kann auf denselben Ordner wie in `PS::cache.rootPaths` eingestellt werden. Der Ordner muss manuell erstellt werden, bevor diese Einstellung geändert wird.

## CS::catalog.modificationWaitTime - Catalog File Parsing Delay {#section-7348065bcc124cb68ea947bf1b9b0845}

Zeit in msec wartet der Katalogdienst, nachdem eine [!DNL catalog.ini]-Datei geändert wurde, bis die sekundären Katalogdateien geladen wurden. Diese Verzögerung stellt sicher, dass alle sekundären Katalogdateien auf dem neuesten Stand sind, bevor der Katalogdienst versucht, sie zu laden. Ganzzahlwert in msec.

## CS::catalog.refreshInterval - Häufigkeit der Katalogdateiprüfung {#section-517fefc1d8784777a1026abec8630d58}

Häufigkeit, mit der der Katalogdienst nach Änderungen an Bildkatalogen sucht. Ganzzahlwert in msec.
