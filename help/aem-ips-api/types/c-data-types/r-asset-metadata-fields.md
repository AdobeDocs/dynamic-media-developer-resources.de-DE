---
title: AssetMetadataFields
description: Gibt Metadatenfelddefinitionen für angegebene Asset-Typen zurück.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
TQID: 'https://experienceleague.adobe.com/U9JVe27HBTMtlBXmwDnkVAOaVfsBspa5r5fvnQl-h58'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 47
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

Gibt Metadatenfelddefinitionen für angegebene Asset-Typen zurück.

Syntax

## Parameter {#section-5ad771540c5f40c187b35e34aac19305}

| Name | Typ | Beschreibung |
|---|---|---|
| assetType | `xsd:string` | Mit Felddefinitionen verknüpfter Asset-Typ (Werte finden Sie unter „Asset-Typen„). |
| fieldArray | `types:MetadataFieldArray` | Array von Metadatenfelddefinitionen, die mit dem in `assetType` angegebenen Asset-Typ verknüpft sind. |
