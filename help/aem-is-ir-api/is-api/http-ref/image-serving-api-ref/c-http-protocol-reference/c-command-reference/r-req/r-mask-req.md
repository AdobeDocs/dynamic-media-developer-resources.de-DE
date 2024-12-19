---
description: Bildmaske. Fordert die Daten der Maske (Alphakanal) an.
solution: Experience Manager
title: Maske
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# Maske{#mask}

Bildmaske. Fordert die Daten der Maske (Alphakanal) an.

`req=mask`

Unterstützt die gleichen Befehle wie `req=img`. Es wird vom Server auf die gleiche Weise verarbeitet, aber anstatt die RGB- oder RGBA-Daten zurückzugeben, verwirft der Server die Farbinformationen und gibt nur die Maskendaten (Alphakanal) zurück. Das Format der Antwortdaten und der MIME-Typ der Antwort werden durch `fmt=` bestimmt.

Die HTTP-Antwort kann basierend auf `catalog::Expiration` mit der TTL zwischengespeichert werden.
