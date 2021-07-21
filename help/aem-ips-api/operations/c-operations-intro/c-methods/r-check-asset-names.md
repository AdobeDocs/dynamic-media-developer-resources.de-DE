---
description: Überprüft, ob Konflikte mit IPS-IDs auftreten, indem Asset-Namen mit allen Namen des Namespace des Image Serving/Image Rendering-Katalogs eines Unternehmens verglichen werden.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# checkAssetNames{#checkassetnames}

Überprüft, ob Konflikte mit IPS-IDs auftreten, indem Asset-Namen mit allen Namen des Namespace des Image Serving/Image Rendering-Katalogs eines Unternehmens verglichen werden.

Syntax

## Autorisierte Benutzertypen {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parameter {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Eingabe (checkAssetNamesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Nein | Der Handle für das Unternehmen, das den Benutzer enthält. |
| `*`assetNamesArray`*` | `types:StringArray` | Ja | Ein Array von Asset-Namen, die überprüft werden sollen. |

**Ausgabe (checkAssetNamesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`inUseNameArray`*` | `types:StringArray` | Ja | Ein Array der verwendeten Asset-Namen. |

## Beispiele {#section-bc5d120d74614a63a425ca3acc337219}

Dieser Beispielcode fordert die Asset-Namen an, die für ein bestimmtes Unternehmen verwendet werden. Die Antwort gibt ein Array von Asset-Namen zurück, die verwendet werden.

**Anforderung**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Antwort**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```
