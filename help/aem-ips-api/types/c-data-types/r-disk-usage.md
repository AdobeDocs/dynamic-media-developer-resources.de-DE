---
description: Speicherplatzstatistiken für ein Asset oder einen Ordner.
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 12%

---


# DiskUsage{#diskusage}

Speicherplatzstatistiken für ein Asset oder einen Ordner.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Firma Handle. |
| `*`companyName`*` | `xsd:string` | Name des Unternehmens. |
| `*`imageCount`*` | `xsd:int` | Anzahl der gespeicherten Bilder. |
| `*`diskSpaceUsage`*` | `xsd:long` | Gesamte Dateiseite in Kilobyte. |
| `*`lastModified`*` | `xsd:dateTime` | Datum, Uhrzeit und Zeitzone, an denen der Typ `DiskUsage` zuletzt geändert wurde. |

