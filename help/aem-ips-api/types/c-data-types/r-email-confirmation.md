---
description: Sendet eine E-Mail an einen angegebenen Empfänger als Antwort auf einen cdnCacheInvalidation-Vorgang.
solution: Experience Manager
title: EmailConfirmation
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# EmailConfirmation{#emailconfirmation}

Sendet eine E-Mail an einen angegebenen Empfänger als Antwort auf einen cdnCacheInvalidation-Vorgang.

Syntax

## Parameter {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Wenn &quot;true&quot;, enthält das Benutzerkonto des Webdiensts, bei dem es sich um eine Liste von E-Mails handelt, die eine E-Mail-Bestätigung vom Dynamic Media CDN erhalten sollen. |
| `*`ccOthersArray`*` | `types:EmailArray` | Ein Array von E-Mail-Adressen (maximal 5), die für den Empfang der Bestätigungsbenachrichtigung vom Dynamic Media CDN vorgesehen sind. |

