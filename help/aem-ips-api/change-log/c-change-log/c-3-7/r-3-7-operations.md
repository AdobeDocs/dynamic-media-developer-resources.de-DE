---
description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.7.
seo-description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.7.
seo-title: Vorgänge - Neu und geändert
solution: Experience Manager
title: Vorgänge - Neu und geändert
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Vorgänge: Neu und geändert{#operations-new-and-modified}

Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.7.

Syntax

## Neue Vorgänge {#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## Geänderte Vorgänge {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* Der `name` Parameter wurde entfernt.
* Added `excludeFieldArray`.

**getFolders**

* Added `excludeFieldArray`.

**getFolderTree**

* Hinzugefügt `excludeFieldArray` und `getUniqueMetadataValues`.
* Es wurde `fieldHandle` ein erforderlicher Parameter erstellt.

