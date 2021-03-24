---
description: Assets, die zu einem Bildsatz gehören.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic, SDK/API, Bildsätze
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# ImageSetMember{#imagesetmember}

Assets, die zu einem Bildsatz gehören.

Beim Zurücksetzen der Seite wird mit einem [!DNL eCatalog] eine neue Seite Beginn. `RenderSet` gibt an, dass es Teil eines  `RenderSet` Farbfelds ist. Der Wert wird für `eCatalog`- und `RenderSet`-Sätze auf `true` gezwungen.

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`asset`*` | `type:Asset` | Assets im Bildsatz-Array. |
| `*`pageReset`*` | `xsd:boolean` | Beginn einer neuen Seite. Die Einstellung wird ignoriert und der Wert wird für `eCatalog`- und `RenderSet`-Sätze auf `true` gezwungen. |

