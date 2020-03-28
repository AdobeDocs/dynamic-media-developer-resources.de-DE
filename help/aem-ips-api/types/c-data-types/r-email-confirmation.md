---
description: Sendet eine E-Mail an einen angegebenen Empfänger als Antwort auf einen cdnCacheInvalidation-Vorgang.
seo-description: Sendet eine E-Mail an einen angegebenen Empfänger als Antwort auf einen cdnCacheInvalidation-Vorgang.
seo-title: EmailConfirmation
solution: Experience Manager
title: EmailConfirmation
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# EmailConfirmation{#emailconfirmation}

Sendet eine E-Mail an einen angegebenen Empfänger als Antwort auf einen cdnCacheInvalidation-Vorgang.

Syntax

## Parameter {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | Wenn &quot;true&quot;, enthält das Benutzerkonto des Webdiensts, bei dem es sich um eine Liste von E-Mails handelt, die eine E-Mail-Bestätigung vom Scene7-CDN erhalten sollen. |
| ` *`ccOthersArray`*` | `types:EmailArray` | Ein Array von E-Mail-Adressen (maximal 5), die für den Empfang der Bestätigungsbenachrichtigung vom Scene7-CDN vorgesehen sind. |

