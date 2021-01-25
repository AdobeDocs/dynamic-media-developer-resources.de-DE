---
description: Image Serving unterstützt Bildkataloge mit ISO-8859-1- und UTF-8-Kodierung.
seo-description: Image Serving unterstützt Bildkataloge mit ISO-8859-1- und UTF-8-Kodierung.
seo-title: Zeichenkodierung
solution: Experience Manager
title: Zeichenkodierung
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Zeichenkodierung{#character-encoding}

Image Serving unterstützt Bildkataloge mit ISO-8859-1- und UTF-8-Kodierung.

Ein Byte Order Mark (BOM) wird verwendet, um die Kodierung für jede Datei anzugeben. Bei UTF-8 ist das BOM die Bytesequenz `EF BB BF`. Die UTF-8-Kodierung wird angenommen, wenn diese Zeichensequenz am Anfang jeder Bildkatalogdatei erkannt wird. Jede andere Bytefolge führt dazu, dass die Datei als mit dem ISO-8859-1-Standard kodiert interpretiert wird.

Viele zeitgenössische Anwendungen, die für UTF-8 konfiguriert sind, fügen das BOM automatisch ein.
