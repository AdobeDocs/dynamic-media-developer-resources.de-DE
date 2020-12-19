---
description: Wird ausgelöst, wenn ein Benutzer nicht authentifiziert werden kann.
seo-description: Wird ausgelöst, wenn ein Benutzer nicht authentifiziert werden kann.
seo-title: authenticationFault
solution: Experience Manager
title: authenticationFault
topic: Scene7 Image Production System API
uuid: 89cc6f09-def6-4db1-a8b5-410909693dce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 17%

---


# authenticationFault{#authenticationfault}

Wird ausgelöst, wenn ein Benutzer nicht authentifiziert werden kann.

Syntax

## Fehlertypen {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | Fehler |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## Standardfelder {#section-1fe84846a7154b03ab49552810ee9ac3}

| Name | Typ | Beschreibung |
|---|---|---|
| `code` | `xsd:int` | Fehler-ID |
| `reason` | `xsd:string` | Eine informative Meldung, die den Fehler beschreibt. |

