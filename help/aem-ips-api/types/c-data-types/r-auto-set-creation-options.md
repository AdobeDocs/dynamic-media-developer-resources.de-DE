---
description: Automatische Skriptliste zur Set-Generierung für Upload-Aufträge. Dabei wird davon ausgegangen, dass jedes für den Upload angegebene Skript auf alle hochgeladenen Assets angewendet wird.
solution: Experience Manager
title: AutoSetCreationOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e6e969be-0410-4be7-88d6-491d715fd137
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 7%

---

# AutoSetCreationOptions{#autosetcreationoptions}

Automatische Skriptliste zur Set-Generierung für Upload-Aufträge. Dabei wird davon ausgegangen, dass jedes für den Upload angegebene Skript auf alle hochgeladenen Assets angewendet wird.

Syntax

## Parameter {#section-0302e9238dbc4704914e938f42c881e6}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`autoSetsArray`*` | `types:HandleArray` | Array von [!DNL PropertySet] verarbeitet das Definieren der automatischen Skripten zur Set-Generierung, die beim Hochladen angewendet werden. |
