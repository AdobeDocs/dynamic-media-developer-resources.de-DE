---
description: Image Serving unterstützt Bildkataloge mit ISO-8859-1 und UTF-8-Kodierung.
solution: Experience Manager
title: Zeichenkodierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Zeichenkodierung{#character-encoding}

Image Serving unterstützt Bildkataloge mit ISO-8859-1 und UTF-8-Kodierung.

Eine Byte Order Mark (BOM) wird verwendet, um die Kodierung für jede Datei anzugeben. Für UTF-8 ist das BOM die Byte-Sequenz `EF BB BF`. Die UTF-8-Kodierung wird angenommen, wenn diese Zeichensequenz am Anfang jeder Bildkatalogdatei erkannt wird. Jede andere Byte-Sequenz führt dazu, dass die Datei als gemäß dem ISO-8859-1-Standard kodiert interpretiert wird.

Viele moderne Anwendungen, die für UTF-8 konfiguriert sind, fügen das BOM automatisch ein.
