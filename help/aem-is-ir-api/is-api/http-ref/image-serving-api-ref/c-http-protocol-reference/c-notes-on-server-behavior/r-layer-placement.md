---
title: Platzierung der Ebene
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# Platzierung der Ebene{#layer-placement}

Ebenen werden positioniert, indem der Ebenenursprung (Origin=) mit dem Hintergrund-Ebenenursprung an einem durch Pos= angegebenen Versatz ausgerichtet wird.

Wenn der Ebenenursprung für eine Bildebene nicht explizit angegeben ist, wird er wie folgt berechnet:

1. Bestimmen Sie den Bildanker. Verwenden Sie `anchor=` oder, falls nicht anders angegeben, `catalog::Anchor`.
1. Wenn der Bildanker definiert ist, wenden Sie die Ebenentransformationen und `extend=` an, um sie in einen Origin=-Wert zu konvertieren.
1. Wenn kein Bildanker definiert ist, wird der Ebenenursprung (nach dem Anwenden von `extend=`) in der Mitte des Ebenenrechtecks platziert.

![Ebenenplatzierungsbild](assets/layerplacement.png)
