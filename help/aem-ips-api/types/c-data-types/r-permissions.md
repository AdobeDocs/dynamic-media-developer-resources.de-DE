---
description: Verwaltet Rechte zum Zugreifen auf, Ändern, Erstellen oder Löschen von Assets nach Gruppe.
solution: Experience Manager
title: Erlaubnis
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 9%

---

# [!DNL Permission]{#permission}

Verwaltet Rechte zum Zugreifen auf, Ändern, Erstellen oder Löschen von Assets nach Gruppe.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| groupHandle | `xsd:string` | Gruppen-Handle. |
| groupName | `xsd:string` | Gruppenname. |
| permissionType | `xsd:string` | Auswahl des Berechtigungstyps. |
| isAllowed | `xsd:boolean` | Bestimmt, ob die Berechtigung zulässig ist. |
| isOverride | `xsd:boolean` | Legt fest, ob die Berechtigung eine andere überschreibt. |
