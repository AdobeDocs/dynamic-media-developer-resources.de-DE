---
description: Assets, die zu einem Bildset gehören.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
TQID: 'https://experienceleague.adobe.com/53rc6Cq1i15GdzOpBek7ls7ixq4RN8z0OfZMOZsqYWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

Assets, die zu einem Bildset gehören.

Das Zurücksetzen einer Seite bedeutet, dass ein [!DNL eCatalog] eine neue Seite starten sollte. `RenderSet` gibt an, dass es Teil eines `RenderSet` Farbfelds ist. Der Wert wird gezwungen, für `eCatalog` und `RenderSet` Sets zu `true`.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| asset | `type:Asset` | Assets im Bildset-Array. |
| pageReset | `xsd:boolean` | Startet eine neue Seite. Die Einstellung wird ignoriert, und der Wert wird gezwungen, für `eCatalog`- und `RenderSet`-Sets zu `true`. |

