---
description: Legt Metadatenwerte für ein Asset fest. Funktioniert mit einem Array von Metadaten-Aktualisierungen, um Werte in einem Stapel festzulegen.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic, SDK/API, Metadaten, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setAssetMetadata{#setassetmetadata}

Legt Metadatenwerte für ein Asset fest. Funktioniert mit einem Array von Metadaten-Aktualisierungen, um Werte in einem Stapel festzulegen.

Syntax

## Autorisierte Benutzertypen {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss über Lesezugriff auf das Asset verfügen.

## Parameter {#section-bcdcff30905e444388811e897b2824bd}

**Input (setAssetMetadataParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle zur Firma mit dem Asset, das Sie aktualisieren möchten. |
| `*`assetHandle`*` | `xsd:string` | Ja | Das Handle für das Asset. |
| `*`updateArray`*` | `types:MetadataUpdateArray` | Ja | Aktualisierungen in einem Metadaten-Aktualisierungsarray. |

**Output (setAssetMetadataReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-1ab412e7ee1d4d6d8469b0b403598c42}

Dieses Codebeispiel verwendet ein Array von Metadaten-Aktualisierungen, um die Metadaten des angegebenen Assets festzulegen.

**Anforderung**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Antwort**

Keine.
