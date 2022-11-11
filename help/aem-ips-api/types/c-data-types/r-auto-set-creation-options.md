---
description: Automatische Skriptliste zur Set-Generierung für Upload-Aufträge. Dabei wird davon ausgegangen, dass jedes für den Upload angegebene Skript auf alle hochgeladenen Assets angewendet wird.
solution: Experience Manager
title: AutoSetCreationOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e6e969be-0410-4be7-88d6-491d715fd137
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 7%

---

# [!DNL AutoSetCreationOptions]{#autosetcreationoptions}

Automatische Skriptliste zur Set-Generierung für Upload-Aufträge. Dabei wird davon ausgegangen, dass jedes für den Upload angegebene Skript auf alle hochgeladenen Assets angewendet wird.

Syntax

## Parameter {#section-0302e9238dbc4704914e938f42c881e6}

| Name | Typ | Beschreibung |
|---|---|---|
| autoSetsArray | `types:HandleArray` | Array von [!DNL PropertySet] behandelt das Definieren der automatischen Skripte zur Set-Erstellung, die während des Uploads angewendet werden. |
