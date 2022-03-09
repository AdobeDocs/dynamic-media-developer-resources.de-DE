---
description: Eine Systemfeldsuchbedingung für den Vorgang "searchAssets".
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 6%

---

# SystemFieldCondition{#systemfieldcondition}

Eine Systemfeldsuchbedingung für den Vorgang &quot;searchAssets&quot;.

Für unäre Vergleiche müssen Sie genau einen Wert ( `boolVal`, `longVal`, `doubleVal`oder `dateVal`) abhängig vom Systemfeldtyp. Für Suchbereiche übergeben Sie `min<Type>` und `max<Type>` Parameter und übergeben Sie eine `op` Wert von `Between` oder `NotBetween`.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| Feld | `xsd:string` | Auswahl der Asset-Suchsystemfelder. |
| op | `xsd:string` | Auswahl der Operatoren für Zeichenfolgenvergleich. |
| value | `xsd:string` | Wert, mit dem getestet werden soll. |
| boolVal | `xsd:boolean` | Boolescher Vergleichswert. |
| longVal | `xsd:long` | Long-Vergleichswert. |
| minLong | `xsd:long` | Untere Grenze des langen Bereichs. |
| maxLong | `xsd:long` | Obere Grenze des langen Bereichs. |
| doubleVal | `xsd:double` | Doppelter Vergleichswert. |
| minDouble | `xsd:double` | Untere Grenze des doppelten Bereichs. |
| maxDouble | `xsd:double` | Obere Grenze des Doppelbereichs. |
| dateVal | `xsd:dateTime` | Datumsvergleichswert. |
| minDate | `xsd:dateTime` | Datumsbereich Minimum. |
| maxDate | `xsd:dateTime` | Maximaler Datumsbereich. |

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
