---
description: Ein Benutzer von Ressourcen und Typen im System.
seo-description: Ein Benutzer von Ressourcen und Typen im System.
seo-title: Benutzer
solution: Experience Manager
title: Benutzer
topic: Scene7 Image Production System API
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Benutzer{#user}

Ein Benutzer von Ressourcen und Typen im System.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Benutzerhandle. |
| ` *`firstName`*` | `xsd:string` | Vorname des Benutzers |
| ` *`lastName`*` | `xsd:string` | Nachname des Benutzers |
| ` *`E-Mail`*` | `xsd:string` | E-Mail-Adresse. |
| ` *`defaultRole`*` | `xsd:string` | Legt die Rolle eines Benutzers in jeder Firma fest, zu der er gehört. Die Benutzerrolle setzt jedoch andere Benutzerrollen `IpsAmin` außer Kraft. |
| ` *`isValid`*` | `xsd:boolean` | Bestimmt, ob der Benutzer gültig ist. |
| ` *`passwordExpires`*` | `xsd:dateTime` | Legt das Ablaufdatum des Kennworts fest. |

