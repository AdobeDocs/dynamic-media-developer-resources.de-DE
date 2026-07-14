---
description: Verwaltet Rechte zum Zugreifen auf, Ändern, Erstellen oder Löschen von Assets nach Gruppe.
solution: Experience Manager
title: Erlaubnis
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
TQID: 'https://experienceleague.adobe.com/BfB4MGiJFqPkJqL26YSmrhd52KfxhVX5TC-LHxEhevo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 53
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

