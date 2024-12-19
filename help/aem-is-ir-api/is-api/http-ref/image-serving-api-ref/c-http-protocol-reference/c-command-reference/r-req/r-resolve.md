---
title: auflösen
description: Debug-Anfrage. Dieser Debug-Befehl analysiert und verarbeitet die Anfrage vorab, führt Bildkatalogsuchen, Katalogmodifikator-Einfügungen, Makro- und Variablenersetzungen usw. aus, genau wie req=img.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# auflösen{#resolve}

Debug-Anfrage. Dieser Debug-Befehl analysiert und verarbeitet die Anfrage vorab, führt Bildkatalogsuchen, catalog:modifier-Einschlüsse, Makro- und Variablenersetzungen usw. aus, genau wie req=img.

`req=resolve`

Die endgültige Anforderungszeichenfolge wird bei MIME-Typ `text/plain` anstelle des Ergebnisbilds zurückgegeben.

Die HTTP-Antwort kann nicht zwischengespeichert werden.
