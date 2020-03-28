---
description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 6.
seo-description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 6.
seo-title: Vorgänge - Neu und geändert
solution: Experience Manager
title: Vorgänge - Neu und geändert
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Vorgänge: Neu und geändert{#operations-new-and-modified}

Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 6.

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

* Hinzugefügt `isHidden` und `initialTagValue` zu:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Hinzugefügt `thumbAssetHandle` zu:

   * `createImageSet`
   * `createAssetSet`
   Hinzugefügt `companyHandle` zu:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`
   Hinzugefügt `contextHandle` zu:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* includeInactive wurde hinzugefügt zu:

   * `getUsers`.
   * `getUserChars`.

* Hinzugefügt `permissionArray` zu `createPropertySet`.

* Hinzugefügt `exportJob` zu `submitJob`.

**Geändert**

* In `addUser` und `setUser`, geändert `role` in `defaultRole`.

* In `getCompanyMembers`, geändert `userArray` zu `memberArray`.

* In `getCompanyMembership`, geändert `companyArray` zu `membershipArray`.

* In `addUser`, `setCompanyMembership`und `addCompanyMembership`, geändert `membershipArray` zu `companyHandleArray`.

* In `getCompanyMembership`, geändert `companyArray` zu `membershipArray`.

* In `getUserChars`ist `includeInvalid` jetzt optional.

**Entfernt**

* Entfernt `renameFiles` von `renameAsset`.

* Removed `getXMPPanelViewDefinition`.
* Entfernt `searchAssetsByFulltext` und `searchAssetsBySimilarity`.

