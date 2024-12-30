---
description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.2.
solution: Experience Manager
title: Datentypen Neu und Geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 1%

---

# Datentypen: Neu und Geändert{#data-types-new-and-modified}

Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.2.

Syntax

## Neue Typen {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## Geänderte Typen {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**Asset**

Parameter hinzugefügt:

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

Entfernte Parameter:

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

Parameter hinzugefügt:

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

Parameter hinzugefügt:

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

Parameter hinzugefügt:

* `preservePublishState`
* `preserveCrop`
