---
description: Fügt dem Wörterbuch eines vorhandenen Tag-Felds neue Tag-Werte hinzu.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 13%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff der Firma, die das Tag-Feld enthält. |
| `*`fieldHandle`*` | `xsd:string` | Ja | Der Griff des zu ändernden Tag-Felds. |
| `*`valueArray`*` | `xsd:string` | Ja | Ein Array von Tag-Werten, die dem vorhandenen Wörterbuch des Felds hinzugefügt werden sollen. |

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
