---
description: Transformationen werden auf Quellbilder und Textebenen angewendet.
solution: Experience Manager
title: Ebenentransformationen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
TQID: 'https://experienceleague.adobe.com/jChFcZzWWOlbicpu0WeRSJb608dGT9JmVSItV-uEjBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 0%

---

# Ebenentransformationen{#layer-transforms}

Transformationen werden auf Quellbilder und Textebenen angewendet.

Die folgenden Operationen werden auf Quellbilder in der angegebenen Reihenfolge angewendet, um die gewünschte räumliche Beziehung zur Ebene 0 zu erreichen:

1. `crop=` anwenden, falls angegeben.
1. Skalierung basierend auf `size=` oder, falls `size=` nicht angegeben ist, basierend auf `scale=`, oder, falls `scale=` nicht angegeben ist, basierend auf `res=`, oder, falls `res=` nicht angegeben ist, verwenden Sie das Quellbild mit voller Auflösung.
1. `flip=` anwenden, falls angegeben.
1. `rotate=` anwenden, falls angegeben.
1. `extend=` anwenden, falls angegeben.
1. Positionieren Sie die Ebene auf der Arbeitsfläche basierend auf `origin=` und `pos=` (siehe unten).

Die folgenden Transformationen werden auf Textebenen angewendet:

1. Die Größe des Textfelds wird durch `size=` oder die Textbreite und -höhe bestimmt, wenn `size=` nur teilweise oder gar nicht angegeben ist. Der Text wird innerhalb des Textfelds mithilfe der rtf-Textausrichtungsattribute ausgerichtet. Text kann durch das Textfeld abgeschnitten werden.
1. Skalieren Sie den Textinhalt basierend auf der mit `textAttr=` angegebenen Auflösung.
1. `rotate=` anwenden, falls angegeben.
1. `extend=` anwenden, falls angegeben.
1. Positionieren Sie die Ebene auf der Arbeitsfläche basierend auf `origin=` und `pos=` (siehe unten).

Sowohl für Bild- als auch für Textebenen gilt der letzte Schritt der Positionierung der Ebene auf der Arbeitsfläche nicht für Ebene 0, da Ebene 0 die Arbeitsfläche darstellt.
