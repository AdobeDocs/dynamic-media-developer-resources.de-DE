---
description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.8.
seo-description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.8.
seo-title: Vorgänge - Neu und geändert
solution: Experience Manager
title: Vorgänge - Neu und geändert
topic: Dynamic Media Image Production System API
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

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

## Modifizierte Vorgänge {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* Mit dem optionalen Parameter `publishState` können Sie nach dem Asset-Status `MarkedForPublish/NotMarkedForPublish` suchen.

**getJobLogs**

* Mit dem optionalen Parameter `userHandle` können Sie Auftragsprotokolle abrufen, die von einem bestimmten Benutzer gesendet wurden.

