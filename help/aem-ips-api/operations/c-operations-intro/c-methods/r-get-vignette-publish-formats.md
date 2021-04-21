---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 22%

---


# getVignettePublishFormats{#getvignettepublishformats}

Syntax

## Autorisierte Benutzertypen {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Input (getVignettePublishFormatsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma. |

**Output (getVignettePublishFormatsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | Ja | Array von Vignettenveröffentlichungsformaten. |

## Beispiele {#section-2cc32b27cc6243b7b3e273cc05996226}

Dieses Codebeispiel gibt zwei Vignettenveröffentlichungsformate zurück, die mit einer bestimmten Firma verknüpft sind. Informationen werden in einem Array zurückgegeben, das aufgrund der Kürze abgeschnitten wird.

**Anforderung**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**Antwort**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```

