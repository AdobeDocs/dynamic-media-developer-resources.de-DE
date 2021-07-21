---
description: Enthält Informationen zu Warn- oder Fehlerbedingungen, die während eines Batch-Asset-Vorgangs generiert werden. Die Code- und Begründungsfelder entsprechen den Fehlermeldungsfeldern, die für den entsprechenden Nicht-Batch-Vorgang ausgegeben worden wären.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# AssetOperationFault{#assetoperationfault}

Enthält Informationen zu Warn- oder Fehlerbedingungen, die während eines Batch-Asset-Vorgangs generiert werden. Die Code- und Begründungsfelder entsprechen den Fehlermeldungsfeldern, die für den entsprechenden Nicht-Batch-Vorgang ausgegeben worden wären.

Syntax

## Parameter {#section-c906f052f43e4785ba46d92b514b0923}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Asset-Handle für den fehlgeschlagenen Vorgang. |
| `*`Code`*` | `xsd:int` | Fehlercode des Vorgangs. |
| `*`Grund`*` | `xsd:string` | Fehlerbeschreibung oder Grund. |
