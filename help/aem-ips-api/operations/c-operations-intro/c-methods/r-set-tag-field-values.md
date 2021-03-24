---
description: Legt Tag-Wörterbuchwerte für ein vorhandenes Tag-Feld fest.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '88'
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
| `*`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| `*`fieldHandle`*` | `xsd:string` | Ja | Tag-Feldgriff. |
| `*`valueArray`*` | `types:StringArray` | Ja | Ein Array von Tag-Werten, die das vorhandene Wörterbuch des Felds ersetzen. Asset-Verknüpfungen werden beibehalten, wenn ein neuer Wert mit einem vorhandenen Wert übereinstimmt. |

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
