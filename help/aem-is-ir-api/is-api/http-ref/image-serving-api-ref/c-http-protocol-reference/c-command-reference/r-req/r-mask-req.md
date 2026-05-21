---
description: Bildmaske. Fordert die Daten der Maske (Alphakanal) an.
solution: Experience Manager
title: Maske
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
TQID: 'https://experienceleague.adobe.com/FMsQMZsc3N1ToEzXBE0vOzkezfemSzT6NaGJQ1gQqd8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# Maske{#mask}

Bildmaske. Fordert die Daten der Maske (Alphakanal) an.

`req=mask`

Unterstützt die gleichen Befehle wie `req=img`. Sie werden vom Server auf die gleiche Weise verarbeitet, aber anstatt die RGB- oder RGBA-Daten zurückzugeben, verwirft der Server die Farbinformationen und gibt nur die Maskendaten (Alphakanal) zurück. Das Format der Antwortdaten und der MIME-Typ der Antwort werden durch `fmt=` bestimmt.

Die HTTP-Antwort kann basierend auf `catalog::Expiration` mit der TTL zwischengespeichert werden.
