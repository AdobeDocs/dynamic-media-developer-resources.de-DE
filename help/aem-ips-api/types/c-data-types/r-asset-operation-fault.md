---
title: AssetOperationFault
description: Enthält Informationen zu Warn- oder Fehlerbedingungen, die während eines Batch-Asset-Vorgangs generiert wurden. Die Code- und Ursachenfelder entsprechen den Feldern der Fehlermeldung, die für den entsprechenden Nicht-Batch-Vorgang ausgelöst worden wären.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 7%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

Enthält Informationen zu Warn- oder Fehlerbedingungen, die während eines Batch-Asset-Vorgangs generiert wurden. Die Code- und Ursachenfelder entsprechen den Feldern der Fehlermeldung, die für den entsprechenden Nicht-Batch-Vorgang ausgelöst worden wären.

Syntax

## Parameter {#section-c906f052f43e4785ba46d92b514b0923}

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Asset-Handle für den fehlgeschlagenen Vorgang. |
| Code | `xsd:int` | Betriebsfehlercode. |
| Grund | `xsd:string` | Fehlerbeschreibung oder -ursache |
