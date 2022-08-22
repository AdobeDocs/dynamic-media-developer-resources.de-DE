---
title: RootPath
description: Quelldaten-Stammpfad. Textzeichenfolgenwert. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für alle Vignetten-, Textur-, Bild- und ICC-Datendateien, auf die in diesem Bildkatalog verwiesen wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# RootPath{#rootpath}

Quelldaten-Stammpfad. Textzeichenfolgenwert. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für alle Vignetten-, Textur-, Bild- und ICC-Datendateien, auf die in diesem Bildkatalog verwiesen wird.

## Eigenschaften {#section-5ff1cf592dd24dfc8cfa470c753ab828}

Textzeichenfolge. Muss leer sein, ein gültiges Pfadsegment relativ zur Konfigurationseinstellung für den Image Rendering-Server `ir.resourceRootPaths`oder einen gültigen absoluten Dateipfad. Sollte keine führenden und nachfolgenden Pfadelement-Trennzeichen enthalten.

## Standard {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

Vererbt von `default::RootPath` falls nicht definiert. Wenn definiert, aber leer, trägt es nicht zum Stammverzeichnis der Quelldatei bei.

## Verwandte Themen {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) , [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969), `ir.resourceRootPaths`
