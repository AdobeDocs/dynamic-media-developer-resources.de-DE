---
description: Laden Sie den Server-Cache vorab. Führt die Anforderung genau wie req=img aus, aber statt das Bild zurückzugeben, gibt der Server die Länge des Antwortbilds (image.length) zurück, formatiert als Textdaten mit MIME-Typ text/plain.
seo-description: Laden Sie den Server-Cache vorab. Führt die Anforderung genau wie req=img aus, aber statt das Bild zurückzugeben, gibt der Server die Länge des Antwortbilds (image.length) zurück, formatiert als Textdaten mit MIME-Typ text/plain.
seo-title: loadcache
solution: Experience Manager
title: loadcache
topic: Scene7 Image Serving - Image Rendering API
uuid: 44f0db05-2323-4aa2-853c-f78e656a4308
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# loadcache{#loadcache}

Laden Sie den Server-Cache vorab. Führt die Anforderung genau wie req=img aus, aber statt das Bild zurückzugeben, gibt der Server die Länge des Antwortbilds (image.length) zurück, formatiert als Textdaten mit MIME-Typ text/plain.

`req=loadcache`

Die HTTP-Antwort kann nicht zwischengespeichert werden.

Andere Befehle in der Anforderung gelten wie dokumentiert.
