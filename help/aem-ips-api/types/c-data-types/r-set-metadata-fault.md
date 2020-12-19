---
description: Warn- oder Fehlerdetails für ein sing-Update in einem batchSetAssetMetadata-Vorgang.
seo-description: Warn- oder Fehlerdetails für ein sing-Update in einem batchSetAssetMetadata-Vorgang.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Scene7 Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---


# SetMetadataFault{#setmetadatafault}

Warn- oder Fehlerdetails für ein sing-Update in einem batchSetAssetMetadata-Vorgang.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Das Asset, dessen Metadaten nicht erfolgreich eingestellt wurden. |
| ` *`fieldHandle`*` | `xsd:string` | Das Handle für das Metadatenfeld, dessen Wert nicht erfolgreich festgelegt wurde. |
| ` *`Code`*` | `xsd:int` | Fehlercode. |
| ` *`Grund`*` | `xsd:string` | Fehlerbeschreibung (Nur-Text). |

