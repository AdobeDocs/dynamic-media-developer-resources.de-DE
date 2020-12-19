---
description: Legt das Miniaturbild für ein oder mehrere Assets fest.
seo-description: Legt das Miniaturbild für ein oder mehrere Assets fest.
seo-title: batchSetThumbAsset
solution: Experience Manager
title: batchSetThumbAsset
topic: Scene7 Image Production System API
uuid: 16c298a7-bb07-4643-824b-8f864d7f0290
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 13%

---


# batchSetThumbAsset{#batchsetthumbasset}

Legt das Miniaturbild für ein oder mehrere Assets fest.

Syntax

## Miniaturansichten Asset-Typen {#section-4edc2a6a8f824213b0aaddb1d437268c}

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
>Der Benutzer muss Lese-/Schreibzugriff auf das Asset der Zielgruppe und Lesezugriff auf das Miniaturbild-Asset haben.

## Parameter {#section-9c6efa000b384b3db6c013def20cf40b}

**Input (batchSetThumbAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, die die Assets enthält. |
| ` *`updateArray`*` | `types:ThumbAssetUpdateArray` | Ja | Das Aktualisierungsarray. |

**Output (batchSetThumbAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Die Anzahl der erfolgreich eingerichteten Miniaturansichten. |
| ` *`warningCount`*` | `xsd:int` | Ja | Die Anzahl der Warnungen, die beim Versuch des Vorgangs generiert wurden, die Miniaturansichten festzulegen. |
| ` *`errorCount`*` | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, die Miniaturansichten festzulegen. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Warnungen generiert haben, wenn der Vorgang versuchte, die Aktualisierungen anzuwenden. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Fehler generiert haben, wenn der Vorgang versuchte, die Aktualisierungen anzuwenden. |

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

