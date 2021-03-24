---
description: Ein Benutzer von Ressourcen und Typen im System.
solution: Experience Manager
title: Benutzer
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# Benutzer{#user}

Ein Benutzer von Ressourcen und Typen im System.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | Benutzerhandle. |
| `*`firstName`*` | `xsd:string` | Vorname des Benutzers |
| `*`lastName`*` | `xsd:string` | Nachname des Benutzers |
| `*`E-Mail`*` | `xsd:string` | E-Mail-Adresse. |
| `*`defaultRole`*` | `xsd:string` | Legt die Rolle eines Benutzers in jeder Firma fest, zu der er gehört. Die Benutzerrolle `IpsAmin` überschreibt jedoch andere Benutzerrollen. |
| `*`isValid`*` | `xsd:boolean` | Bestimmt, ob der Benutzer gültig ist. |
| `*`passwordExpires`*` | `xsd:dateTime` | Legt das Ablaufdatum des Kennworts fest. |

