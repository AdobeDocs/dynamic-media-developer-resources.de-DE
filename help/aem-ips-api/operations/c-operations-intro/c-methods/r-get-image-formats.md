---
description: Gibt Bildformate wie PDF, EPS, SWF und andere zurück.
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 17%

---

# getImageFormats{#getimageformats}

Gibt Bildformate wie PDF, EPS, SWF und andere zurück.

Syntax

## Autorisierte Benutzertypen {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-eefa36a70b74498f8727ef61d98cfb63}

**Eingabe (getImageFormatsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handler für das Unternehmen mit den Bildformaten, die Sie erhalten möchten. |

**Ausgabe (getImageFormatsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | Ja | Das Bildformat-Array. |

## Beispiele {#section-73881e12839b4904bf3299b0920bdd0c}

Dieses Codebeispiel gibt alle Bildformate für das angegebene Unternehmen zurück.

**Anfrage**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**Antwort**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```
