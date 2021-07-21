---
description: Diese neuen oder modifizierten Vorgänge und Datentypen, die in der Beta-WSDL verfügbar sind, dürfen außerhalb der von Dynamic Media entwickelten Anwendungen nicht verwendet werden.
solution: Experience Manager
title: Eingeschränkte Verwendung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '237'
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

**Geänderte Typen**

* `ActiveJob` wurde geändert, um einen `createVideoSitemapJob`-Typ einzuschließen

* `ScheduledJob` wurde geändert, um einen `createVideoSitemapJob`-Typ einzuschließen

* `ImageServingPublishJob` wurde geändert, um ein optionales `contextHandle` einzuschließen.

* `ImageRenderingPublishJob` wurde geändert, um ein optionales `contextHandle` einzuschließen.

* `MetadataField` wurde geändert, um ein optionales `initialTagField` einzuschließen.

* `MetadataCondition` wurde geändert, um den optionalen Parameter `caseSensitive` einzuschließen.

* `PropertySet` wurde geändert, um ein optionales `PermissionArray` als `permissions` einzufügen.

* `UploadDirectoryJob` wurde geändert, um optionale Parameter `xmpKeywords`, `xmpTemplateId` und `xmpTemplateOverride` einzuschließen.

* `VideoPublishJob` wurde geändert, um ein optionales `contextHandle` einzuschließen.

**Geänderte Vorgänge**

* `createAssetSet` wurde geändert, um ein optionales `thumbAssetHandle` einzuschließen.

* `createImageSet` wurde geändert, um ein optionales `thumbAssetHandle` einzuschließen.

* `createMetadataField` wurde geändert, um einen optionalen Parameter `initialTagValue` einzufügen.

* `createPropertySet` wurde geändert, um ein optionales `PermissionUpdateArray` als `permissionArray` einzufügen.

* `getImageServingPublishSettings` wurde geändert, um einen optionalen Parameter `contextHandle` einzufügen.

* `getImageRenderingPublishSettings` wurde geändert, um einen optionalen Parameter `contextHandle` einzufügen.

* `searchAssetsByFullText` wurde geändert, um eine Reihe optionaler Parameter einzuschließen:

   * `SearchFilter` als  `filters` Parameter

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata` wurde geändert, um eine Reihe optionaler Parameter einzuschließen:

   * `SearchFilter` als  `filters` Parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` Sequenz von sieben Parametern

* `setAssetPublishState` wurde geändert, um ein optionales `HandleArray` als `contextHandleArray` einzufügen.

* `setImageServingPublishSettings` wurde geändert, um einen optionalen Parameter `contextHandle` einzufügen.

* `setImageRenderingPublishSettings` wurde geändert, um einen optionalen Parameter `contextHandle`einzufügen.

* `submitJob` wurde geändert, um einen optionalen Auftragstyp `createVideoSitemap` einzuschließen.
