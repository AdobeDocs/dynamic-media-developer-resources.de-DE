---
description: Beschreibt neue und geänderte Vorgangsmethoden für die IPS-API Version 6.
solution: Experience Manager
title: Vorgänge - Neu und geändert
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# Vorgänge: Neu und geändert{#operations-new-and-modified}

Beschreibt neue und geänderte Vorgangsmethoden für die IPS-API Version 6.

Syntax

## Neue Vorgänge {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Geänderte Vorgänge {#section-f4e8755527444266ae806e3f4c851ae6}

**Hinzugefügt**

* `isHidden` und `initialTagValue` wurden hinzugefügt zu:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* `thumbAssetHandle` wurde hinzugefügt zu:

   * `createImageSet`
   * `createAssetSet`

  `companyHandle` wurde hinzugefügt zu:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  `contextHandle` wurde hinzugefügt zu:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* includeInactive wurde hinzugefügt zu:

   * `getUsers`.
   * `getUserChars`.

* `permissionArray` wurde zu `createPropertySet` hinzugefügt.

* `exportJob` wurde zu `submitJob` hinzugefügt.

**Changed**

* In `addUser` und `setUser` wurde `role` in `defaultRole` geändert.

* In `getCompanyMembers` wurde `userArray` in `memberArray` geändert.

* In `getCompanyMembership` wurde `companyArray` in `membershipArray` geändert.

* In `addUser`, `setCompanyMembership` und `addCompanyMembership` wurde `membershipArray` in `companyHandleArray` geändert.

* In `getCompanyMembership` wurde `companyArray` in `membershipArray` geändert.

* In `getUserChars` ist `includeInvalid` jetzt optional.

**Entfernt**

* `renameFiles` wurde aus `renameAsset` entfernt.

* `getXMPPanelViewDefinition` wurde entfernt.
* `searchAssetsByFulltext` und `searchAssetsBySimilarity` entfernt.
