---
description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.5.
solution: Experience Manager
title: Datentypen Neu und Geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
TQID: 'https://experienceleague.adobe.com/F5YaUftY3yP7VaDh3g6-SiCfetzEciXwFGS5to3Ux-0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 62
ht-degree: 1%

---

# Datentypen: Neu und Geändert{#data-types-new-and-modified}

Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.5.

Syntax

## Neue Typen {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## Geänderte Typen {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* Asset enthält ein neues `fileName`, das den Namen der virtuellen Datei zurückgibt.
* `AssetSummary` gibt ein `type`- und `name` zurück

* `MetadataField` umfasst `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` erfordert eine `urlArray` und fügt eine optionale `numUrls` hinzu

