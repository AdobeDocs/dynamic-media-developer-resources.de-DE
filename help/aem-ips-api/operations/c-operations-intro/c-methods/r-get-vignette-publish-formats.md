---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 21%

---

# getVignettePublishFormats{#getvignettepublishformats}

Syntax

## Autorisierte Benutzertypen {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Eingabe (getVignettePublishFormatsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Griff zum Unternehmen. |

**Ausgabe (getVignettePublishFormatsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| vignetteFormatArray | `types:VignettePublishFormatArray` | Ja | Eine Reihe von Vignettenveröffentlichungsformaten. |

## Beispiele {#section-2cc32b27cc6243b7b3e273cc05996226}

Dieses Codebeispiel gibt zwei Vignettenveröffentlichungsformate zurück, die mit einem bestimmten Unternehmen verknüpft sind. Informationen werden in einem Array zurückgegeben, das zur Vereinfachung gekürzt wird.

**Anfrage**

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
