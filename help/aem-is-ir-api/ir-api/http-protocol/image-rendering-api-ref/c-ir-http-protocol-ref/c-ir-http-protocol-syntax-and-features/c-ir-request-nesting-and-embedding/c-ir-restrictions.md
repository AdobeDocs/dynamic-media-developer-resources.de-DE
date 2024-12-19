---
title: Einschränkungen
description: Für die Verschachtelung und Einbettung gelten einige Einschränkungen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# Einschränkungen{#restrictions}

Für die Verschachtelung und Einbettung gelten einige Einschränkungen.

Für eine gute Server-Leistung sollte die Auflösung der Bilder, die von verschachtelten Anforderungen zurückgegeben werden, in angemessenem Maße mit der Texturauflösung der Objekte übereinstimmen, auf die das Material angewendet wird.

Fremdbilder werden lokal zwischengespeichert. Änderungen an solchen Bildern werden erst erkannt, wenn der lokale Cache-Eintrag veraltet ist (basierend auf dem Ablaufdatum-HTTP-Header).
