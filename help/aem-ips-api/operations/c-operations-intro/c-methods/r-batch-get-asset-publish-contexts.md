---
description: Gibt den Veröffentlichungskontext für Assets zurück, die zur Veröffentlichung markiert wurden.
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 16%

---

# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

Gibt den Veröffentlichungskontext für Assets zurück, die zur Veröffentlichung markiert wurden.

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
>* Alle Benutzer haben Zugriff auf das freigegebene Unternehmen.
>


## Parameter {#section-1742fcb196224545b270eb8241f757a8}

**Eingabe (batchGetAssetPublishContextsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| assetHandleArray | ` `Typen:HandleArray&quot; | Ja | Eine Liste der Assets, die für aktive (zur Veröffentlichung markierte) Kontexte abgefragt werden sollen. |

**Ausgabe (batchGetAssetPublishContextsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetPublishContextsArray | `types:assetPublishContextsArray` | Ja | Ein Array von Veröffentlichungskontexten, in denen jedes Asset zur Veröffentlichung markiert ist. |

## Beispiele {#section-457f6809ccfa425b9a0976313d613f4e}

**Anforderung**

```java {.line-numbers}
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Antwort**

```java {.line-numbers}
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
