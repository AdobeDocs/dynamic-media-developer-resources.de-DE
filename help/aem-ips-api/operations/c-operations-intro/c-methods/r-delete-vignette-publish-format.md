---
description: Löscht ein Vignettenveröffentlichungsformat.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 12%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

Löscht ein Vignettenveröffentlichungsformat.

## Autorisierte Benutzertypen {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-789625ba29df4b5f880914d4c64f77ce}

**Eingabe (deleteVignettePublishFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Griff für das Unternehmen, zu dem die Vignette gehört. |
| vignetteFormatHandle | `xsd:string` | Ja | Der Ziehgriff zum Vignettenveröffentlichungsformat, das gelöscht werden soll. |

**Ausgabe (deleteVignettePublishFormatParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Dieses Codebeispiel löscht ein Vignettenveröffentlichungsformat, das durch seinen Handle angegeben ist.

**Anfrage**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Antwort**

Keine.
