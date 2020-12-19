---
description: Eine Systemfeldsuchbedingung für den Vorgang searchAssets.
seo-description: Eine Systemfeldsuchbedingung für den Vorgang searchAssets.
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
topic: Scene7 Image Production System API
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 6%

---


# SystemFieldCondition{#systemfieldcondition}

Eine Systemfeldsuchbedingung für den Vorgang searchAssets.

Bei unären Vergleichen müssen Sie je nach Systemfeldtyp genau einen Wert ( `boolVal`, `longVal`, `doubleVal` oder `dateVal`) übergeben. Übergeben Sie für Suchbereiche die Parameter `min<Type>` und `max<Type>` und übergeben Sie den Wert `op` von `Between` oder `NotBetween`.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`Feld`*` | `xsd:string` | Auswahl der Systemfelder für die Asset-Suche. |
| ` *`op`*` | `xsd:string` | Auswahl von Stringvergleichsoperatoren. |
| ` *`Wert`*` | `xsd:string` | Zu testender Wert. |
| ` *`boolVal`*` | `xsd:boolean` | Boolescher Vergleichswert. |
| ` *`longVal`*` | `xsd:long` | Langer Vergleichswert. |
| ` *`minLong`*` | `xsd:long` | Untere Begrenzung des langen Bereichs. |
| ` *`maxLong`*` | `xsd:long` | Obere Grenze des langen Bereichs. |
| ` *`doubleVal`*` | `xsd:double` | Vergleichswert der Dublette. |
| ` *`minDouble`*` | `xsd:double` | Untere Begrenzung des Bereichs Dublette. |
| ` *`maxDouble`*` | `xsd:double` | Obere Begrenzung des Bereichs Dublette. |
| ` *`dateVal`*` | `xsd:dateTime` | Datumsvergleichswert. |
| ` *`minDate`*` | `xsd:dateTime` | Minimum des Datumsbereichs. |
| ` *`maxDate`*` | `xsd:dateTime` | Maximum für Datumsbereich. |

## Beispiel {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```

