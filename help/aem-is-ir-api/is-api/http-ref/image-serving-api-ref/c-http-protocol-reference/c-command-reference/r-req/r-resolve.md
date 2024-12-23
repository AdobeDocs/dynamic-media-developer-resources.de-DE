---
title: auflösen
description: Debug-Anfrage. Dieser Debug-Befehl analysiert und verarbeitet die Anfrage vorab, führt Bildkatalogsuchen, Katalogmodifikator-Einfügungen, Makro- und Variablenersetzungen usw. aus, genau wie req=img.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# auflösen{#resolve}

Debug-Anfrage. Dieser Debug-Befehl analysiert und verarbeitet die Anfrage vorab, führt Bildkatalogsuchen, catalog:modifier-Einschlüsse, Makro- und Variablenersetzungen usw. aus, genau wie req=img.

`req=resolve`

Die endgültige Anforderungszeichenfolge wird bei MIME-Typ `text/plain` anstelle des Ergebnisbilds zurückgegeben.

Die HTTP-Antwort kann nicht zwischengespeichert werden.
