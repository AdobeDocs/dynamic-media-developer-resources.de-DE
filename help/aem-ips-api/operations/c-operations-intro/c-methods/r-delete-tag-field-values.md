---
description: Entfernt Tag-Feldwerte aus dem Wörterbuch eines Tag-Felds.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 13%

---

# deleteTagFieldValues{#deletetagfieldvalues}

Entfernt Tag-Feldwerte aus dem Wörterbuch eines Tag-Felds.

## Autorisierte Benutzertypen {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-5db64a6ae238426395bc760b83587260}

**Eingabe (deleteTagFieldValuesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle des Unternehmens, das das Tag-Feld enthält. |
| fieldHandle | `xsd:string` | Ja | Der Handle des zu ändernden Tag-Felds. |
| valueArray | `types:StringArray` | Ja | Ein Array von Tag-Werten, die aus dem Wörterbuch des Felds gelöscht werden sollen. |

**Ausgabe (deleteTagFieldValuesParam)**

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
