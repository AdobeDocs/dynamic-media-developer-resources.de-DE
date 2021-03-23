---
title: Veraltete Aufrufe
description: API-Aufrufe des Image Production Systems und zugehörige Parameter, die nicht mehr in Dynamic Media verwendet werden.
solution: Experience Manager
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# Veraltete Aufrufe{#deprecated-calls}

API-Aufrufe des Image Production Systems und zugehörige Parameter, die nicht mehr verwendet werden.

## Veraltete Aufrufe {#topic-654c0466e6434fe4a95953322255b08c}

API-Aufrufe des Image Production Systems und zugehörige Parameter, die nicht mehr in Dynamic Media verwendet werden.

* `addMediaPortalEvent` - Veraltet von Vorgängen. Mit diesem Aufruf können Sie ein Media Portal-Ereignis zum IPS hinzufügen.
* `getMediaPortalEvent` - Veraltet von Vorgängen. Mit diesem Aufruf können Sie Media Portal-Ereignis abrufen, die bestimmten Kriterien entsprechen.
* `getCdnCacheInvalidationStatus` - Veraltet von Vorgängen. Diese API wird jetzt nicht mehr unterstützt, da die API `cdnCacheInvalidation` den Cache fast sofort ungültig macht (~5 Sekunden). Daher ist eine Abfrage nach dem Ungültigkeitsstatus nicht mehr erforderlich.

