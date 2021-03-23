---
description: Die meisten Materialien können dynamisch eingefärbt werden.
seo-description: Die meisten Materialien können dynamisch eingefärbt werden.
seo-title: Färben von Materialien
solution: Experience Manager
title: Färben von Materialien
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---


# Färben von Materialien{#colorizing-materials}

Die meisten Materialien können dynamisch eingefärbt werden.

Der Farbalgorithmus ist recht simpel und eignet sich am besten für Materialbilder mit einem begrenzten Farbbereich. Zur Färbung eines Materials zieht der Renderer einfach den Wert `bgc=` herab und fügt jedem Pixelwert den Wert `color=` hinzu.

Die Färbung ist deaktiviert, wenn `color=` nicht angegeben ist. `bgc=` von Kabinenmaterial ignoriert wird; Stattdessen wird der in die  [!DNL vnc] Datei eingebettete Basisfarbwert verwendet.
