---
description: Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.
seo-description: Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
feature: Dynamic Media Classic, SDK/API, Metadaten, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---


# AssetMetadataFields{#assetmetadatafields}

Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.

Syntax

## Parameter {#section-5ad771540c5f40c187b35e34aac19305}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Mit Felddefinitionen verknüpfter Asset-Typ (für Werte siehe &quot;Asset-Typen&quot;). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Array von Metadatenfelddefinitionen, die mit dem in `assetType` angegebenen Asset-Typ verknüpft sind. |

