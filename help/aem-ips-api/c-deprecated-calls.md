---
title: Veraltete Aufrufe
description: API-Aufrufe des Bildproduktionssystems und die zugehörigen Parameter, die nicht mehr in Dynamic Media verwendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# Veraltete Aufrufe{#deprecated-calls}

API-Aufrufe des Bildproduktionssystems und die zugehörigen Parameter, die nicht mehr verwendet werden.

## Veraltete Aufrufe {#topic-654c0466e6434fe4a95953322255b08c}

API-Aufrufe des Bildproduktionssystems und die zugehörigen Parameter, die nicht mehr in Dynamic Media verwendet werden.

* `addMediaPortalEvent` - Veraltet von Vorgängen. Mit diesem Aufruf können Sie ein Media Portal-Ereignis zu IPS hinzufügen.
* `getMediaPortalEvent` - Veraltet von Vorgängen. Mit diesem Aufruf können Sie Medienportal-Ereignisse abrufen, die bestimmten Kriterien entsprechen.
* `getCdnCacheInvalidationStatus` - Veraltet von Vorgängen. Diese API wird jetzt nicht mehr unterstützt, da die `cdnCacheInvalidation`-API den Cache fast sofort ungültig macht (~5 Sekunden). Daher ist eine Abfrage zum Invalidierungsstatus nicht mehr erforderlich.
