---
description: Sendet eine E-Mail an einen angegebenen Empfänger als Antwort auf einen cdnCacheInvalidation-Vorgang.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 6%

---

# EmailConfirmation{#emailconfirmation}

Sendet eine E-Mail an einen angegebenen Empfänger als Antwort auf einen cdnCacheInvalidation-Vorgang.

Syntax

## Parameter {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Wenn der Wert &quot;true&quot;lautet, enthält das Webdienst-Benutzerkonto des Benutzers, bei dem es sich um eine Liste von E-Mails handelt, die vom Dynamic Media-CDN per E-Mail bestätigt werden sollen. |
| `*`ccOthersArray`*` | `types:EmailArray` | Eine Gruppe von E-Mail-Adressen (maximal 5), die die Bestätigungsbenachrichtigung vom Dynamic Media CDN erhalten. |
