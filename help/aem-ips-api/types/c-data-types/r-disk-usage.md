---
description: Speicherplatzstatistiken für ein Asset oder einen Ordner.
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

---

# DiskUsage{#diskusage}

Speicherplatzstatistiken für ein Asset oder einen Ordner.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Handle des Unternehmens. |
| `*`companyName`*` | `xsd:string` | Name des Unternehmens. |
| `*`imageCount`*` | `xsd:int` | Anzahl der gespeicherten Bilder. |
| `*`diskSpaceUsage`*` | `xsd:long` | Gesamte Dateiseite in Kilobyte. |
| `*`lastModified`*` | `xsd:dateTime` | Datum, Uhrzeit und Zeitzone, in der der Typ `DiskUsage` zuletzt geändert wurde. |
