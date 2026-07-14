---
description: Eine Suchbedingung für Systemfelder für den Vorgang searchAssets .
solution: Experience Manager
title: SystemfeldBedingung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
TQID: 'https://experienceleague.adobe.com/dCZl4pLGuG5hHpEq04W-qv8mRWcFiA7PvmzcO7Un-sM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 6%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Eine Suchbedingung für Systemfelder für den Vorgang searchAssets .

Übergeben Sie bei unären Vergleichen genau einen Wert ( `boolVal`, `longVal`, `doubleVal` oder `dateVal`), je nach Systemfeldtyp. Übergeben Sie für Suchbereiche `min<Type>` und `max<Type>` Parameter und einen `op` Wert von `Between` oder `NotBetween`.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| Feld | `xsd:string` | Auswahl der Asset-Suchsystemfelder. |
| op | `xsd:string` | Auswahl von Zeichenfolgenvergleichsoperatoren. |
| value | `xsd:string` | Zu testender Wert. |
| boolVal | `xsd:boolean` | Boolescher Vergleichswert. |
| longVal | `xsd:long` | Langer Vergleichswert. |
| minLong | `xsd:long` | Unterer Rand des langen Bereichs. |
| maxLong | `xsd:long` | Obere Grenze des langen Bereichs. |
| doubleVal | `xsd:double` | Doppelter Vergleichswert. |
| minDouble | `xsd:double` | Untere Grenze des doppelten Bereichs. |
| maxDouble | `xsd:double` | Obere Grenze des doppelten Bereichs. |
| dateVal | `xsd:dateTime` | Datumsvergleichswert. |
| minDate | `xsd:dateTime` | Mindestdatumsbereich. |
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

