---
description: Legt das Miniaturbild für ein oder mehrere Assets fest.
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 14%

---

# batchSetThumbAsset{#batchsetthumbasset}

Legt das Miniaturbild für ein oder mehrere Assets fest.

Syntax

## Miniatur-Asset-Typen {#section-4edc2a6a8f824213b0aaddb1d437268c}

Zulässige Asset-Typen für Miniaturansichten bestehen aus den folgenden:

* Bild
* Angepasste Ansicht
* Maske
* Vorlage
* PsdTemplate

## Autorisierte Benutzertypen {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese-/Schreibzugriff auf das Ziel-Asset und Lesezugriff auf das Daumenasset haben.

## Parameter {#section-9c6efa000b384b3db6c013def20cf40b}

**Eingabe (batchSetThumbAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, das die Assets enthält. |
| updateArray | `types:ThumbAssetUpdateArray` | Ja | Das Array von Updates. |

**Ausgabe (batchSetThumbAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Die Anzahl der erfolgreich eingerichteten Miniaturansichten. |
| warningCount | `xsd:int` | Ja | Die Anzahl der Warnungen, die generiert wurden, wenn der Vorgang versuchte, die Miniaturansichten festzulegen. |
| errorCount | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, die Miniaturansichten festzulegen. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Warnungen generiert haben, wenn der Vorgang versucht hat, die Aktualisierungen anzuwenden. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Fehler generiert haben, wenn der Vorgang versucht hat, die Aktualisierungen anzuwenden. |

## Beispiele {#section-6de69a8680c24c1486c5f01488393381}

**Anforderung**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**Antwort**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```
