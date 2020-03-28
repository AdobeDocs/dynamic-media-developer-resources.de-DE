---
description: Transformationen werden auf Quellbilder und Textebenen angewendet.
seo-description: Transformationen werden auf Quellbilder und Textebenen angewendet.
seo-title: Ebenentransformationen
solution: Experience Manager
title: Ebenentransformationen
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ebenentransformationen{#layer-transforms}

Transformationen werden auf Quellbilder und Textebenen angewendet.

Die folgenden Vorgänge werden auf Quellbilder in der angegebenen Reihenfolge angewendet, um die gewünschte räumliche Beziehung mit Ebene 0 zu erreichen:

1. Wenden Sie `crop=`die Anwendung an, falls angegeben.
1. Skalierung basierend auf `size=` oder, falls `size=` nicht angegeben, basierend auf `scale=`oder, falls nicht angegeben, basierend auf `scale=` oder, falls nicht angegeben, verwenden Sie `res=``res=`das Quellbild mit voller Auflösung.
1. Wenden Sie `flip=`die Anwendung an, falls angegeben.
1. Wenden Sie `rotate=`die Anwendung an, falls angegeben.
1. Wenden Sie `extend=`die Anwendung an, falls angegeben.
1. Positionieren Sie die Ebene auf der Arbeitsfläche basierend auf `origin=` und `pos=` (siehe unten).

Die folgenden Transformationen werden auf Textebenen angewendet:

1. Die Größe des Textfelds wird durch `size=`die Breite und Höhe des Textes bestimmt, wenn sie nur teilweise oder gar nicht angegeben `size=` ist. Der Text wird mithilfe der Attribute für die Textausrichtung rtf innerhalb des Textfelds ausgerichtet. Der Text kann durch das Textfeld beschnitten werden.
1. Skalieren Sie den Textinhalt basierend auf der mit `textAttr=`angegebenen Auflösung.
1. Wenden Sie `rotate=`die Anwendung an, falls angegeben.
1. Wenden Sie `extend=`die Anwendung an, falls angegeben.
1. Positionieren Sie die Ebene auf der Arbeitsfläche basierend auf `origin=` und `pos=`(siehe unten).

Sowohl für Bild- als auch für Textebenen gilt die letzte Schritt-Positionierung der Ebene in der Arbeitsfläche nicht für Ebene 0, da Ebene 0 die Arbeitsfläche darstellt.
