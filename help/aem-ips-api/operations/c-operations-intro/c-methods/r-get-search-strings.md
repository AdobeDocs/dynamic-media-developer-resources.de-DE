---
description: Ruft die Suchzeichenfolgen, Suchbegriffe und andere Informationen zu einem Asset ab. Die Antwort enthält weitere Informationen zum Asset.
seo-description: Ruft die Suchzeichenfolgen, Suchbegriffe und andere Informationen zu einem Asset ab. Die Antwort enthält weitere Informationen zum Asset.
seo-title: getSearchStrings
solution: Experience Manager
title: getSearchStrings
topic: Scene7 Image Production System API
uuid: 9d588d6b-c79c-4531-a2e8-8467254a7985
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getSearchStrings{#getsearchstrings}

Ruft die Suchzeichenfolgen, Suchbegriffe und andere Informationen zu einem Asset ab. Die Antwort enthält weitere Informationen zum Asset.

Syntax

## Autorisierte Benutzertypen {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-c1efda4bb15349a68b276bafee8c18fd}

**Eingabe (getSearchStringsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem Asset. |

**Output (getSearchStringsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`searchStringArray`*` | `types:SearchStrings` | Ja | Ein Array von Asset-Suchzeichenfolgen. |

## Beispiele {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Dieses Codebeispiel gibt Asset-spezifische Suchzeichenfolgen zurück. Die Antwort gibt ein leeres Array zurück.

**Anforderung**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Antwort**

Keine.
