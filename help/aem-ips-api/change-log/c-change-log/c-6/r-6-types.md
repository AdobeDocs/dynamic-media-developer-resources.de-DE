---
description: Beschreibt neue und geänderte Typen für die IPS-API-Version 6.
solution: Experience Manager
title: Datentypen Neu und Geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '71'
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
