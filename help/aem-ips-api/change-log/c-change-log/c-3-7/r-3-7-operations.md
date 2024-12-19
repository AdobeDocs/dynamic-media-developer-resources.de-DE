---
description: Beschreibt neue und geänderte Vorgangsmethoden für die IPS-API-Version 3.7.
solution: Experience Manager
title: Vorgänge Neu und Geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 2%

---

# Vorgänge: Neu und Geändert{#operations-new-and-modified}

Beschreibt neue und geänderte Vorgangsmethoden für die IPS-API-Version 3.7.

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

* `name` Parameter entfernt.
* `excludeFieldArray` hinzugefügt.

**getFolders**

* `excludeFieldArray` hinzugefügt.

**getFolderTree**

* `excludeFieldArray` und `getUniqueMetadataValues` hinzugefügt.
* `fieldHandle` zu einem erforderlichen Parameter gemacht.
