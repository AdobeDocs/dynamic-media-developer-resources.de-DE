---
description: Eine Systemfeldsuchbedingung für den Vorgang searchAssets .
solution: Experience Manager
title: SystemFieldBedingung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 6%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Eine Systemfeldsuchbedingung für den Vorgang searchAssets .

Übergeben Sie bei unären Vergleichen genau einen Wert ( `boolVal`, `longVal`, `doubleVal` oder `dateVal`), je nach Systemfeldtyp. Übergeben Sie für Suchbereiche die Parameter `min<Type>` und `max<Type>` und übergeben Sie den Wert `op` von `Between` oder `NotBetween`.

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
| maxDouble | `xsd:double` | Obere Grenze des doppelten Bereichs. |
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
