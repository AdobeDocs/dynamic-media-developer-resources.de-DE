---
title: AssetContextStateUpdate
description: Legen Sie einen neuen Satz von Veröffentlichungsstatus-Flags für den Veröffentlichungskontext fest, der mit einem Asset verknüpft ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 6%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

Legen Sie einen neuen Satz von Veröffentlichungsstatus-Flags für den Veröffentlichungskontext fest, der mit einem Asset verknüpft ist.

**Parameter**

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Behandeln Sie das Asset, das Sie aktualisieren möchten. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | Ein Array von Veröffentlichungskontaktstatus für das Asset, das Sie aktualisieren möchten. |
