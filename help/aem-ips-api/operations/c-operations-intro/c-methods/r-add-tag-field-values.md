---
description: Fügt dem Wörterbuch eines vorhandenen Tag-Felds neue Tag-Werte hinzu.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 12%

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
| companyHandle | `xsd:string` | Ja | Der Handle des Unternehmens, das das Tag-Feld enthält. |
| fieldHandle | `xsd:string` | Ja | Der Handle des zu ändernden Tag-Felds. |
| valueArray | `xsd:string` | Ja | Ein Array von Tag-Werten, die dem vorhandenen Wörterbuch des Felds hinzugefügt werden sollen. |

**Output (addTagFieldValuesParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-c4049392f1c548f883b8b1f8f167bada}

**Anfrage**

```java {.line-numbers}
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
