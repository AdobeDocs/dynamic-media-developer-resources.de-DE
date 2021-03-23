---
description: Entfernt Tag-Feldwerte aus dem Wörterbuch eines Tag-Felds.
seo-description: Entfernt Tag-Feldwerte aus dem Wörterbuch eines Tag-Felds.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 11%

---


# deleteTagFieldValues{#deletetagfieldvalues}

Entfernt Tag-Feldwerte aus dem Wörterbuch eines Tag-Felds.

## Autorisierte Benutzertypen {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-5db64a6ae238426395bc760b83587260}

**Input (deleteTagFieldValuesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff der Firma, die das Tag-Feld enthält. |
| `*`fieldHandle`*` | `xsd:string` | Ja | Der Griff des zu ändernden Tag-Felds. |
| `*`valueArray`*` | `types:StringArray` | Ja | Ein Array von Tag-Werten, die aus dem Wörterbuch des Felds gelöscht werden sollen. |

**Output (deleteTagFieldValuesParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-92f9e575a6da491caa09e264b4d6ee55}

**Anforderung**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**Antwort**

Keine.
