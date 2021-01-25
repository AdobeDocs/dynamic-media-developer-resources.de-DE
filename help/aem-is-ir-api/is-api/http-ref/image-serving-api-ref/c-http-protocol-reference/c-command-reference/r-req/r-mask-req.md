---
description: Bildmaske. Fordert die Maskendaten (Alpha-Kanal) an.
seo-description: Bildmaske. Fordert die Maskendaten (Alpha-Kanal) an.
seo-title: Maske
solution: Experience Manager
title: Maske
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# mask{#mask}

Bildmaske. Fordert die Maskendaten (Alpha-Kanal) an.

`req=mask`

Unterstützt dieselben Befehle wie `req=img` und wird auf dieselbe Weise vom Server verarbeitet. Anstatt jedoch die RGB- oder RGBA-Daten zurückzugeben, verwirft der Server die Farbinformationen und gibt nur die Daten zur Maske (Alpha-Kanal) zurück. Das Antwortdatenformat und der AntwortmIME-Typ werden von `fmt=` bestimmt.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.
