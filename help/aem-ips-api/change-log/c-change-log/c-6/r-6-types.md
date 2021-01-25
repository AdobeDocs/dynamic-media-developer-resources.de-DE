---
description: Beschreibt neue und geänderte Typen für die IPS-API Version 6.
solution: Experience Manager
title: Datentypen neu und geändert
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '69'
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

## Modifizierte Typen {#section-56b834b1a3b843279d8715b4a4f3890b}

**Hinzugefügt**

* `numUrls` zu `UploadUrlsJob` hinzugefügt.

* `fileName` zu `Asset.` hinzugefügt

* `isHidden` zu `MetadataField` hinzugefügt.

* `taskState` zu `TaskProgress` hinzugefügt.

* `exportJob` zu `ActiveJob` und `ScheduledJob` hinzugefügt.

* `optmizedPath` und `optimizedFile` zu `PsdInfo` hinzugefügt.

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

