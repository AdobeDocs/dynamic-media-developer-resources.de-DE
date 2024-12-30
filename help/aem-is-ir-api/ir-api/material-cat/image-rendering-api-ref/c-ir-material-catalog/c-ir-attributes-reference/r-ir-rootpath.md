---
title: rootPath
description: Stammverzeichnis der Source-Daten. Text-Zeichenfolgenwert. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für alle Vignetten-, Textur-, Bild- und ICC-Datendateien, auf die dieser Bildkatalog verweist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# rootPath{#rootpath}

Stammverzeichnis der Source-Daten. Text-Zeichenfolgenwert. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für alle Vignetten-, Textur-, Bild- und ICC-Datendateien, auf die dieser Bildkatalog verweist.

## Eigenschaften {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Text-String Muss leer sein, ein gültiges Pfadsegment, das mit der Konfigurationseinstellung des Image-Rendering-Servers `ir.resourceRootPaths` ist, oder ein gültiger absoluter Dateipfad. Sollte keine Trennzeichen für Pfad-Elemente am Anfang und am Ende enthalten.

## Standard {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Von `default::RootPath` geerbt, wenn nicht definiert. Wenn er definiert, aber leer ist, trägt er nicht zum Stammverzeichnis der Quelldatei bei.

## Verwandte Themen {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`
