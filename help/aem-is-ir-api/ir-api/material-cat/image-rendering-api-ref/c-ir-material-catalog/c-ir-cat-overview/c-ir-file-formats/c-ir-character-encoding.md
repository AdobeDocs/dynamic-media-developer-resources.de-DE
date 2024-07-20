---
title: Zeichenkodierung
description: Image Rendering unterstützt Materialkataloge mit ISO-8859-1 und UTF-8-Kodierung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Zeichenkodierung{#character-encoding}

Image Rendering unterstützt Materialkataloge mit ISO-8859-1 und UTF-8-Kodierung.

Eine Byte Order Mark (BOM) wird verwendet, um die Kodierung für jede Datei anzugeben. Bei UTF-8 ist das BOM die Bytefolge `EF BB BF`. UTF-8-Kodierung wird angenommen, wenn diese Zeichensatzsequenz am Anfang jeder Materialkatalogdatei erkannt wird. Jede andere Byte-Sequenz führt dazu, dass die Datei als gemäß dem ISO-8859-1-Standard kodiert interpretiert wird.

Viele moderne Anwendungen, die für UTF-8 konfiguriert sind, fügen das BOM automatisch ein.
