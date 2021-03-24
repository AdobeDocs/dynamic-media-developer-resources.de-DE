---
description: Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic, SDK/API, Metadaten, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 8%

---


# AssetMetadataFields{#assetmetadatafields}

Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.

Syntax

## Parameter {#section-5ad771540c5f40c187b35e34aac19305}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Mit Felddefinitionen verknüpfter Asset-Typ (für Werte siehe &quot;Asset-Typen&quot;). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Array von Metadatenfelddefinitionen, die mit dem in `assetType` angegebenen Asset-Typ verknüpft sind. |

