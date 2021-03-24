---
description: Bildmaske. Fordert die Maskendaten (Alpha-Kanal) an.
solution: Experience Manager
title: Maske
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# mask{#mask}

Bildmaske. Fordert die Maskendaten (Alpha-Kanal) an.

`req=mask`

Unterstützt dieselben Befehle wie `req=img`. Er wird auf die gleiche Weise vom Server verarbeitet, aber anstatt die RGB- oder RGBA-Daten zurückzugeben, verwirft der Server die Farbinformationen und gibt nur die Daten zur Maske (Alpha-Kanal) zurück. Das Antwortdatenformat und der AntwortmIME-Typ werden von `fmt=` bestimmt.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.
