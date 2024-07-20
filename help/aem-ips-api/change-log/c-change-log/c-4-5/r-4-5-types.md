---
description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.5.
solution: Experience Manager
title: Neue und geänderte Datentypen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# Datentypen: neu und geändert{#data-types-new-and-modified}

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

* Das Asset enthält ein neues `fileName` -Feld, das den Namen der virtuellen Datei zurückgibt.
* `AssetSummary` gibt ein Feld `type` und `name` zurück

* `MetadataField` enthält `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` erfordert eine `urlArray` und fügt eine optionale `numUrls` Anzahl hinzu
