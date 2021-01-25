---
description: Beschreibt neue und geänderte Methoden für Vorgänge für die IPS-API Version 6.
solution: Experience Manager
title: Vorgänge - Neu und geändert
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 1%

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

## Modifizierte Vorgänge {#section-f4e8755527444266ae806e3f4c851ae6}

**Hinzugefügt**

* `isHidden` und `initialTagValue` wurden hinzugefügt zu:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* `thumbAssetHandle` hinzugefügt zu:

   * `createImageSet`
   * `createAssetSet`

   `companyHandle` hinzugefügt zu:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   `contextHandle` hinzugefügt zu:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* includeInactive wurde hinzugefügt zu:

   * `getUsers`.
   * `getUserChars`.

* `permissionArray` zu `createPropertySet` hinzugefügt.

* `exportJob` zu `submitJob` hinzugefügt.

**Geändert**

* In `addUser` und `setUser` wurde `role` in `defaultRole` geändert.

* In `getCompanyMembers` wurde `userArray` in `memberArray` geändert.

* In `getCompanyMembership` wurde `companyArray` in `membershipArray` geändert.

* In `addUser`, `setCompanyMembership` und `addCompanyMembership` wurde `membershipArray` in `companyHandleArray` geändert.

* In `getCompanyMembership` wurde `companyArray` in `membershipArray` geändert.

* In `getUserChars` ist `includeInvalid` jetzt optional.

**Entfernt**

* `renameFiles` aus `renameAsset` entfernt.

* `getXMPPanelViewDefinition` entfernt.
* `searchAssetsByFulltext` und `searchAssetsBySimilarity` entfernt.

