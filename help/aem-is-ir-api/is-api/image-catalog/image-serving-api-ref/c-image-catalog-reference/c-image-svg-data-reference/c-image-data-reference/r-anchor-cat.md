---
description: Bildanker. Herkunft, wenn dieses Bild als Ebene in einer Vorlage oder einem Composite-Bild verwendet wird.
solution: Experience Manager
title: Anker
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 5%

---


# Anker{#anchor}

Bildanker. Herkunft, wenn dieses Bild als Ebene in einer Vorlage oder einem Composite-Bild verwendet wird.

Definiert auch den Standard-Mittelpunkt für die Drehung.

## Eigenschaften {#section-95740f14160744e7bc763094b8be40d8}

Zwei Ganzzahlzahlen, durch Kommas getrennt. Pixel-Versatz relativ zur oberen, linken Ecke des Bildes mit voller Auflösung.

Überschrieben von `anchor=`(die wiederum mit `origin=` überschrieben werden können).

## Standard {#section-ca3a4cc837d643519eff15951f2b47a1}

Der Mittelpunkt des Bilds wird verwendet, wenn dieses Feld nicht vorhanden ist oder leer ist, und wenn es sich um einen gültigen Bilddatensatz handelt (d. h. wenn `catalog::Path` gültig ist).

## Verwandte Themen {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [Herkunft=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
