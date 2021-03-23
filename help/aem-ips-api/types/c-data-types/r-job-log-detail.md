---
description: Auftragsprotokollinformationen.
seo-description: Auftragsprotokollinformationen.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

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

