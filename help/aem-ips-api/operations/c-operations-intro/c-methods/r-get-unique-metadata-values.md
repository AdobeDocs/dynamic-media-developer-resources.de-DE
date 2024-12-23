---
description: Ruft eindeutige Metadatenfeldwerte ab.
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 24%

---

# getUniqueMetadataValues{#getuniquemetadatavalues}

Ruft eindeutige Metadatenfeldwerte ab.

Syntax

## Autorisierte Benutzertypen {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-b9d1413811c24566b6d095701f0f66db}

**Eingabe (getUniqueMetadataValuesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Übernehmen Sie die Firma. |
| fieldHandle | `xsd:string` | Nein | Verarbeiten Sie das -Metadatenfeld. |

**Ausgabe (getUniqueMetadataValuesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| Werte | `type:StringArray` |  |  |

## Beispiele {#section-440f3bc3e5be436cb6ec26117d05f476}

Dieses Codebeispiel verwendet ein Feld-Handle, um bestimmte Metadatenwerte zurückzugeben.

**Anfrage**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Antwort**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```
