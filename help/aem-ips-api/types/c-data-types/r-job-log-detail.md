---
description: Auftragsprotokollinformationen.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---

# JobLogDetail{#joblogdetail}

Auftragsprotokollinformationen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| logMessage | `xsd:string` | Nachrichten im Auftragsprotokoll. |
| logType | `xsd:string` | Auftragsprotokolldateityp. |
| assetName | `xsd:string` | Name des Assets im Auftragsprotokoll (optional). |
| assetType | `xsd:string` | Auswahl des Asset-Typs. |
| assetHandle | `xsd:string` | Asset-Handle, auf die im Auftragsprotokoll verwiesen wird. |
| auxArray | `types:JobLogDetailAuxArray` | Bietet zusätzliche detaillierte Auftragsprotokollinformationen, die über die oben beschriebenen fünf Auftragsprotokolltypen hinausgehen. |
