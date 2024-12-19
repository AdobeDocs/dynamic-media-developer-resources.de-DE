---
description: Ein Benutzer von Ressourcen und Typen im System.
solution: Experience Manager
title: Benutzer
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---

# [!DNL User]{#user}

Ein Benutzer von Ressourcen und Typen im System.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| userHandle | `xsd:string` | Benutzerhandle. |
| firstName | `xsd:string` | Vorname des Benutzers. |
| lastName | `xsd:string` | Nachname des Benutzers. |
| E-Mail | `xsd:string` | E-Mail-Adresse. |
| defaultRole | `xsd:string` | Legt die Rolle eines Benutzers in jedem Unternehmen fest, dem er angehört. Die Benutzerrolle überschreibt jedoch `IpsAmin` andere Benutzerrollen. |
| isValid | `xsd:boolean` | Bestimmt, ob der Benutzer gültig ist. |
| passwordExpires | `xsd:dateTime` | Legt das Ablaufdatum des Passworts fest. |
