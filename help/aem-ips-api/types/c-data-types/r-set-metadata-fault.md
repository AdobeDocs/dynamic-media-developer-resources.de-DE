---
description: Warn- oder Fehlerdetails für eine Verwendung der Aktualisierung in einem batchSetAssetMetadata-Vorgang.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 12%

---

# [!DNL SetMetadataFault]{#setmetadatafault}

Warn- oder Fehlerdetails für eine Verwendung der Aktualisierung in einem batchSetAssetMetadata-Vorgang.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Das Asset, dessen Metadaten nicht erfolgreich festgelegt wurden. |
| fieldHandle | `xsd:string` | Das Handle zum Metadatenfeld, dessen Wert nicht erfolgreich festgelegt wurde. |
| Code | `xsd:int` | Fehlercode. |
| Grund | `xsd:string` | Fehlerbeschreibung (Nur-Text). |
