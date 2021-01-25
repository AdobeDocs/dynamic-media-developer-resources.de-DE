---
description: Auftragsprotokollinformationen.
seo-description: Auftragsprotokollinformationen.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
topic: Dynamic Media Image Production System API
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 7%

---


# JobLogDetail{#joblogdetail}

Auftragsprotokollinformationen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Meldungen im Auftragsprotokoll. |
| `*`logType`*` | `xsd:string` | Auftragsprotokolldateityp. |
| `*`assetName`*` | `xsd:string` | Name des Assets im Auftragsprotokoll (optional). |
| `*`assetType`*` | `xsd:string` | Auswahl des Asset-Typs. |
| `*`assetHandle`*` | `xsd:string` | Asset-Handle, auf die im Auftragsprotokoll verwiesen wird. |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | Bietet zusätzliche detaillierte Auftragsprotokollinformationen, die über die oben beschriebenen fünf Auftragsprotokolltypen hinausgehen. |

