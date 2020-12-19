---
description: Legt Tag-Wörterbuchwerte für ein vorhandenes Tag-Feld fest.
seo-description: Legt Tag-Wörterbuchwerte für ein vorhandenes Tag-Feld fest.
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Scene7 Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 14%

---


# setTagFieldValues{#settagfieldvalues}

Legt Tag-Wörterbuchwerte für ein vorhandenes Tag-Feld fest.

Syntax

## Autorisierte Benutzertypen {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-a05cbee4cb4f44198c414a6b14e69156}

**Eingabe**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | Tag-Feldgriff. |
| ` *`valueArray`*` | `types:StringArray` | Ja | Ein Array von Tag-Werten, die das vorhandene Wörterbuch des Felds ersetzen. Asset-Verknüpfungen werden beibehalten, wenn ein neuer Wert mit einem vorhandenen Wert übereinstimmt. |

**Output (setTagFieldValuesReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-b11cafd9bed54ab5836c737cc075c918}

**Anforderung**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**Antwort**

Keine.
