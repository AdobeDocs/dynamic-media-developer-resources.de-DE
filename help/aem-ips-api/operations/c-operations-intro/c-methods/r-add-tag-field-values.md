---
description: Fügt dem Wörterbuch eines vorhandenen Tag-Felds neue Tag-Werte hinzu.
seo-description: Fügt dem Wörterbuch eines vorhandenen Tag-Felds neue Tag-Werte hinzu.
seo-title: addTagFieldValues
solution: Experience Manager
title: addTagFieldValues
topic: Scene7 Image Production System API
uuid: 9304f02c-a1df-4477-ab33-f2491c390c92
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addTagFieldValues{#addtagfieldvalues}

Fügt dem Wörterbuch eines vorhandenen Tag-Felds neue Tag-Werte hinzu.

Syntax

## Autorisierte Benutzertypen {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff der Firma, die das Tag-Feld enthält. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | Der Griff des zu ändernden Tag-Felds. |
| ` *`valueArray`*` | `xsd:string` | Ja | Ein Array von Tag-Werten, die dem vorhandenen Wörterbuch des Felds hinzugefügt werden sollen. |

**Output (addTagFieldValuesParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-c4049392f1c548f883b8b1f8f167bada}

**Anforderung**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**Antwort**

Keine.
