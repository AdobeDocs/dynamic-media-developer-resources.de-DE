---
description: Gibt die Kontexte zum Veröffentlichen für zur Veröffentlichung markierte Assets zurück.
seo-description: Gibt die Kontexte zum Veröffentlichen für zur Veröffentlichung markierte Assets zurück.
seo-title: batchGetAssetPublishContexts
solution: Experience Manager
title: batchGetAssetPublishContexts
topic: Scene7 Image Production System API
uuid: 7f442019-37a9-4473-be92-a952a7a67664
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 14%

---


# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

Gibt die Kontexte zum Veröffentlichen für zur Veröffentlichung markierte Assets zurück.

Syntax

## Autorisierte Benutzertypen {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>* Der Benutzer muss über Lesezugriff verfügen, um die Assets zurückgeben zu können.
>* Alle Benutzer haben Zugriff auf die freigegebene Firma.

>



## Parameter {#section-1742fcb196224545b270eb8241f757a8}

**Input (batchGetAssetPublishContextsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| ` *`assetHandleArray`*` | ` `Typen:HandleArray&quot; | Ja | Eine Liste von Assets, die Sie für aktive (zur Veröffentlichung markierte) Kontexte Abfrage haben möchten. |

**Output (batchGetAssetPublishContextsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`assetPublishContextsArray`*` | `types:assetPublishContextsArray` | Ja | Ein Array von Kontexten zum Veröffentlichen, in denen jedes Asset zur Veröffentlichung markiert ist. |

## Beispiele {#section-457f6809ccfa425b9a0976313d613f4e}

**Anforderung**

```java
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Antwort**

```java
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```

