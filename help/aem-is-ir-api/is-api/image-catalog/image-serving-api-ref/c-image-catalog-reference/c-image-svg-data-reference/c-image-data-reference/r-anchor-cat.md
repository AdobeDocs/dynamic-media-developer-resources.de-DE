---
description: Bildanker. Herkunft, wenn dieses Bild als Ebene in einer Vorlage oder einem Composite-Bild verwendet wird.
seo-description: Bildanker. Herkunft, wenn dieses Bild als Ebene in einer Vorlage oder einem Composite-Bild verwendet wird.
seo-title: Anker
solution: Experience Manager
title: Anker
topic: Scene7 Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '130'
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
