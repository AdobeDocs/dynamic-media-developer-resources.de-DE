---
description: Beschreibt neue und geänderte Typen für die IPS-API-Version 6.
solution: Experience Manager
title: Datentypen Neu und Geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
TQID: 'https://experienceleague.adobe.com/LI8xzlS2eACzYqcV3krzThLm77-z6imYLohPRCTHIYs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 1%

---

# Datentypen: Neu und Geändert{#data-types-new-and-modified}

Beschreibt neue und geänderte Typen für die IPS-API-Version 6.

Syntax

## Neue Typen {#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## Geänderte Typen {#section-56b834b1a3b843279d8715b4a4f3890b}

**hinzugefügt**

* `numUrls` zu `UploadUrlsJob` hinzugefügt.

* `fileName` zu `Asset.` hinzugefügt

* `isHidden` zu `MetadataField` hinzugefügt.

* `taskState` zu `TaskProgress` hinzugefügt.

* `exportJob` zu `ActiveJob` und `ScheduledJob` hinzugefügt.

* `optmizedPath` und `optimizedFile` zu `PsdInfo` hinzugefügt.

* `contextHandle` hinzugefügt zu:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Folgende Parameter wurden `Asset` hinzugefügt:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Geändert**

* `User` wurde `role` in `defaultRole` geändert.

* `Folder` wurde `permissions` in `permissionsSetHandle` geändert.

* In `AssetSummary` sind `type` und `name` jetzt optional.

