---
title: auflösen
description: Debug-Anfrage. Dieser Debugging-Befehl analysiert und verarbeitet die Anforderung, führt Bildkatalogsuche, Katalogmodifikations-Einschlüsse, Makro- und Variablenersetzungen usw. wie req=img aus.
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

Debug-Anfrage. Dieser Debugging-Befehl analysiert und verarbeitet die Anforderung, führt Bildkatalogsuche, catalog::Modifier-Einschlüsse, Makro- und Variablenersetzungen usw. aus, genau wie req=img.

`req=resolve`

Die endgültige Anforderungszeichenfolge wird mit dem MIME-Typ anstelle des Ergebnisbilds zurückgegeben. `text/plain`.

Die HTTP-Antwort kann nicht zwischengespeichert werden.
