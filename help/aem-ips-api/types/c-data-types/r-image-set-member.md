---
description: Assets, die zu einem Bildset gehören.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Bildsets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# ImageSetMember{#imagesetmember}

Assets, die zu einem Bildset gehören.

Seitenrücksetzung bedeutet, dass ein [!DNL eCatalog] eine neue Seite starten sollte. `RenderSet` zeigt an, dass es Teil eines  `RenderSet` Farb-/Bildmusters ist. Der Wert wird für `eCatalog`- und `RenderSet`-Sets auf `true` erzwungen.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`asset`*` | `type:Asset` | Assets im Bildset-Array. |
| `*`pageReset`*` | `xsd:boolean` | Startet eine neue Seite. Einstellung wird ignoriert und der Wert für `eCatalog`- und `RenderSet`-Sets wird auf `true` erzwungen. |
