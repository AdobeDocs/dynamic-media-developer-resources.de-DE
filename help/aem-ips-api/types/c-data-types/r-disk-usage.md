---
description: Statistik zum Festplattenspeicher für ein Asset oder einen Ordner.
solution: Experience Manager
title: Festplattenauslastung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 10%

---

# [!DNL DiskUsage]{#diskusage}

Statistik zum Festplattenspeicher für ein Asset oder einen Ordner.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| companyHandle | `xsd:string` | Firmengriff. |
| companyName | `xsd:string` | Firmenname. |
| imageCount | `xsd:int` | Anzahl der gespeicherten Bilder. |
| diskSpaceUsage | `xsd:long` | Gesamte Dateiseite in Kilobyte. |
| lastModify | `xsd:dateTime` | Datum, Uhrzeit und Zeitzone der letzten Änderung des `DiskUsage`. |
