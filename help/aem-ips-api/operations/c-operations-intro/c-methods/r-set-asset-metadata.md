---
description: Legt Metadatenwerte für ein Asset fest. Funktioniert mit einem Array von Metadaten-Aktualisierungen, um Werte in einem Stapel festzulegen.
seo-description: Legt Metadatenwerte für ein Asset fest. Funktioniert mit einem Array von Metadaten-Aktualisierungen, um Werte in einem Stapel festzulegen.
seo-title: setAssetMetadata
solution: Experience Manager
title: setAssetMetadata
topic: Dynamic Media Image Production System API
uuid: 17fe8277-a164-4f91-af96-ea43d41bd4f2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '143'
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
