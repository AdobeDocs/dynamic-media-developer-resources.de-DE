---
description: Ein Benutzer von Ressourcen und Typen im System.
solution: Experience Manager
title: Benutzer
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
TQID: 'https://experienceleague.adobe.com/XM-2FjVie-j71W3Sc3-TypNJUFnz5AQuZZuGOx1fePs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
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
