---
description: Beschreibt Berechtigungsänderungen.
seo-description: Beschreibt Berechtigungsänderungen.
seo-title: PermissionUpdate
solution: Experience Manager
title: PermissionUpdate
topic: Scene7 Image Production System API
uuid: 7b1850ca-6a8c-402d-8c8f-4528d978245f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '38'
ht-degree: 13%

---


# PermissionUpdate{#permissionupdate}

Beschreibt Berechtigungsänderungen.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | Gruppengriff. |
| ` *`permissionType`*` | `xsd:string` | Berechtigungstyp |
| ` *`isAllowed`*` | `xsd:boolean` | Bestimmt, ob die Berechtigungsaktualisierung zulässig ist. |
| ` *`isOverride`*` | `xsd:boolean` | Stellt fest, ob die Berechtigung eine andere überschreibt. |

