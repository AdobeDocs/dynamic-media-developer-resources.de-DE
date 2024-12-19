---
description: Beschreibt neue und geänderte Vorgangsmethoden für die IPS-API-Version 4.5.
solution: Experience Manager
title: Betrieb - Neu und geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---

# Vorgänge: Neu und Geändert{#operations-new-and-modified}

Beschreibt neue und geänderte Vorgangsmethoden für die IPS-API-Version 4.5.

Syntax

## Neue Vorgänge {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## Geänderte Vorgänge {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` umfasst `animatedGifInfo`-, `swcInfo`-, `cssInfo`- und `javascriptInfo`.
* `createMetadataField` enthält einen optionalen `isHidden`.
* `saveMetadataField` enthält einen optionalen `isHidden`.
* `searchAssets`
* Der `renameFiles`-Parameter wird seit früheren Versionen nicht mehr unterstützt und aus dem `renameAsset` entfernt. Der virtuelle Dateipfad wird geändert, sodass er dem neuen Asset-Namen entspricht (wobei die Dateierweiterung beibehalten wird), während die physischen Dateipfade nicht betroffen sind. API-Clients müssen Verweise auf diesen Parameter entfernen, wenn sie auf die neue API-Version aktualisieren.
