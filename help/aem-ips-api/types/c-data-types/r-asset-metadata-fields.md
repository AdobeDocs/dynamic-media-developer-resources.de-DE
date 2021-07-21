---
description: Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadaten,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# AssetMetadataFields{#assetmetadatafields}

Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.

Syntax

## Parameter {#section-5ad771540c5f40c187b35e34aac19305}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Asset-Typ, der mit Felddefinitionen verknüpft ist (Werte finden Sie unter &quot;Asset-Typen&quot;). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Array von Metadatenfelddefinitionen, die mit dem in `assetType` angegebenen Asset-Typ verknüpft sind. |
