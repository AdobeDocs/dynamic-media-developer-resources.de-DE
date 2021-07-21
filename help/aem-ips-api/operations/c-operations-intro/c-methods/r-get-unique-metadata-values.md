---
description: Ruft eindeutige Metadatenfeldwerte ab.
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadaten
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 25%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| `*`fieldHandle`*` | `xsd:string` | Nein | Umgang mit Metadatenfeldern. |

**Ausgabe (getUniqueMetadataValuesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`Werte`*` | `type:StringArray` |  |  |

## Beispiele {#section-440f3bc3e5be436cb6ec26117d05f476}

In diesem Codebeispiel wird ein Feld-Handle verwendet, um bestimmte Metadatenwerte zurückzugeben.

**Anforderung**

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
