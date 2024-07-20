---
description: Diese neuen oder modifizierten Vorgänge und Datentypen, die in der Beta-WSDL verfügbar sind, dürfen außerhalb der von Dynamic Media entwickelten Anwendungen nicht verwendet werden.
solution: Experience Manager
title: Eingeschränkte Verwendung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Eingeschränkte Verwendung{#restricted-use}

Diese neuen oder modifizierten Vorgänge und Datentypen, die in der Beta-WSDL verfügbar sind, dürfen außerhalb der von Dynamic Media entwickelten Anwendungen nicht verwendet werden.

Diese Vorgänge und Typen können bei nachfolgenden Systemaktualisierungen deaktiviert, geändert oder eingestellt werden.

**Neue Typen**

* AssetPublishContexts
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**Neue Vorgänge**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsByÄhnarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Modifizierte Typen**

* `ActiveJob` wurde geändert, um den Typ `createVideoSitemapJob` einzuschließen

* `ScheduledJob` wurde geändert, um den Typ `createVideoSitemapJob` einzuschließen

* `ImageServingPublishJob` wurde geändert, um einen optionalen `contextHandle` einzuschließen.

* `ImageRenderingPublishJob` wurde geändert, um einen optionalen `contextHandle` einzuschließen.

* `MetadataField` wurde geändert, um einen optionalen `initialTagField` einzuschließen.

* `MetadataCondition` wurde zum Einschließen und optionalen Parameter `caseSensitive` geändert

* `PropertySet` wurde geändert, um eine optionale `PermissionArray` als `permissions` einzuschließen

* `UploadDirectoryJob` wurde geändert, um optionale Parameter `xmpKeywords`, `xmpTemplateId` und `xmpTemplateOverride` einzuschließen.

* `VideoPublishJob` wurde geändert, um einen optionalen `contextHandle` einzuschließen.

**Modifizierte Vorgänge**

* `createAssetSet` wurde geändert, um einen optionalen `thumbAssetHandle` einzuschließen.

* `createImageSet` wurde geändert, um einen optionalen `thumbAssetHandle` einzuschließen.

* `createMetadataField` wurde geändert, um einen optionalen `initialTagValue` -Parameter einzuschließen

* `createPropertySet` wurde geändert, um eine optionale `PermissionUpdateArray` als `permissionArray` einzuschließen

* `getImageServingPublishSettings` wurde geändert, um einen optionalen `contextHandle` -Parameter einzuschließen

* `getImageRenderingPublishSettings` wurde geändert, um einen optionalen `contextHandle` -Parameter einzuschließen

* `searchAssetsByFullText` wurde geändert, um eine Reihe optionaler Parameter einzuschließen:

   * `SearchFilter` als `filters` Parameter

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata` wurde geändert, um eine Reihe optionaler Parameter einzuschließen:

   * `SearchFilter` als `filters` Parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` Sequenz von sieben Parametern

* `setAssetPublishState` wurde geändert, um eine optionale `HandleArray` als `contextHandleArray` einzuschließen

* `setImageServingPublishSettings` wurde geändert, um einen optionalen `contextHandle` -Parameter einzuschließen

* `setImageRenderingPublishSettings` wurde geändert, um einen optionalen `contextHandle`Parameter einzuschließen

* `submitJob` wurde geändert, um einen optionalen `createVideoSitemap` Auftragstyp einzuschließen
