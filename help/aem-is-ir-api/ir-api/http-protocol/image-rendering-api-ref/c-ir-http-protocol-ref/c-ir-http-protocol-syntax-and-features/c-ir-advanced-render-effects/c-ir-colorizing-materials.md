---
description: Die meisten Materialien können dynamisch eingefärbt werden.
seo-description: Die meisten Materialien können dynamisch eingefärbt werden.
seo-title: Färben von Materialien
solution: Experience Manager
title: Färben von Materialien
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Färben von Materialien{#colorizing-materials}

Die meisten Materialien können dynamisch eingefärbt werden.

Der Farbalgorithmus ist recht simpel und eignet sich am besten für Materialbilder mit einem begrenzten Farbbereich. Zur Färbung eines Materials zieht der Renderer einfach den Wert `bgc=` herab und fügt jedem Pixelwert den Wert `color=` hinzu.

Die Färbung ist deaktiviert, wenn `color=` nicht angegeben ist. `bgc=` von Kabinenmaterial ignoriert wird; Stattdessen wird der in die  [!DNL vnc] Datei eingebettete Basisfarbwert verwendet.
