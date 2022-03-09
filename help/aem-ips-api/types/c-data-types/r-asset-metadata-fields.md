---
title: AssetMetadataFields
description: Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 10%

---

# AssetMetadataFields{#assetmetadatafields}

Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.

Syntax

## Parameter {#section-5ad771540c5f40c187b35e34aac19305}

| Name | Typ | Beschreibung |
|---|---|---|
| assetType | `xsd:string` | Asset-Typ, der mit Felddefinitionen verknüpft ist (Werte finden Sie unter &quot;Asset-Typen&quot;). |
| fieldArray | `types:MetadataFieldArray` | Array von Metadatenfelddefinitionen, die mit dem in `assetType`. |
