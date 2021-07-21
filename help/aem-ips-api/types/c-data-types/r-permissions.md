---
description: Verwaltet Berechtigungen zum Zugriff, Ändern, Erstellen oder Löschen von Assets nach Gruppe.
solution: Experience Manager
title: Berechtigung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 8%

---

# Berechtigung{#permission}

Verwaltet Berechtigungen zum Zugriff, Ändern, Erstellen oder Löschen von Assets nach Gruppe.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Gruppieren. |
| `*`groupName`*` | `xsd:string` | Gruppenname. |
| `*`permissionType`*` | `xsd:string` | Auswahl des Berechtigungstyps. |
| `*`isAllowed`*` | `xsd:boolean` | Bestimmt, ob die Berechtigung zulässig ist. |
| `*`isOverride`*` | `xsd:boolean` | Bestimmt, ob die Berechtigung eine andere überschreibt. |
