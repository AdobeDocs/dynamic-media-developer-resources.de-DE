---
description: Assets, die zu einem Bildset gehören.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

Assets, die zu einem Bildset gehören.

Das Zurücksetzen einer Seite bedeutet, dass ein [!DNL eCatalog] eine neue Seite starten sollte. `RenderSet` gibt an, dass es Teil eines `RenderSet` Farbfelds ist. Der Wert wird gezwungen, für `true` und `eCatalog` Sets zu `RenderSet`.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| asset | `type:Asset` | Assets im Bildset-Array. |
| pageReset | `xsd:boolean` | Startet eine neue Seite. Die Einstellung wird ignoriert, und der Wert wird gezwungen, für `true`- und `eCatalog`-Sets zu `RenderSet`. |
