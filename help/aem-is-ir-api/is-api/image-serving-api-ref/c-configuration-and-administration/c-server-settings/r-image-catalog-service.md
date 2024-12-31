---
description: Verwenden Sie diese Server-Einstellungen für den Bildkatalog-Service.
solution: Experience Manager
title: Bildkatalog-Service
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Bildkatalog-Service{#image-catalog-service}

Verwenden Sie diese Server-Einstellungen für den Bildkatalog-Service.

## CS:catalog.rootPath - Bildkatalogordner {#section-02d107f157384b18835f884f24fea3aa}

Speicherort des Bildkatalogordners (in dem sich alle [!DNL catalog.ini] befinden müssen). Kann ein absoluter Dateipfad oder ein Pfad relativ zum *[!DNL install_folder]* sein. Der Server überwacht diesen Ordner kontinuierlich und lädt oder lädt Kataloge neu, wenn eine neue Hauptkatalogdatei (mit [!DNL .ini] Dateisuffix) erkannt wird oder wenn die letzte Änderungszeit einer vorhandenen Hauptkatalogdatei geändert wurde.

## CS::catalog.cacheRoot - Ordner des Katalog-Caches {#section-73e499c3a5974f1aa4251e70272ff503}

Der Stammordner für den Cache des Katalogsystems. Kann auf denselben Ordner wie einer der Ordner in `PS::cache.rootPaths` festgelegt werden. Der Ordner muss manuell erstellt werden, bevor diese Einstellung geändert wird.

## CS::catalog.modifiedWaitTime - Analyseverzögerung der Katalogdatei {#section-7348065bcc124cb68ea947bf1b9b0845}

Die Zeit in ms, die der Katalog-Service nach dem Ändern einer [!DNL catalog.ini] wartet, bis die sekundären Katalogdateien geladen werden. Diese Verzögerung hilft sicherzustellen, dass alle sekundären Katalogdateien auf dem neuesten Stand sind, bevor der Katalog-Service versucht, sie zu laden. Ganzzahliger Wert in ms.

## CS::catalog.refreshInterval - Häufigkeit der Überprüfung der Katalogdatei {#section-517fefc1d8784777a1026abec8630d58}

Häufigkeit, mit der der Katalog-Service nach Änderungen an Bildkatalogen sucht. Ganzzahliger Wert in ms.
