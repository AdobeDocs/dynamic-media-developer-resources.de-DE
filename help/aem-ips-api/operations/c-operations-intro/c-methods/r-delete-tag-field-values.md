---
description: Entfernt Tag-Feldwerte aus dem Wörterbuch eines Tag-Felds.
seo-description: Entfernt Tag-Feldwerte aus dem Wörterbuch eines Tag-Felds.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
topic: Scene7 Image Production System API
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
translation-type: tm+mt
source-git-commit: b5eaefb375fbd0d0786619fa6d84b4f6fc17a77f
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 12%

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff der Firma, die das Tag-Feld enthält. |
| ` *`fieldHandle`*` | `xsd:string` | Ja | Der Griff des zu ändernden Tag-Felds. |
| ` *`valueArray`*` | `types:StringArray` | Ja | Ein Array von Tag-Werten, die aus dem Wörterbuch des Felds gelöscht werden sollen. |

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
