---
description: Diese neuen oder geänderten Vorgänge und Datentypen, die in der Beta-WSDL verfügbar sind, dürfen nicht außerhalb von in Dynamic Media entwickelten Anwendungen verwendet werden.
solution: Experience Manager
title: Eingeschränkte Verwendung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
TQID: 'https://experienceleague.adobe.com/X-Q28iVTM95SDSwlSy3yhmJcfJv0TC3LtxXPRv8RCpg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Eingeschränkte Verwendung{#restricted-use}

Diese neuen oder geänderten Vorgänge und Datentypen, die in der Beta-WSDL verfügbar sind, dürfen nicht außerhalb von in Dynamic Media entwickelten Anwendungen verwendet werden.

Diese Vorgänge und Typen können bei späteren Systemaktualisierungen deaktiviert, geändert oder eingestellt werden.

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
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Geänderte Typen**

* `ActiveJob` geändert, um einen `createVideoSitemapJob` einzuschließen

* `ScheduledJob` geändert, um einen `createVideoSitemapJob` einzuschließen

* Der `ImageServingPublishJob` wurde geändert und enthält jetzt eine optionale `contextHandle`

* Der `ImageRenderingPublishJob` wurde geändert und enthält jetzt eine optionale `contextHandle`

* Der `MetadataField` wurde geändert und enthält jetzt eine optionale `initialTagField`

* `MetadataCondition` geändert, um und optionale `caseSensitive` einzuschließen

* `PropertySet` geändert, um eine optionale `PermissionArray` als `permissions` einzuschließen

* `UploadDirectoryJob` geändert, um optionale `xmpKeywords`-, `xmpTemplateId`- und `xmpTemplateOverride` einzuschließen

* Der `VideoPublishJob` wurde geändert und enthält jetzt eine optionale `contextHandle`

**Geänderte Vorgänge**

* Der `createAssetSet` wurde geändert und enthält jetzt eine optionale `thumbAssetHandle`

* Der `createImageSet` wurde geändert und enthält jetzt eine optionale `thumbAssetHandle`

* Der `createMetadataField` wurde geändert und enthält jetzt einen optionalen `initialTagValue`

* `createPropertySet` geändert, um eine optionale `PermissionUpdateArray` als `permissionArray` einzuschließen

* Der `getImageServingPublishSettings` wurde geändert und enthält jetzt einen optionalen `contextHandle`

* Der `getImageRenderingPublishSettings` wurde geändert und enthält jetzt einen optionalen `contextHandle`

* `searchAssetsByFullText` wurde geändert, um eine Reihe optionaler Parameter einzuschließen:

   * Als `filters` Parameter `SearchFilter`

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata` wurde geändert, um eine Reihe optionaler Parameter einzuschließen:

   * Als `filters` Parameter `SearchFilter`

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` Sequenz von sieben Parametern

* `setAssetPublishState` geändert, um eine optionale `HandleArray` als `contextHandleArray` einzuschließen

* Der `setImageServingPublishSettings` wurde geändert und enthält jetzt einen optionalen `contextHandle`

* Der `setImageRenderingPublishSettings` wurde geändert und enthält jetzt einen optionalen `contextHandle`.

* `submitJob` geändert, um einen optionalen `createVideoSitemap`-Vorgangstyp einzuschließen

