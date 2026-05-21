---
title: Färbemittel
description: Die meisten Materialien können dynamisch eingefärbt werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
TQID: 'https://experienceleague.adobe.com/MGmuOj214tFPKeSGwz33pGn2m0B0fme1Cq-umlxG9v0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# Färbemittel{#colorizing-materials}

Die meisten Materialien können dynamisch eingefärbt werden.

Der Farbalgorithmus ist einfach aufgebaut und eignet sich am besten für Materialbilder mit begrenztem Farbtonbereich. Um ein Material einzufärben, subtrahiert der Renderer einfach den `bgc=` und addiert den `color=` Wert zu jedem Pixelwert.

Die Farbgebung ist deaktiviert, wenn kein `color=` angegeben ist. Das Attribut `bgc=` wird von Schrankmaterialien ignoriert. Stattdessen wird der in die [!DNL vnc] eingebettete Grundfarbwert verwendet.
