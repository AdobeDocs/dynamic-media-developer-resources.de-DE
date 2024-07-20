---
description: Legt Asset-Metadaten mithilfe des Batch-Modus fest.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 12%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

Legt Asset-Metadaten mithilfe des Batch-Modus fest.

Syntax

## Autorisierte Benutzertypen {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-7111ac93bc7747f69ba14db4ac3912b0}

**Input (batchSetAssetMetadataParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, dessen Metadaten Sie in einem Batch-Vorgang festlegen möchten. |
| updateArray | `types:BatchMetadataUpdateArray` | Ja | Das Array der auf die Assets angewendeten Metadaten-Aktualisierungen. |

**Output (batchSetAssetMetadataParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Die Anzahl der erfolgreich eingerichteten Metadaten. |
| warningCount | `xsd:int` | Ja | Die Anzahl der Warnungen, die generiert wurden, wenn der Vorgang versucht hat, Metadaten festzulegen. |
| errorCount | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, Metadaten festzulegen. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Warnungen generieren, wenn der Vorgang versucht hat, Metadaten für die Assets im Batch-Modus festzulegen. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Fehler generieren, wenn der Vorgang versucht hat, Metadaten für die Assets im Batch-Modus festzulegen. |

## Beispiele {#section-2de798ac920e4b47b971b1729a64395b}

**Anfrage**

```java {.line-numbers}
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**Antwort**

```java {.line-numbers}
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
