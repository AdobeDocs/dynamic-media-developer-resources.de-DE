---
description: Auftragsprotokollinformationen.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
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

