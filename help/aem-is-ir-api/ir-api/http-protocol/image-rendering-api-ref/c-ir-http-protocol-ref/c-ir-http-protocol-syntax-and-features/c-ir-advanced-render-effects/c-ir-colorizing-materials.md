---
description: Die meisten Materialien können dynamisch eingefärbt werden.
solution: Experience Manager
title: Farbstoffe
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Farbstoffe{#colorizing-materials}

Die meisten Materialien können dynamisch eingefärbt werden.

Der Farbalgorithmus ist recht simpel und eignet sich am besten für Materialbilder mit einem begrenzten Farbbereich. Um ein Material zu färben, subtrahiert der Renderer einfach den `bgc=` -Wert und fügt den `color=` -Wert zu jedem Pixelwert hinzu.

Die Kolorisierung ist deaktiviert, wenn `color=` nicht angegeben ist. `bgc=` von Kabinenmaterial ignoriert wird; stattdessen wird der in die  [!DNL vnc] Datei eingebettete Basisfarbwert verwendet.
