---
description: Vorgangslog-Informationen.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

Vorgangslog-Informationen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| LogMessage | `xsd:string` | Meldungen im Vorgangslog. |
| logType | `xsd:string` | Typ der Vorgangslog-Datei. |
| assetName | `xsd:string` | Name des Assets im Vorgangslog (optional). |
| assetType | `xsd:string` | Auswahl des Asset-Typs. |
| assetHandle | `xsd:string` | Asset-Handle, auf das im Vorgangsprotokoll verwiesen wird. |
| auxArray | `types:JobLogDetailAuxArray` | Bietet zusätzliche detaillierte Auftragsprotokollinformationen über die fünf oben beschriebenen Auftragsprotokolltypen hinaus. |
