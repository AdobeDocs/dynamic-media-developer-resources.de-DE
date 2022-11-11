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

Seitenrücksetzung bedeutet, dass eine [!DNL eCatalog] eine neue Seite starten. `RenderSet` gibt an, dass es Teil eines `RenderSet` Muster. Der Wert muss `true` für `eCatalog` und `RenderSet` Sets.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| asset | `type:Asset` | Assets im Bildset-Array. |
| pageReset | `xsd:boolean` | Startet eine neue Seite. Einstellung wird ignoriert und Wert wird erzwungen `true` für `eCatalog` und `RenderSet` Sets. |
