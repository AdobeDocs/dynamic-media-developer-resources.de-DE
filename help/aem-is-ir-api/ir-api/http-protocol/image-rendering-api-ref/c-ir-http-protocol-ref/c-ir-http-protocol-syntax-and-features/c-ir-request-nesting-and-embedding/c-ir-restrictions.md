---
title: Einschränkungen
description: Für die Verschachtelung und Einbettung gelten einige Einschränkungen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
TQID: 'https://experienceleague.adobe.com/rwy6ZnKA0pc-z-dqhsI0gD-FSqpqZr1bcIgJqtsjfIs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# Einschränkungen{#restrictions}

Für die Verschachtelung und Einbettung gelten einige Einschränkungen.

Für eine gute Server-Leistung sollte die Auflösung der Bilder, die von verschachtelten Anforderungen zurückgegeben werden, in angemessenem Maße mit der Texturauflösung der Objekte übereinstimmen, auf die das Material angewendet wird.

Fremdbilder werden lokal zwischengespeichert. Änderungen an solchen Bildern werden erst erkannt, wenn der lokale Cache-Eintrag veraltet ist (basierend auf dem Ablaufdatum-HTTP-Header).
