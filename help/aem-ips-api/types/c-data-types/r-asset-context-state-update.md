---
title: AssetContextStateUpdate
description: Legen Sie einen neuen Satz von Veröffentlichungsstatus-Flags für den Veröffentlichungskontext fest, der mit einem Asset verknüpft ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

Legen Sie einen neuen Satz von Veröffentlichungsstatus-Flags für den Veröffentlichungskontext fest, der mit einem Asset verknüpft ist.

**Parameter**

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Verarbeiten Sie das Asset, das Sie aktualisieren möchten. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | Ein Array von Status der Veröffentlichungskontakte für das Asset, das Sie aktualisieren möchten. |
