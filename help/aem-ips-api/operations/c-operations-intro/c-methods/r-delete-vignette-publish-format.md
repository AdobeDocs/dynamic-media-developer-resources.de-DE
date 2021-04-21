---
description: Löscht das Veröffentlichungsformat einer Vignette.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 13%

---


# deleteVignettePublishFormat{#deletevignettepublishformat}

Löscht das Veröffentlichungsformat einer Vignette.

## Autorisierte Benutzertypen {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-789625ba29df4b5f880914d4c64f77ce}

**Input (deleteVignettePublishFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff der Firma, zu der die Vignette gehört. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Ja | Der Griff zum zu löschenden Vignettenveröffentlichungsformat. |

**Output (deleteVignettePublishFormatParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Mit diesem Codebeispiel wird ein vom Handle angegebenes Vignettenveröffentlichungsformat gelöscht.

**Anforderung**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Antwort**

Keine.
