---
description: Verwenden Sie diese Servereinstellungen für den Bildkatalogdienst.
solution: Experience Manager
title: Bildkatalogdienst
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Bildkatalogdienst{#image-catalog-service}

Verwenden Sie diese Servereinstellungen für den Bildkatalogdienst.

## CS::catalog.rootPath - Ordner des Bildkatalogs {#section-02d107f157384b18835f884f24fea3aa}

Speicherort des Bildkatalogordners (wo alle [!DNL catalog.ini]-Dateien gespeichert sein müssen). Kann ein absoluter Dateipfad oder ein Pfad relativ zum *[!DNL install_folder]* sein. Der Server überwacht diesen Ordner ständig und lädt Kataloge neu, wenn eine neue Hauptkatalogdatei (mit dem Suffix [!DNL .ini] ) erkannt wird oder sich die letzte Änderung einer vorhandenen Hauptkatalogdatei geändert hat.

## CS::catalog.cacheRoot - Catalog Cache Folder {#section-73e499c3a5974f1aa4251e70272ff503}

Der Stammordner für den Cache des Katalogsystems. Kann auf denselben Ordner wie in `PS::cache.rootPaths` gesetzt werden. Der Ordner muss manuell erstellt werden, bevor diese Einstellung geändert wird.

## CS::catalog.modificationWaitTime - Catalog File Parsing Delay {#section-7348065bcc124cb68ea947bf1b9b0845}

Zeit in msec, die der Katalogdienst wartet, nachdem eine [!DNL catalog.ini] -Datei geändert wurde, bis sie die sekundären Katalogdateien lädt. Diese Verzögerung stellt sicher, dass alle sekundären Katalogdateien auf dem neuesten Stand sind, bevor der Katalogdienst versucht, sie zu laden. Ganzzahlwert in msec.

## CS::catalog.refreshInterval - Häufigkeit der Katalogdateiüberprüfung {#section-517fefc1d8784777a1026abec8630d58}

Häufigkeit, mit der der Katalogdienst nach Änderungen an Bildkatalogen sucht. Ganzzahlwert in msec.
