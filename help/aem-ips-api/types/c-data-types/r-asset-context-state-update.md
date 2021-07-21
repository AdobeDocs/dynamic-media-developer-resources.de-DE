---
description: Legen Sie einen neuen Satz von Veröffentlichungsstatus-Flags für den Veröffentlichungskontext fest, der mit einem Asset verknüpft ist.
solution: Experience Manager
title: AssetContextStateUpdate
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

Legen Sie einen neuen Satz von Veröffentlichungsstatus-Flags für den Veröffentlichungskontext fest, der mit einem Asset verknüpft ist.

**Parameter**

| Name | Typ | Beschreibung |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Behandeln Sie das Asset, das Sie aktualisieren möchten. |
| `*`contextStateUpdateArray`*` | `types:ContextStateUpdateArray` | Ein Array von Veröffentlichungskontaktstatus für das Asset, das Sie aktualisieren möchten. |
