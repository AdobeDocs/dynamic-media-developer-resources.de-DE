---
description: Servercache vorladen. Führt die Anfrage genau wie req=img aus, aber anstatt das Bild zurückzugeben, gibt der Server die Länge des Antwortbildes (image.length) zurück, formatiert als Textdaten mit dem MIME-Typ text/plain.
solution: Experience Manager
title: LoadCache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
TQID: 'https://experienceleague.adobe.com/Llp-0huLGkxBVxSgRngyAtNKqeHuZ02xJu71MM-Nqww'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 0%

---

# LoadCache{#loadcache}

Servercache vorladen. Führt die Anfrage genau wie req=img aus, aber anstatt das Bild zurückzugeben, gibt der Server die Länge des Antwortbildes (image.length) zurück, formatiert als Textdaten mit dem MIME-Typ text/plain.

`req=loadcache`

Die HTTP-Antwort kann nicht zwischengespeichert werden.

Andere Befehle in der Anfrage gelten wie dokumentiert.
