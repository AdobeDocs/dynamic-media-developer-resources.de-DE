---
description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.2.
solution: Experience Manager
title: Datentypen neu und geändert
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
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

