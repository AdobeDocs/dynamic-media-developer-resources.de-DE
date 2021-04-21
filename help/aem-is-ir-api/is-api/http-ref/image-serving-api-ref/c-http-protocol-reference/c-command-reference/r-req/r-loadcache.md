---
description: Laden Sie den Server-Cache vorab. Führt die Anforderung genau wie req=img aus, aber statt das Bild zurückzugeben, gibt der Server die Länge des Antwortbilds (image.length) zurück, formatiert als Textdaten mit MIME-Typ text/plain.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# loadcache{#loadcache}

Laden Sie den Server-Cache vorab. Führt die Anforderung genau wie req=img aus, aber statt das Bild zurückzugeben, gibt der Server die Länge des Antwortbilds (image.length) zurück, formatiert als Textdaten mit MIME-Typ text/plain.

`req=loadcache`

Die HTTP-Antwort kann nicht zwischengespeichert werden.

Andere Befehle in der Anforderung gelten wie dokumentiert.
