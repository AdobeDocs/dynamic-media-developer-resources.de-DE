---
description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.8.
seo-description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.8.
seo-title: Vorgänge - Neu und geändert
solution: Experience Manager
title: Vorgänge - Neu und geändert
topic: Scene7 Image Production System API
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Vorgänge: Neu und geändert{#operations-new-and-modified}

Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.8.

Syntax

## Neue Vorgänge {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## Geänderte Vorgänge {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* Mit dem optionalen `publishState` Parameter können Sie nach dem Status des `MarkedForPublish/NotMarkedForPublish` Assets suchen.

**getJobLogs**

* Mit dem optionalen `userHandle` Parameter können Sie Auftragsprotokolle abrufen, die von einem bestimmten Benutzer gesendet wurden.

