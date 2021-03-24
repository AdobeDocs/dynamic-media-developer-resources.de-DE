---
description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 3.8.
solution: Experience Manager
title: Vorgänge - Neu und geändert
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
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

