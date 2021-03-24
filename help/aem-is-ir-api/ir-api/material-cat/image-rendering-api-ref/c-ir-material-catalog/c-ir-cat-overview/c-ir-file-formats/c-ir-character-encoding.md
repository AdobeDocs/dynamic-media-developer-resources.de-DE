---
description: Image Rendering unterstützt Materialkataloge mit ISO-8859-1 und UTF-8 Kodierung.
solution: Experience Manager
title: Zeichenkodierung
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Zeichenkodierung{#character-encoding}

Image Rendering unterstützt Materialkataloge mit ISO-8859-1 und UTF-8 Kodierung.

Ein Byte Order Mark (BOM) wird verwendet, um die Kodierung für jede Datei anzugeben. Bei UTF-8 ist das BOM die Bytesequenz `EF BB BF`. Die UTF-8-Kodierung wird angenommen, wenn diese Zeichensequenz am Anfang jeder Materialkatalogdatei erkannt wird. Jede andere Bytefolge führt dazu, dass die Datei als mit dem ISO-8859-1-Standard kodiert interpretiert wird.

Viele zeitgenössische Anwendungen, die für UTF-8 konfiguriert sind, fügen das BOM automatisch ein.
