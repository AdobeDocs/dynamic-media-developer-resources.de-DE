---
title: rootPath
description: Stammverzeichnis der Source-Daten. Text-Zeichenfolgenwert. Absoluter Pfad oder relatives Pfadsegment für den Stammordner für alle Vignetten-, Textur-, Bild- und ICC-Datendateien, auf die dieser Bildkatalog verweist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
TQID: 'https://experienceleague.adobe.com/yCtXjcZDG0HCqydirr7TDe5-e0oWtHmlvAxHDl-gfac'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
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
