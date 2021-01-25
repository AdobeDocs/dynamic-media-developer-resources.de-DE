---
description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.2.
solution: Experience Manager
title: Datentypen neu und geändert
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 3%

---


# Datentypen: Neu und geändert{#data-types-new-and-modified}

Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.2.

Syntax

## Neue Typen {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## Modifizierte Typen {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**Asset**

hinzugefügte Parameter:

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

Entfernte Parameter:

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

hinzugefügte Parameter:

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

hinzugefügte Parameter:

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

hinzugefügte Parameter:

* `preservePublishState`
* `preserveCrop`

