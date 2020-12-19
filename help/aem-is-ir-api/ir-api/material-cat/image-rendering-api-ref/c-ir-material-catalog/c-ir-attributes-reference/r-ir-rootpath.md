---
description: Quelldatenstammpfad. Textzeichenfolgenwert. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für alle Vignetten-, Textur-, Bild- und ICC-Datendateien, auf die in diesem Bildkatalog verwiesen wird.
seo-description: Quelldatenstammpfad. Textzeichenfolgenwert. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für alle Vignetten-, Textur-, Bild- und ICC-Datendateien, auf die in diesem Bildkatalog verwiesen wird.
seo-title: RootPath *
solution: Experience Manager
title: RootPath *
topic: Scene7 Image Serving - Image Rendering API
uuid: a23ea524-8ca4-47c4-83a5-64a174d8767e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# RootPath *{#rootpath}

Quelldatenstammpfad. Textzeichenfolgenwert. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für alle Vignetten-, Textur-, Bild- und ICC-Datendateien, auf die in diesem Bildkatalog verwiesen wird.

## Eigenschaften {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Textzeichenfolge. Muss leer sein, ein gültiges Pfadsegment relativ zur Image Rendering Server-Konfigurationseinstellung `ir.resourceRootPaths` oder ein gültiger absoluter Dateipfad. Es sollten keine Trennzeichen für vorangestellte und nachfolgende Pfadelemente enthalten sein.

## Standard {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Vererbt von `default::RootPath`, wenn nicht definiert. Wenn definiert, aber leer, trägt nicht zum Stammpfad der Quelldatei bei.

## Verwandte Themen {#section-92012cc1ce32448ea977e7e0484857e2}

[Katalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ,  [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969),  `ir.resourceRootPaths`
