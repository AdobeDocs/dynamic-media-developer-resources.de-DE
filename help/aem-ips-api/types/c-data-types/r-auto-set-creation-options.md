---
description: Automatische Skriptliste zur Set-Generierung für Upload-Aufträge. Dabei wird davon ausgegangen, dass jedes für den Upload angegebene Skript auf alle hochgeladenen Assets angewendet wird.
solution: Experience Manager
title: AutoSetCreationOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e6e969be-0410-4be7-88d6-491d715fd137
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# AutoSetCreationOptions{#autosetcreationoptions}

Automatische Skriptliste zur Set-Generierung für Upload-Aufträge. Dabei wird davon ausgegangen, dass jedes für den Upload angegebene Skript auf alle hochgeladenen Assets angewendet wird.

Syntax

## Parameter {#section-0302e9238dbc4704914e938f42c881e6}

| Name | Typ | Beschreibung |
|---|---|---|
| autoSetsArray | `types:HandleArray` | Array von [!DNL PropertySet] behandelt das Definieren der automatischen Skripte zur Set-Erstellung, die während des Uploads angewendet werden. |
