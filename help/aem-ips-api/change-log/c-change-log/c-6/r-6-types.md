---
description: Beschreibt neue und geänderte Typen für die IPS-API Version 6.
solution: Experience Manager
title: Neue und geänderte Datentypen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 1%

---

# Datentypen: Neu und geändert{#data-types-new-and-modified}

Beschreibt neue und geänderte Typen für die IPS-API Version 6.

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

**Hinzugefügt**

* `numUrls` zu `UploadUrlsJob` hinzugefügt.

* `fileName` zu `Asset.` hinzugefügt

* `isHidden` zu `MetadataField` hinzugefügt.

* `taskState` zu `TaskProgress` hinzugefügt.

* `exportJob` zu `ActiveJob` und `ScheduledJob` hinzugefügt.

* `optmizedPath` und `optimizedFile` wurden zu `PsdInfo` hinzugefügt.

* `contextHandle` hinzugefügt zu:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Die folgenden Parameter wurden zu `Asset` hinzugefügt:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Geändert**

* In `User` wurde `role` in `defaultRole` geändert.

* In `Folder` wurde `permissions` in `permissionsSetHandle` geändert.

* In `AssetSummary` sind `type` und `name` jetzt optional.
