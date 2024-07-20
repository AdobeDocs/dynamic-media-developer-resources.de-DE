---
title: AssetMetadataFields
description: Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

Gibt Metadatenfelddefinitionen für bestimmte Asset-Typen zurück.

Syntax

## Parameter {#section-5ad771540c5f40c187b35e34aac19305}

| Name | Typ | Beschreibung |
|---|---|---|
| assetType | `xsd:string` | Asset-Typ, der mit Felddefinitionen verknüpft ist (Werte finden Sie unter &quot;Asset-Typen&quot;). |
| fieldArray | `types:MetadataFieldArray` | Array von Metadatenfelddefinitionen, die mit dem in `assetType` angegebenen Asset-Typ verknüpft sind. |
