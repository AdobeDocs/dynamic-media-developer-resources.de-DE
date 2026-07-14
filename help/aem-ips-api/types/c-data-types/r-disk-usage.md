---
description: Statistik zum Festplattenspeicher für ein Asset oder einen Ordner.
solution: Experience Manager
title: Festplattenauslastung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
TQID: 'https://experienceleague.adobe.com/Md0oAgpJDqSrn1JRZsebpaZKeXIAoLcgkC5KPaHad5s'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 50
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

