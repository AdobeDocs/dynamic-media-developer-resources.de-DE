---
description: Wird ausgelöst, wenn ein authentifizierter Benutzer nicht über ausreichende Berechtigungen zum Ausführen einer Aufgabe verfügt.
solution: Experience Manager
title: authorizationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 76965735-92d8-46be-b589-67cad3b987dc
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 25%

---

# authorizationFault{#authorizationfault}

Wird ausgelöst, wenn ein authentifizierter Benutzer nicht über ausreichende Berechtigungen zum Ausführen einer Aufgabe verfügt.

Syntax

## Fehlertypen {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | Fehler |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 2001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 2002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 2003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 2004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 2005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 2006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 2007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 2008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 2009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## Standardfelder {#section-4e3e41f41fea402a9ae314bfd05f663e}

| Name | Typ | Beschreibung |
|---|---|---|
| `code` | `xsd:int` | Fehler-ID |
| `reason` | `xsd:string` | Eine informative Meldung, die den Fehler beschreibt. |
