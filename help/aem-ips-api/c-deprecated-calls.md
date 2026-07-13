---
title: Veraltete Aufrufe
description: Aufrufe der Image Production System-API und die zugehörigen Parameter, die in nicht mehr verwendet oder unterstützt werden [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
autotag-review: '2026-05-13T21:03:57.183Z'
TQID: 'https://experienceleague.adobe.com/JLoyXksHQ-LAXXxfY71Dv-FOE0trpt-RzcKcV-Pv96I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 0%

---

# Veraltete Aufrufe{#deprecated-calls}

Aufrufe der Image Production System-API und die zugehörigen Parameter, die nicht mehr verwendet werden.

## Veraltete Aufrufe {#topic-654c0466e6434fe4a95953322255b08c}

Aufrufe der Image Production System-API und die zugehörigen Parameter, die in [!DNL Dynamic Media] nicht mehr verwendet werden.

* `ExcludeMasterVideoFromAVS` - Veraltet von [Datentypen](/help/aem-ips-api/types/c-data-types/c-data-types.md). Durch diesen Parameter wird das primäre Video aus dem adaptiven Videoset ausgeschlossen. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Veraltet von [Vorgänge](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Mit diesem Parameter können Sie ein Medienportalereignis zu IPS hinzufügen.
* `getMediaPortalEvent` - Veraltet von [Vorgänge](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Mit diesem Parameter können Sie Medienportalereignisse abrufen, die bestimmten Kriterien entsprechen.
* `getCdnCacheInvalidationStatus` - Veraltet von [Vorgänge](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Dieser Parameter wird jetzt nicht mehr unterstützt, da der `cdnCacheInvalidation` den Cache fast sofort ungültig macht (~5 Sekunden). Daher ist das Abrufen des Invalidierungsstatus nicht mehr erforderlich.

