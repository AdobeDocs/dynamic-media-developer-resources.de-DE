---
title: Veraltete Aufrufe
description: Aufrufe der Image Production System-API und die zugehörigen Parameter, die in nicht mehr verwendet oder unterstützt werden [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '124'
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
