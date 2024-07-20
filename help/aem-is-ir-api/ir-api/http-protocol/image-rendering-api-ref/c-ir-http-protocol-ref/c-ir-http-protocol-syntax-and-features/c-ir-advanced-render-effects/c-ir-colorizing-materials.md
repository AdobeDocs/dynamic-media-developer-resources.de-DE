---
title: Materialien einfärben
description: Die meisten Materialien können dynamisch eingefärbt werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# Materialien einfärben{#colorizing-materials}

Die meisten Materialien können dynamisch eingefärbt werden.

Der Farbalgorithmus ist simpel und eignet sich am besten für Materialbilder mit einem begrenzten Farbbereich. Um ein Material zu färben, subtrahiert der Renderer einfach den Wert `bgc=` und fügt den Wert `color=` zu jedem Pixelwert hinzu.

Die Kolorisierung ist deaktiviert, wenn `color=` nicht angegeben ist. Das Attribut `bgc=` wird von Kabinenmaterialien ignoriert; stattdessen wird der in die Datei [!DNL vnc] eingebettete Basisfarbwert verwendet.
