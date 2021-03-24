---
description: Die Ebenen werden positioniert, indem die Herkunft der Ebene (Herkunft=) an der Herkunft der Hintergrundebene an einem durch "pos="festgelegten Offset ausgerichtet wird.
solution: Experience Manager
title: Ebenenplatzierung
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# Ebenenplatzierung{#layer-placement}

Die Ebenen werden positioniert, indem die Herkunft der Ebene (Herkunft=) an der Herkunft der Hintergrundebene an einem durch &quot;pos=&quot;festgelegten Offset ausgerichtet wird.

Wenn die Herkunft der Ebene nicht explizit für eine Bildebene angegeben ist, wird sie wie folgt berechnet:

1. Legen Sie den Bildanker fest. Verwenden Sie `anchor=` oder, falls nicht angegeben, `catalog::Anchor`.
1. Wenn der Bildanker definiert ist, wenden Sie die Ebene transformiert an und `extend=`, um sie in einen Herkunft=-Wert zu konvertieren.
1. Wenn kein Bildanker definiert ist, wird die Herkunft der Ebene in der Mitte des Ebenenrechtecks platziert (nach dem Anwenden von `extend=`).

![](assets/layerplacement.png)

