---
description: Benutzer von Ressourcen und Typen im System.
solution: Experience Manager
title: Benutzer
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# Benutzer{#user}

Benutzer von Ressourcen und Typen im System.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| userHandle | `xsd:string` | Benutzerhandbuch. |
| firstName | `xsd:string` | Vorname des Benutzers. |
| lastName | `xsd:string` | Nachname des Benutzers. |
| E-Mail | `xsd:string` | E-Mail-Adresse. |
| defaultRole | `xsd:string` | Legt die Rolle für einen Benutzer in jedem Unternehmen fest, zu dem er gehört. Die Benutzerrolle `IpsAmin` überschreibt andere Benutzerrollen. |
| isValid | `xsd:boolean` | Bestimmt, ob der Benutzer gültig ist. |
| passwordExpires | `xsd:dateTime` | Legt das Ablaufdatum des Kennworts fest. |
