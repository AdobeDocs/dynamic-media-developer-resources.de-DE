---
description: Transformationen werden auf Quellbilder und Textebenen angewendet.
solution: Experience Manager
title: Ebenentransformationen
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Ebenentransformationen{#layer-transforms}

Transformationen werden auf Quellbilder und Textebenen angewendet.

Die folgenden Vorgänge werden auf Quellbilder in der angegebenen Reihenfolge angewendet, um die gewünschte räumliche Beziehung mit Ebene 0 zu erreichen:

1. Wenden Sie `crop=` an, falls angegeben.
1. Skalierung basierend auf `size=` oder, wenn `size=` nicht angegeben ist, basierend auf `scale=` oder, wenn `scale=` nicht angegeben ist, basierend auf `res=` oder, wenn `res=`nicht angegeben ist, verwenden Sie das Quellbild mit voller Auflösung.
1. Wenden Sie `flip=` an, falls angegeben.
1. Wenden Sie `rotate=` an, falls angegeben.
1. Wenden Sie `extend=` an, falls angegeben.
1. Positionieren Sie die Ebene auf der Arbeitsfläche basierend auf `origin=` und `pos=` (siehe unten).

Die folgenden Transformationen werden auf Textebenen angewendet:

1. Die Größe des Textfelds wird durch `size=` oder die Textbreite und -höhe bestimmt, wenn `size=` nur teilweise oder gar nicht angegeben ist. Der Text wird mithilfe der Attribute für die Textausrichtung rtf innerhalb des Textfelds ausgerichtet. Der Text kann durch das Textfeld beschnitten werden.
1. Skalieren Sie den Textinhalt basierend auf der mit `textAttr=` angegebenen Auflösung.
1. Wenden Sie `rotate=` an, falls angegeben.
1. Wenden Sie `extend=` an, falls angegeben.
1. Positionieren Sie die Ebene auf der Arbeitsfläche basierend auf `origin=` und `pos=` (siehe unten).

Sowohl für Bild- als auch für Textebenen gilt die letzte Schritt-Positionierung der Ebene in der Arbeitsfläche nicht für Ebene 0, da Ebene 0 die Arbeitsfläche darstellt.
