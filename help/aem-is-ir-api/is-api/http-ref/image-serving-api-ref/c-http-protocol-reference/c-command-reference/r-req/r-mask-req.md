---
description: Bildmaske. Fordert die Maskendaten (Alphakanal) an.
solution: Experience Manager
title: mask
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# mask{#mask}

Bildmaske. Fordert die Maskendaten (Alphakanal) an.

`req=mask`

Unterstützt dieselben Befehle wie `req=img`. Er wird auf die gleiche Weise vom Server verarbeitet, aber anstatt die RGB- oder RGBA-Daten zurückzugeben, verwirft der Server die Farbinformationen und gibt nur die Maskendaten (Alphakanal) zurück. Das Antwortdatenformat und der Antwort-MIME-Typ werden von `fmt=` bestimmt.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.
