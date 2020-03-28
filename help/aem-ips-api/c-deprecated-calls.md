---
description: API-Aufrufe des Image Production Systems und zugehörige Parameter, die nicht mehr verwendet werden.
seo-description: API-Aufrufe des Image Production Systems und zugehörige Parameter, die nicht mehr verwendet werden.
seo-title: Veraltete Aufrufe
solution: Experience Manager
title: Veraltete Aufrufe
topic: Scene7 Image Production System API
uuid: 03925728-f011-45f0-84a6-808dff0fd529
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Veraltete Aufrufe{#deprecated-calls}

API-Aufrufe des Image Production Systems und zugehörige Parameter, die nicht mehr verwendet werden.

## Veraltete Aufrufe {#topic-654c0466e6434fe4a95953322255b08c}

API-Aufrufe des Image Production Systems und zugehörige Parameter, die nicht mehr verwendet werden.

* `addMediaPortalEvent` - Veraltet von Vorgängen. Mit diesem Aufruf können Sie ein Media Portal-Ereignis zum IPS hinzufügen.
* `getMediaPortalEvent` - Veraltet von Vorgängen. Mit diesem Aufruf können Sie Media Portal-Ereignis abrufen, die bestimmten Kriterien entsprechen.
* `getCdnCacheInvalidationStatus` - Veraltet von Vorgängen. Diese API wird jetzt nicht mehr unterstützt, da die `cdnCacheInvalidation` API den Cache fast sofort ungültig macht (~5 Sekunden). Daher ist eine Abfrage nach dem Ungültigkeitsstatus nicht mehr erforderlich.

