---
description: Image Serving unterstützt Bildkataloge mit ISO-8859-1- und UTF-8-Kodierung.
solution: Experience Manager
title: Zeichenkodierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
TQID: 'https://experienceleague.adobe.com/tsIJu-zCT-NlV6SD1I1pPYQ0DfqNcu9jSCBVXCcQ9tE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Zeichenkodierung{#character-encoding}

Image Serving unterstützt Bildkataloge mit ISO-8859-1- und UTF-8-Kodierung.

Eine Byte Order Mark (BOM) wird verwendet, um die Kodierung für jede Datei anzugeben. Bei UTF-8 ist die BOM die Bytefolge `EF BB BF`. Die UTF-8-Codierung wird angenommen, wenn diese Zeichensequenz ganz am Anfang jeder Bildkatalogdatei erkannt wird. Jede andere Bytefolge führt dazu, dass die Datei als nach dem ISO-8859-1-Standard kodiert interpretiert wird.

Viele zeitgenössische Anwendungen fügen die STL automatisch ein, wenn sie für UTF-8 konfiguriert sind.
