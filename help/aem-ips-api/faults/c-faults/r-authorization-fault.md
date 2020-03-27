---
description: Wird ausgelöst, wenn ein authentifizierter Benutzer nicht über ausreichende Berechtigungen zum Ausführen einer Aufgabe verfügt.
seo-description: Wird ausgelöst, wenn ein authentifizierter Benutzer nicht über ausreichende Berechtigungen zum Ausführen einer Aufgabe verfügt.
seo-title: authorizedFault
solution: Experience Manager
title: authorizedFault
topic: Scene7 Image Production System API
uuid: 8b8df22a-aa76-4cbd-9c14-89969c5f9620
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# authorizedFault{#authorizationfault}

Wird ausgelöst, wenn ein authentifizierter Benutzer nicht über ausreichende Berechtigungen zum Ausführen einer Aufgabe verfügt.

Syntax

## Fehlertypen {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | Fehler |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 20001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 20002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 20003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 20004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 20005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 20006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 20007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 20008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 20009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## Standardfelder {#section-4e3e41f41fea402a9ae314bfd05f663e}

| Name | Typ | Beschreibung |
|---|---|---|
| `code` | `xsd:int` | Fehler-ID |
| `reason` | `xsd:string` | Eine informative Meldung, die den Fehler beschreibt. |

