---
title: Ebenenplatzierung
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

# Ebenenplatzierung{#layer-placement}

Die Ebenen werden positioniert, indem der Ebenenursprung (origin=) an der Herkunft der Hintergrundebene an einem durch pos= festgelegten Versatz ausgerichtet wird.

Wenn der Ebenenursprung nicht explizit für eine Bildebene angegeben ist, wird er wie folgt berechnet:

1. Legen Sie den Bildanker fest. Verwenden Sie `anchor=` oder, falls nicht angegeben, `catalog::Anchor`.
1. Wenn der Bildanker definiert ist, wenden Sie die Ebene an, um sie zu transformieren, und `extend=`, um sie in den Wert origin= zu konvertieren.
1. Wenn kein Bildanker definiert ist, wird der Ebenenursprung in der Mitte des Ebenenrechtecks platziert (nach dem Anwenden von `extend=`).

![Ebenenplatzierungsbild](assets/layerplacement.png)
