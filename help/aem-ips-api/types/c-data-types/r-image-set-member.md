---
description: Assets, die zu einem Bildsatz gehören.
seo-description: Assets, die zu einem Bildsatz gehören.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Scene7 Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 6%

---


# ImageSetMember{#imagesetmember}

Assets, die zu einem Bildsatz gehören.

Beim Zurücksetzen der Seite wird mit einem [!DNL eCatalog] eine neue Seite Beginn. `RenderSet` gibt an, dass es Teil eines  `RenderSet` Farbfelds ist. Der Wert wird für `eCatalog`- und `RenderSet`-Sätze auf `true` gezwungen.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`asset`*` | `type:Asset` | Assets im Bildsatz-Array. |
| ` *`pageReset`*` | `xsd:boolean` | Beginn einer neuen Seite. Die Einstellung wird ignoriert und der Wert wird für `eCatalog`- und `RenderSet`-Sätze auf `true` gezwungen. |

