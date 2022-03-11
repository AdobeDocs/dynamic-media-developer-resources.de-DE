---
description: Beschreibt neue und geänderte Betriebsmethoden für die IPS-API Version 4.5.
solution: Experience Manager
title: Vorgänge - Neu und geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---

# Vorgänge: Neu und geändert{#operations-new-and-modified}

Beschreibt neue und geänderte Betriebsmethoden für die IPS-API Version 4.5.

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

* `Asset` include `animatedGifInfo`, `swcInfo`, `cssInfo`und `javascriptInfo` Parameter.
* `createMetadataField` enthält ein optionales `isHidden` Parameter.
* `saveMetadataField` enthält ein optionales `isHidden` Parameter.
* `searchAssets`
* Die `renameFiles` -Parameter wurde für frühere Versionen nicht mehr unterstützt und aus der `renameAsset` Vorgang. Der virtuelle Dateipfad wird so geändert, dass er mit dem neuen Asset-Namen übereinstimmt (wobei die Dateierweiterung beibehalten wird), während die physischen Dateipfade nicht betroffen sind. API-Clients müssen beim Aktualisieren auf die neue API-Version Verweise auf diesen Parameter entfernen.
