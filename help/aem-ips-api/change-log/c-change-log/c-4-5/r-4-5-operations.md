---
description: Beschreibt neue und geänderte Vorgangsmethoden für die IPS-API-Version 4.5.
solution: Experience Manager
title: Betrieb - Neu und geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
TQID: 'https://experienceleague.adobe.com/n4U8LW8otIaBBDalW1wRJFaweTAw3-0Sh0ckgIEADAI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 100
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

