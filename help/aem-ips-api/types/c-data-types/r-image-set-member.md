---
description: Assets, die zu einem Bildsatz gehören.
seo-description: Assets, die zu einem Bildsatz gehören.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
feature: Dynamic Media Classic, SDK/API, Bildsätze
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# ImageSetMember{#imagesetmember}

Assets, die zu einem Bildsatz gehören.

Beim Zurücksetzen der Seite wird mit einem [!DNL eCatalog] eine neue Seite Beginn. `RenderSet` gibt an, dass es Teil eines  `RenderSet` Farbfelds ist. Der Wert wird für `eCatalog`- und `RenderSet`-Sätze auf `true` gezwungen.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`asset`*` | `type:Asset` | Assets im Bildsatz-Array. |
| `*`pageReset`*` | `xsd:boolean` | Beginn einer neuen Seite. Die Einstellung wird ignoriert und der Wert wird für `eCatalog`- und `RenderSet`-Sätze auf `true` gezwungen. |

