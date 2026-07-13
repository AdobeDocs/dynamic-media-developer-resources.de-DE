---
title: Zeichenkodierung
description: Das Bild-Rendering unterstützt Materialkataloge mit ISO-8859-1- und UTF-8-Codierung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
TQID: 'https://experienceleague.adobe.com/1ITLimvCUD8hrdfeyyod6nE0sMmfIJ3ySx5HCFa2ZQk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Zeichenkodierung{#character-encoding}

Das Bild-Rendering unterstützt Materialkataloge mit ISO-8859-1- und UTF-8-Codierung.

Eine Byte Order Mark (BOM) wird verwendet, um die Kodierung für jede Datei anzugeben. Bei UTF-8 ist die BOM die Bytefolge `EF BB BF`. Die UTF-8-Codierung wird angenommen, wenn diese Zeichensequenz ganz am Anfang jeder Materialkatalogdatei erkannt wird. Jede andere Bytefolge führt dazu, dass die Datei als nach dem ISO-8859-1-Standard kodiert interpretiert wird.

Viele zeitgenössische Anwendungen fügen die STL automatisch ein, wenn sie für UTF-8 konfiguriert sind.

