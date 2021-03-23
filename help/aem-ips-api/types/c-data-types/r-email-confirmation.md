---
description: Sendet eine E-Mail an einen angegebenen Empfänger als Antwort auf einen cdnCacheInvalidation-Vorgang.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# EmailConfirmation{#emailconfirmation}

Sendet eine E-Mail an einen angegebenen Empfänger als Antwort auf einen cdnCacheInvalidation-Vorgang.

Syntax

## Parameter {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Wenn &quot;true&quot;, enthält das Benutzerkonto des Webdiensts, bei dem es sich um eine Liste von E-Mails handelt, die eine E-Mail-Bestätigung vom Dynamic Media CDN erhalten sollen. |
| `*`ccOthersArray`*` | `types:EmailArray` | Ein Array von E-Mail-Adressen (maximal 5), die für den Empfang der Bestätigungsbenachrichtigung vom Dynamic Media CDN vorgesehen sind. |

