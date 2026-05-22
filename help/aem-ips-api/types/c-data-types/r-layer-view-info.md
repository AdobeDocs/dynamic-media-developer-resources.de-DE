---
description: Eigenschaften der Ebenenansicht.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
TQID: 'https://experienceleague.adobe.com/cx-B-BmcEP6vefJY5tsrNMZcwWIKM-pW0CYfP7BjxMM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 46
ht-degree: 13%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Eigenschaften der Ebenenansicht.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| url | `xsd:string` | Bildserver-URL, die die Vorlage darstellt. Kombiniert `urlModifier`- und `urlPostAp- plyModifier`. |
| urlModifier | `xsd:string` | Image-Serving-Protokollbefehle, die vor der Anforderung oder dem `urlPostApplyModifier` angewendet werden sollen. |
| urlPostApplyModifier | `xsd:string` | Image-Serving-Protokollbefehle, die nach `urlModifier`- und Anforderungsbefehlen angewendet werden sollen. |
