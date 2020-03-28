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

* Änderung `ActiveJob` zur Einbeziehung eines `createVideoSitemapJob` Typs

* Änderung `ScheduledJob` zur Einbeziehung eines `createVideoSitemapJob` Typs

* Änderung `ImageServingPublishJob` zur Aufnahme eines optionalen `contextHandle`

* Änderung `ImageRenderingPublishJob` zur Aufnahme eines optionalen `contextHandle`

* Änderung `MetadataField` zur Aufnahme eines optionalen `initialTagField`

* In `MetadataCondition` Einschluss- und optionalen `caseSensitive` Parameter geändert

* Änderung `PropertySet` zum Hinzufügen eines optionalen `PermissionArray` als `permissions`

* Änderung `UploadDirectoryJob` zum Einschließen optionaler `xmpKeywords`Parameter `xmpTemplateId` und `xmpTemplateOverride` Parameter

* Änderung `VideoPublishJob` zur Aufnahme eines optionalen `contextHandle`

**Geänderte Vorgänge**

* Änderung `createAssetSet` zur Aufnahme eines optionalen `thumbAssetHandle`

* Änderung `createImageSet` zur Aufnahme eines optionalen `thumbAssetHandle`

* Änderung `createMetadataField` zur Aufnahme eines optionalen `initialTagValue` Parameters

* Änderung `createPropertySet` zum Hinzufügen eines optionalen `PermissionUpdateArray` als `permissionArray`

* Änderung `getImageServingPublishSettings` zur Aufnahme eines optionalen `contextHandle` Parameters

* Änderung `getImageRenderingPublishSettings` zur Aufnahme eines optionalen `contextHandle` Parameters

* Änderung `searchAssetsByFullText` zur Einbeziehung einer Reihe optionaler Parameter:

   * `SearchFilter` as- `filters` Parameter

   * `sortBy`
   * `sortDirection`

* Änderung `searchAssetsByMetadata` zur Einbeziehung einer Reihe optionaler Parameter:

   * `SearchFilter` as- `filters` Parameter

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` Sequenz von sieben Parametern

* Änderung `setAssetPublishState` zum Hinzufügen eines optionalen `HandleArray` als `contextHandleArray`

* Änderung `setImageServingPublishSettings` zur Aufnahme eines optionalen `contextHandle` Parameters

* Änderung `setImageRenderingPublishSettings` zur Aufnahme eines optionalen `contextHandle`Parameters

* Änderung `submitJob` zur Aufnahme eines optionalen `createVideoSitemap` Auftragstyps

