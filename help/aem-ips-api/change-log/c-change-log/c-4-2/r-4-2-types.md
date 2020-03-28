---
description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.2.
seo-description: Beschreibt neue und geänderte Datentypen für die IPS-API-Version 4.2.
seo-title: Datentypen neu und geändert
solution: Experience Manager
title: Datentypen neu und geändert
topic: Scene7 Image Production System API
uuid: 274e49da-9eb8-4082-971c-056acb47a53e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

