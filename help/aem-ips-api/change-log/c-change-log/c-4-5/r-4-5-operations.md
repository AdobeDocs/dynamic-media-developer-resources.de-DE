---
description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 4.5.
solution: Experience Manager
title: Vorgänge - Neu und geändert
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---


# Vorgänge: Neu und geändert{#operations-new-and-modified}

Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 4.5.

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

## Modifizierte Vorgänge {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` enthält  `animatedGifInfo`,  `swcInfo`,  `cssInfo`und  `javascriptInfo` Parameter.

* `createMetadataField` enthält einen optionalen  `isHidden` Parameter.

* `saveMetadataField` enthält einen optionalen  `isHidden` Parameter.

* `searchAssets`
* 
* Der Parameter `renameFiles` wurde für frühere Versionen nicht mehr unterstützt und aus dem Vorgang `renameAsset` entfernt. Der Pfad der virtuellen Datei wird an den Namen des neuen Assets angepasst (unter Beibehaltung der Dateierweiterung), während die physischen Dateipfade nicht betroffen sind. API-Clients müssen Verweise auf diesen Parameter bei der Aktualisierung auf die neue API-Version entfernen.

