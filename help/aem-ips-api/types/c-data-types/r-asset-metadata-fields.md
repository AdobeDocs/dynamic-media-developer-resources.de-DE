---
description: Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.
seo-description: Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
topic: Scene7 Image Production System API
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetMetadataFields{#assetmetadatafields}

Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.

Syntax

## Parameter {#section-5ad771540c5f40c187b35e34aac19305}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`assetType`*` | `xsd:string` | Mit Felddefinitionen verknüpfter Asset-Typ (für Werte siehe &quot;Asset-Typen&quot;). |
| ` *`fieldArray`*` | `types:MetadataFieldArray` | Array von Metadatenfelddefinitionen, die mit dem in `assetType`angegebenen Asset-Typ verbunden sind. |

