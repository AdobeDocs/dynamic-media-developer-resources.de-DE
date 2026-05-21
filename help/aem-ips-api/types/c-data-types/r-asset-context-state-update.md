---
title: AssetContextStateUpdate
description: Legen Sie einen neuen Satz von Veröffentlichungsstatus-Flags für den Veröffentlichungskontext fest, der mit einem Asset verknüpft ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
TQID: 'https://experienceleague.adobe.com/FYrAYgX9jmgxDsajc7PLH4BW-FCpS1bU0ONUQUkRSV8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 62
ht-degree: 4%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

Legen Sie einen neuen Satz von Veröffentlichungsstatus-Flags für den Veröffentlichungskontext fest, der mit einem Asset verknüpft ist.

**Parameter**

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Verarbeiten Sie das Asset, das Sie aktualisieren möchten. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | Ein Array von Status der Veröffentlichungskontakte für das Asset, das Sie aktualisieren möchten. |
