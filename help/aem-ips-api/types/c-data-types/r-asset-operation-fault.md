---
description: Enthält Informationen zu Warn- oder Fehlerbedingungen, die während eines Batch-Asset-Vorgangs generiert wurden. Die Felder Code und Grund entsprechen den Feldern der Fehlermeldung, die für den entsprechenden Nicht-Batch-Vorgang ausgegeben wurden.
seo-description: Enthält Informationen zu Warn- oder Fehlerbedingungen, die während eines Batch-Asset-Vorgangs generiert wurden. Die Felder Code und Grund entsprechen den Feldern der Fehlermeldung, die für den entsprechenden Nicht-Batch-Vorgang ausgegeben wurden.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 5%

---


# AssetOperationFault{#assetoperationfault}

Enthält Informationen zu Warn- oder Fehlerbedingungen, die während eines Batch-Asset-Vorgangs generiert wurden. Die Felder Code und Grund entsprechen den Feldern der Fehlermeldung, die für den entsprechenden Nicht-Batch-Vorgang ausgegeben wurden.

Syntax

## Parameter {#section-c906f052f43e4785ba46d92b514b0923}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Asset-Handle für den fehlgeschlagenen Vorgang. |
| `*`Code`*` | `xsd:int` | Betriebsfehlercode. |
| `*`Grund`*` | `xsd:string` | Fehlerbeschreibung oder Grund. |

