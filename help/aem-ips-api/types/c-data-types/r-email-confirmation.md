---
description: Sendet als Antwort auf einen cdnCacheInvalidation-Vorgang eine E-Mail an einen angegebenen Empfänger.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '78'
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
