---
description: Debug-Anfrage. Dieser Debugging-Befehl analysiert und verarbeitet die Anforderung, führt Bildkatalogsuche, Katalogmodifikations-Einschlüsse, Makro- und Variablenersetzungen usw. wie req=img aus.
solution: Experience Manager
title: auflösen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 2%

---

# auflösen{#resolve}

Debug-Anfrage. Dieser Debugging-Befehl analysiert und verarbeitet die Anforderung, führt Bildkatalog-Suchvorgänge, Katalog::Modifier-Einschlüsse, Makro- und Variablenersetzungen usw. aus, wie req=img.

`req=resolve`

Die endgültige Anforderungszeichenfolge wird anstelle des Ergebnisbilds mit dem MIME-Typ `text/plain` zurückgegeben.

Die HTTP-Antwort kann nicht zwischengespeichert werden.
