---
description: Speicherplatzstatistiken für ein Asset oder einen Ordner.
seo-description: Speicherplatzstatistiken für ein Asset oder einen Ordner.
seo-title: DiskUsage
solution: Experience Manager
title: DiskUsage
topic: Scene7 Image Production System API
uuid: a63f0ed0-c689-43b0-9c3e-9500715d15a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---


# DiskUsage{#diskusage}

Speicherplatzstatistiken für ein Asset oder einen Ordner.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Firma Handle. |
| ` *`companyName`*` | `xsd:string` | Name des Unternehmens. |
| ` *`imageCount`*` | `xsd:int` | Anzahl der gespeicherten Bilder. |
| ` *`diskSpaceUsage`*` | `xsd:long` | Gesamte Dateiseite in Kilobyte. |
| ` *`lastModified`*` | `xsd:dateTime` | Datum, Uhrzeit und Zeitzone, an denen der Typ `DiskUsage` zuletzt geändert wurde. |

