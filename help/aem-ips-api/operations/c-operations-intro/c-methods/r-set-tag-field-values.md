---
description: Legt Tag-Wörterbuchwerte für ein vorhandenes Tag-Feld fest.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 15%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Handle des Unternehmens. |
| `*`fieldHandle`*` | `xsd:string` | Ja | Tag-Feld-Handle. |
| `*`valueArray`*` | `types:StringArray` | Ja | Ein Array von Tag-Werten, die das vorhandene Wörterbuch des Felds ersetzen. Asset-Zuordnungen werden beibehalten, wenn ein neuer Wert mit einem vorhandenen Wert übereinstimmt. |

**Ausgabe (setTagFieldValuesReturn)**

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
