---
description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.5.
seo-description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.5.
seo-title: Datentypen neu und geändert
solution: Experience Manager
title: Datentypen neu und geändert
topic: Scene7 Image Production System API
uuid: 2752f9dd-ec47-45d6-a465-6d275ec2b2fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

* Asset enthält ein neues `fileName` Feld, das den Namen der virtuellen Datei zurückgibt.
* `AssetSummary` gibt ein `type` und `name` -Feld zurück

* `MetadataField` beinhaltet `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` benötigt eine `urlArray` und fügt eine optionale `numUrls` Anzahl hinzu

