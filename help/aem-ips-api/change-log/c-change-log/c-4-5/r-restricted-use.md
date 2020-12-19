---
description: Diese neuen oder geänderten Vorgänge und Datentypen, die in der Beta-WSDL verfügbar sind, dürfen nicht außerhalb der von Scene7 entwickelten Anwendungen verwendet werden.
seo-description: Diese neuen oder geänderten Vorgänge und Datentypen, die in der Beta-WSDL verfügbar sind, dürfen nicht außerhalb der von Scene7 entwickelten Anwendungen verwendet werden.
seo-title: Eingeschränkte Verwendung
solution: Experience Manager
title: Eingeschränkte Verwendung
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---


# Eingeschränkte Verwendung{#restricted-use}

Diese neuen oder geänderten Vorgänge und Datentypen, die in der Beta-WSDL verfügbar sind, dürfen nicht außerhalb der von Scene7 entwickelten Anwendungen verwendet werden.

Diese Vorgänge und Typen können mit nachfolgenden Systemaktualisierungen deaktiviert, geändert oder eingestellt werden.

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

* `ActiveJob` wurde geändert, um einen `createVideoSitemapJob`-Typ einzuschließen

* `ScheduledJob` wurde geändert, um einen `createVideoSitemapJob`-Typ einzuschließen

* `ImageServingPublishJob` wurde geändert, um ein optionales `contextHandle` einzuschließen

* `ImageRenderingPublishJob` wurde geändert, um ein optionales `contextHandle` einzuschließen

* `MetadataField` wurde geändert, um ein optionales `initialTagField` einzuschließen

* Der Parameter `MetadataCondition` wurde zum Einschließen und zum optionalen Parameter `caseSensitive` geändert.

* `PropertySet` wurde geändert, um ein optionales `PermissionArray` als `permissions` einzuschließen

* Die Parameter `UploadDirectoryJob` wurden geändert, um optionale Parameter `xmpKeywords`, `xmpTemplateId` und `xmpTemplateOverride` einzuschließen.

* `VideoPublishJob` wurde geändert, um ein optionales `contextHandle` einzuschließen

**Geänderte Vorgänge**

* `createAssetSet` wurde geändert, um ein optionales `thumbAssetHandle` einzuschließen

* `createImageSet` wurde geändert, um ein optionales `thumbAssetHandle` einzuschließen

* `createMetadataField` wurde geändert, um einen optionalen Parameter `initialTagValue` einzuschließen

* `createPropertySet` wurde geändert, um ein optionales `PermissionUpdateArray` als `permissionArray` einzuschließen

* `getImageServingPublishSettings` wurde geändert, um einen optionalen Parameter `contextHandle` einzuschließen

* `getImageRenderingPublishSettings` wurde geändert, um einen optionalen Parameter `contextHandle` einzuschließen

* `searchAssetsByFullText` wurde geändert, um eine Reihe optionaler Parameter einzuschließen:

   * `SearchFilter` as- `filters` Parameter

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata` wurde geändert, um eine Reihe optionaler Parameter einzuschließen:

   * `SearchFilter` as- `filters` Parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` Sequenz von sieben Parametern

* `setAssetPublishState` wurde geändert, um ein optionales `HandleArray` als `contextHandleArray` einzuschließen

* `setImageServingPublishSettings` wurde geändert, um einen optionalen Parameter `contextHandle` einzuschließen

* `setImageRenderingPublishSettings` wurde geändert, um einen optionalen `contextHandle`Parameter einzuschließen

* `submitJob` wurde geändert, um einen optionalen `createVideoSitemap` Auftragstyp einzuschließen

