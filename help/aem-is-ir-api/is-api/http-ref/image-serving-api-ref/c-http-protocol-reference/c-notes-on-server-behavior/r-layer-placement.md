---
description: Die Ebenen werden positioniert, indem die Herkunft der Ebene (Herkunft=) an der Herkunft der Hintergrundebene an einem durch "pos="festgelegten Offset ausgerichtet wird.
seo-description: Die Ebenen werden positioniert, indem die Herkunft der Ebene (Herkunft=) an der Herkunft der Hintergrundebene an einem durch "pos="festgelegten Offset ausgerichtet wird.
seo-title: Ebenenplatzierung
solution: Experience Manager
title: Ebenenplatzierung
topic: Scene7 Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ebenenplatzierung{#layer-placement}

Die Ebenen werden positioniert, indem die Herkunft der Ebene (Herkunft=) an der Herkunft der Hintergrundebene an einem durch &quot;pos=&quot;festgelegten Offset ausgerichtet wird.

Wenn die Herkunft der Ebene nicht explizit für eine Bildebene angegeben ist, wird sie wie folgt berechnet:

1. Legen Sie den Bildanker fest. Verwenden Sie `anchor=`oder, falls nicht angegeben, `catalog::Anchor`.
1. Wenn der Bildanker definiert ist, wenden Sie die Ebene transformiert an und konvertieren Sie sie `extend=` in den Wert Herkunft=.
1. Wenn kein Bildanker definiert ist, wird die Herkunft der Ebene (nach dem Anwenden `extend=`) in der Mitte des Ebenenrechtecks platziert.

![](assets/layerplacement.png)

