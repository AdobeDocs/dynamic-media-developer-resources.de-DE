---
description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 4.5.
seo-description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 4.5.
seo-title: Vorgänge - Neu und geändert
solution: Experience Manager
title: Vorgänge - Neu und geändert
topic: Scene7 Image Production System API
uuid: c4002670-c830-474e-bb84-343f76b6fb80
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

## Geänderte Vorgänge {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` enthält `animatedGifInfo`, `swcInfo`, `cssInfo`und `javascriptInfo` Parameter.

* `createMetadataField` enthält einen optionalen `isHidden` Parameter.

* `saveMetadataField` enthält einen optionalen `isHidden` Parameter.

* `searchAssets`
* 
* Der `renameFiles` Parameter wurde für frühere Versionen nicht mehr unterstützt und aus dem `renameAsset` Vorgang entfernt. Der Pfad der virtuellen Datei wird an den Namen des neuen Assets angepasst (unter Beibehaltung der Dateierweiterung), während die physischen Dateipfade nicht betroffen sind. API-Clients müssen Verweise auf diesen Parameter bei der Aktualisierung auf die neue API-Version entfernen.

