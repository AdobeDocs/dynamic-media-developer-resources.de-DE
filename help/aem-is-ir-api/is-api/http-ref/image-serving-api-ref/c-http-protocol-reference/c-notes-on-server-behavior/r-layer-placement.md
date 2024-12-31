---
title: Platzierung der Ebene
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Platzierung der Ebene{#layer-placement}

Ebenen werden positioniert, indem der Ebenenursprung (Origin=) mit dem Hintergrund-Ebenenursprung an einem durch Pos= angegebenen Versatz ausgerichtet wird.

Wenn der Ebenenursprung für eine Bildebene nicht explizit angegeben ist, wird er wie folgt berechnet:

1. Bestimmen Sie den Bildanker. Verwenden Sie `anchor=` oder, falls nicht anders angegeben, `catalog::Anchor`.
1. Wenn der Bildanker definiert ist, wenden Sie die Ebenentransformationen und `extend=` an, um sie in einen Origin=-Wert zu konvertieren.
1. Wenn kein Bildanker definiert ist, wird der Ebenenursprung (nach dem Anwenden von `extend=`) in der Mitte des Ebenenrechtecks platziert.

![Ebenenplatzierungsbild](assets/layerplacement.png)
