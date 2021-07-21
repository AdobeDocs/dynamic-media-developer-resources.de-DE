---
description: Ruft die Suchzeichenfolgen, Keywords und andere Informationen zu einem Asset ab. Die Antwort enthält zusätzliche Informationen zum Asset.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 17%

---

# getSearchStrings{#getsearchstrings}

Ruft die Suchzeichenfolgen, Keywords und andere Informationen zu einem Asset ab. Die Antwort enthält zusätzliche Informationen zum Asset.

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
| `*`companyHandle`*` | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| `*`assetHandle`*` | `xsd:string` | Ja | Umgang mit dem Asset. |

**Ausgabe (getSearchStringsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | Ja | Ein Array von Asset-Suchzeichenfolgen. |

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
