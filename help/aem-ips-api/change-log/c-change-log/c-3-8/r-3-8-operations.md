---
description: Beschreibt neue und geänderte Vorgangsmethoden für die IPS-API-Version 3.8.
solution: Experience Manager
title: Vorgänge Neu und Geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# Vorgänge: Neu und Geändert{#operations-new-and-modified}

Beschreibt neue und geänderte Vorgangsmethoden für die IPS-API-Version 3.8.

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

* Mit dem optionalen `publishState` können Sie nach dem `MarkedForPublish/NotMarkedForPublish` Asset-Status suchen.

**getJobLogs**

* Mit dem optionalen `userHandle` können Sie Vorgangslogs abrufen, die von einem bestimmten Benutzer gesendet wurden.
