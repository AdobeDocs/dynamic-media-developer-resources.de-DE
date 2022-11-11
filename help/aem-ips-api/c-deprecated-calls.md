---
title: Veraltete Aufrufe
description: API-Aufrufe des Bildproduktionssystems und die zugehörigen Parameter, die in [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Veraltete Aufrufe{#deprecated-calls}

API-Aufrufe des Bildproduktionssystems und die zugehörigen Parameter, die nicht mehr verwendet werden.

## Veraltete Aufrufe {#topic-654c0466e6434fe4a95953322255b08c}

API-Aufrufe des Bildproduktionssystems und die zugehörigen Parameter, die nicht mehr in [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - Veraltet von [Datentypen](/help/aem-ips-api/types/c-data-types/c-data-types.md). Dieser Parameter hat das Primärvideo aus dem adaptiven Videoset ausgeschlossen. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Veraltet von [Aktivitäten](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Mit diesem Parameter können Sie ein Media Portal-Ereignis zu IPS hinzufügen.
* `getMediaPortalEvent` - Veraltet von [Aktivitäten](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Mit diesem Parameter können Sie Medienportal-Ereignisse abrufen, die bestimmten Kriterien entsprechen.
* `getCdnCacheInvalidationStatus` - Veraltet von [Aktivitäten](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Dieser Parameter wird jetzt nicht mehr unterstützt, da die Variable `cdnCacheInvalidation` -Parameter macht den Cache fast sofort ungültig (~5 Sekunden). Daher ist eine Abfrage zum Invalidierungsstatus nicht mehr erforderlich.
