---
title: AssetOperationFault
description: Enthält Informationen zu Warn- oder Fehlerbedingungen, die während eines Batch-Asset-Vorgangs generiert wurden. Die Code- und Ursachenfelder entsprechen den Feldern der Fehlermeldung, die für den entsprechenden Nicht-Batch-Vorgang ausgelöst worden wären.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
TQID: 'https://experienceleague.adobe.com/LCiMAp-8grDIfCEGX3sF2kBhDamlxZ8iFHT1BjBLkCY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 92
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
