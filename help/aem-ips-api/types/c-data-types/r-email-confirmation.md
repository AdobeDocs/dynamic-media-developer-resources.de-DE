---
description: Sendet als Antwort auf einen cdnCacheInvalidation-Vorgang eine E-Mail an einen angegebenen Empfänger.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
TQID: 'https://experienceleague.adobe.com/h9ZZRR0zR347mzSifomCmtNW5GorTC6fgGjeSRf52KU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

Sendet als Antwort auf einen cdnCacheInvalidation-Vorgang eine E-Mail an einen angegebenen Empfänger.

Syntax

## Parameter {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Name | Typ | Beschreibung |
|---|---|---|
| ccOriginator | `xsd:boolean` | Wenn „true“, enthält das Web-Service-Benutzerkonto des Benutzers, d. h. eine Liste von E-Mails, die zum Empfang einer E-Mail-Bestätigung vom Dynamic Media CDN vorgesehen sind. |
| ccOthersArray | `types:EmailArray` | Ein Array von E-Mail-Adressen (maximal 5), die für den Empfang der Bestätigungsbenachrichtigung vom Dynamic Media CDN vorgesehen sind. |
