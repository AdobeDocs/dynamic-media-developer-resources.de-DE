---
description: Warn- oder Fehlerdetails für ein sing-Update in einem batchSetAssetMetadata-Vorgang.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 10%

---


# SetMetadataFault{#setmetadatafault}

Warn- oder Fehlerdetails für ein sing-Update in einem batchSetAssetMetadata-Vorgang.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Das Asset, dessen Metadaten nicht erfolgreich eingestellt wurden. |
| `*`fieldHandle`*` | `xsd:string` | Das Handle für das Metadatenfeld, dessen Wert nicht erfolgreich festgelegt wurde. |
| `*`Code`*` | `xsd:int` | Fehlercode. |
| `*`Grund`*` | `xsd:string` | Fehlerbeschreibung (Nur-Text). |

