---
description: Die meisten Materialien können dynamisch eingefärbt werden.
solution: Experience Manager
title: Färben von Materialien
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Färben von Materialien{#colorizing-materials}

Die meisten Materialien können dynamisch eingefärbt werden.

Der Farbalgorithmus ist recht simpel und eignet sich am besten für Materialbilder mit einem begrenzten Farbbereich. Zur Färbung eines Materials zieht der Renderer einfach den Wert `bgc=` herab und fügt jedem Pixelwert den Wert `color=` hinzu.

Die Färbung ist deaktiviert, wenn `color=` nicht angegeben ist. `bgc=` von Kabinenmaterial ignoriert wird; Stattdessen wird der in die  [!DNL vnc] Datei eingebettete Basisfarbwert verwendet.
