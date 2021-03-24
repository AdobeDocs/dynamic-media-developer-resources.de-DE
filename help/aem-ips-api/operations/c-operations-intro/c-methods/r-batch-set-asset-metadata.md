---
description: Legt Asset-Metadaten im Stapelmodus fest.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata.Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 12%

---


# batchSetAssetMetadata{#batchsetassetmetadata}

Legt Asset-Metadaten im Stapelmodus fest.

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
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, deren Metadaten Sie bei einem Stapelvorgang festlegen möchten. |
| `*`updateArray`*` | `types:BatchMetadataUpdateArray` | Ja | Das Array der auf die Assets angewendeten Metadaten-Aktualisierungen. |

**Output (batchSetAssetMetadataParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Die Anzahl der erfolgreich eingerichteten Metadaten. |
| `*`warningCount`*` | `xsd:int` | Ja | Die Anzahl der Warnungen, die beim Versuch des Vorgangs generiert wurden, Metadaten festzulegen. |
| `*`errorCount`*` | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, Metadaten festzulegen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details, die mit den Assets verknüpft sind, die Warnungen generieren, wenn der Vorgang versucht hat, Metadaten für die Assets im Stapelverfahren festzulegen. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Fehler generiert haben, wenn der Vorgang versucht hat, Metadaten für die Assets im Stapelverfahren festzulegen. |

## Beispiele {#section-2de798ac920e4b47b971b1729a64395b}

**Anforderung**

```java
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

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```

