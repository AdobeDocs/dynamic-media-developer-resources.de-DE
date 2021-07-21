---
description: Warn- oder Fehlerdetails für ein Sling-Update in einem batchSetAssetMetadata-Vorgang.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadaten
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 10%

---

# SetMetadataFault{#setmetadatafault}

Warn- oder Fehlerdetails für ein Sling-Update in einem batchSetAssetMetadata-Vorgang.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Das Asset, dessen Metadaten nicht erfolgreich festgelegt wurden. |
| `*`fieldHandle`*` | `xsd:string` | Der Handle für das Metadatenfeld, dessen Wert nicht erfolgreich festgelegt wurde. |
| `*`Code`*` | `xsd:int` | Fehler-Code. |
| `*`Grund`*` | `xsd:string` | Fehlerbeschreibung (Nur-Text). |
