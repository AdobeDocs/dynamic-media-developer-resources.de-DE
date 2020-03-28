---
description: Beschreibt neue und geänderte Typen für die IPS-API Version 6.
seo-description: Beschreibt neue und geänderte Typen für die IPS-API Version 6.
seo-title: Datentypen neu und geändert
solution: Experience Manager
title: Datentypen neu und geändert
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

## Modifizierte Typen {#section-56b834b1a3b843279d8715b4a4f3890b}

**Hinzugefügt**

* Hinzugefügt `numUrls` zu `UploadUrlsJob`.

* Hinzugefügt `fileName` zu `Asset.`

* Hinzugefügt `isHidden` zu `MetadataField`.

* Hinzugefügt `taskState` zu `TaskProgress`.

* Hinzugefügt `exportJob` zu `ActiveJob` und `ScheduledJob`.

* Hinzugefügt `optmizedPath` und `optimizedFile` zu `PsdInfo`.

* Hinzugefügt `contextHandle` zu:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Folgende Parameter wurden hinzugefügt `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Geändert**

* In `User`, geändert `role` zu `defaultRole`.

* In `Folder`, geändert `permissions` zu `permissionsSetHandle`.

* In `AssetSummary`, `type` und `name` sind jetzt optional.

