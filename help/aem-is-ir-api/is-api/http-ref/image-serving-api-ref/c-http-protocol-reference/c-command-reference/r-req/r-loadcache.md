---
description: Servercache vorladen. Führt die Anfrage genau wie req=img aus, aber anstatt das Bild zurückzugeben, gibt der Server die Länge des Antwortbildes (image.length) zurück, formatiert als Textdaten mit dem MIME-Typ text/plain.
solution: Experience Manager
title: LoadCache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# LoadCache{#loadcache}

Servercache vorladen. Führt die Anfrage genau wie req=img aus, aber anstatt das Bild zurückzugeben, gibt der Server die Länge des Antwortbildes (image.length) zurück, formatiert als Textdaten mit dem MIME-Typ text/plain.

`req=loadcache`

Die HTTP-Antwort kann nicht zwischengespeichert werden.

Andere Befehle in der Anfrage gelten wie dokumentiert.
