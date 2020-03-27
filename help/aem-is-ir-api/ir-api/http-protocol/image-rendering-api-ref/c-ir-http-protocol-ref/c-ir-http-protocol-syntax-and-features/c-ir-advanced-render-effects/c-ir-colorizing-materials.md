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

---


# Färben von Materialien{#colorizing-materials}

Die meisten Materialien können dynamisch eingefärbt werden.

Der Farbalgorithmus ist recht simpel und eignet sich am besten für Materialbilder mit einem begrenzten Farbbereich. Zur Färbung eines Materials zieht der Renderer den `bgc=` Wert einfach ab und fügt den `color=` Wert zu jedem Pixelwert hinzu.

Die Färbung ist deaktiviert, wenn `color=` keine Angabe gemacht wurde. `bgc=` von Kabinenmaterial ignoriert wird; Stattdessen wird der in die [!DNL vnc] Datei eingebettete Basisfarbwert verwendet.
