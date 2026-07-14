---
description: Aktualisiert das einem Bild-Asset zugeordnete Bildfeld.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
TQID: 'https://experienceleague.adobe.com/IsOZvDzvJTa0KJfUkYblEln9Qrx7nQm79FEEbnFVjiw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 56
ht-degree: 8%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

Aktualisiert das einem Bild-Asset zugeordnete Bildfeld.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Asset-Handle. |
| [!DNL resolution] | `xsd:double` | Bildauflösung in Pixel pro Zoll. |
| [!DNL anchorX] | `xsd:int` | X-Achsen-Bildanker. |
| [!DNL anchorY] | `xsd:int` | Bildanker der Y-Achse. |
| [!DNL userData] | `xsd:string` | Wert `userData` Metadatenfelds, der im Feld „Image Serving User Data Catalog“ veröffentlicht wird. |

