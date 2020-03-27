---
description: Verwenden Sie diese Servereinstellungen für den Bildkatalogdienst.
seo-description: Verwenden Sie diese Servereinstellungen für den Bildkatalogdienst.
seo-title: Bildkatalogdienst
solution: Experience Manager
title: Bildkatalogdienst
topic: Scene7 Image Serving - Image Rendering API
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Bildkatalogdienst{#image-catalog-service}

Verwenden Sie diese Servereinstellungen für den Bildkatalogdienst.

## CS::catalog.rootPath - Bildkatalogordner {#section-02d107f157384b18835f884f24fea3aa}

Speicherort des Bildkatalogordners (in dem sich alle [!DNL catalog.ini] Dateien befinden müssen). Kann ein absoluter Dateipfad oder ein Pfad relativ zum *[!DNL install_folder]* Pfad sein. Der Server überwacht diesen Ordner kontinuierlich und lädt Kataloge, wenn eine neue Hauptkatalogdatei (mit [!DNL .ini] Dateisuffix) erkannt wird oder sich die letzte geänderte Zeit einer vorhandenen Hauptkatalogdatei geändert hat.

## CS::catalog.cacheRoot - Katalogcache-Ordner {#section-73e499c3a5974f1aa4251e70272ff503}

Der Stammordner für den Cache des Katalogsystems. Kann auf denselben Ordner wie in einem der Ordner in `PS::cache.rootPaths`festgelegt werden. Der Ordner muss manuell erstellt werden, bevor diese Einstellung geändert wird.

## CS::catalog.modificationWaitTime - Verzögerung bei der Analyse von Katalogdateien {#section-7348065bcc124cb68ea947bf1b9b0845}

Zeit in msec wartet der Katalogdienst, nachdem eine [!DNL catalog.ini] Datei geändert wurde, bis die sekundären Katalogdateien geladen wurden. Diese Verzögerung stellt sicher, dass alle sekundären Katalogdateien auf dem neuesten Stand sind, bevor der Katalogdienst versucht, sie zu laden. Ganzzahlwert in msec.

## CS::catalog.refreshInterval - Häufigkeit der Katalogdateiprüfung {#section-517fefc1d8784777a1026abec8630d58}

Häufigkeit, mit der der Katalogdienst nach Änderungen an Bildkatalogen sucht. Ganzzahlwert in msec.
