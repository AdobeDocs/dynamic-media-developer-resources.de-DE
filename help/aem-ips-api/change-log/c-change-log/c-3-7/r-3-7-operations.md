---
description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.7.
solution: Experience Manager
title: Vorgänge - Neu und geändert
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 1%

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

## Modifizierte Vorgänge {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* Der Parameter `name` wurde entfernt.
* `excludeFieldArray` hinzugefügt.

**getFolders**

* `excludeFieldArray` hinzugefügt.

**getFolderTree**

* `excludeFieldArray` und `getUniqueMetadataValues` hinzugefügt.
* Es wurde `fieldHandle` ein erforderlicher Parameter erstellt.

