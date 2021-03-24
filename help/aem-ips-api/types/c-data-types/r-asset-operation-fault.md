---
description: Enthält Informationen zu Warn- oder Fehlerbedingungen, die während eines Batch-Asset-Vorgangs generiert wurden. Die Felder Code und Grund entsprechen den Feldern der Fehlermeldung, die für den entsprechenden Nicht-Batch-Vorgang ausgegeben wurden.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

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

