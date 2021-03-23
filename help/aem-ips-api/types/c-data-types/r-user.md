---
description: Ein Benutzer von Ressourcen und Typen im System.
seo-description: Ein Benutzer von Ressourcen und Typen im System.
seo-title: Benutzer
solution: Experience Manager
title: Benutzer
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
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

