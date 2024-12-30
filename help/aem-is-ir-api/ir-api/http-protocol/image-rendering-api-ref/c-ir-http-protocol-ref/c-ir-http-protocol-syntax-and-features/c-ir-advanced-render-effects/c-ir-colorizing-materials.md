---
title: Färbemittel
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

# Färbemittel{#colorizing-materials}

Die meisten Materialien können dynamisch eingefärbt werden.

Der Farbalgorithmus ist einfach aufgebaut und eignet sich am besten für Materialbilder mit begrenztem Farbtonbereich. Um ein Material einzufärben, subtrahiert der Renderer einfach den `bgc=` und addiert den `color=` Wert zu jedem Pixelwert.

Die Farbgebung ist deaktiviert, wenn kein `color=` angegeben ist. Das Attribut `bgc=` wird von Schrankmaterialien ignoriert. Stattdessen wird der in die [!DNL vnc] eingebettete Grundfarbwert verwendet.
