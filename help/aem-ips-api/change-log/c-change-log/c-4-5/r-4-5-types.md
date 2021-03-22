---
description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.5.
solution: Experience Manager
title: Datentypen neu und geändert
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 2%

---


# Datentypen: Neu und geändert{#data-types-new-and-modified}

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

## Modifizierte Typen {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* Asset enthält ein neues `fileName`-Feld, das den Namen der virtuellen Datei zurückgibt.
* `AssetSummary` gibt ein  `type` und- `name` Feld zurück

* `MetadataField` beinhaltet `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` benötigt eine  `urlArray` und fügt eine optionale  `numUrls` Anzahl hinzu

