---
title: Szenenkoordinaten
description: Der Szenenkoordinatenraum wird verwendet, um Größen und Abstände auf den texturierbaren Objektoberflächen festzulegen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
TQID: 'https://experienceleague.adobe.com/eiZh-q74Q7fGwtuyj8dKSi8h-RMSjOSP7I6Wbq5FxTU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 0%

---

# Szenenkoordinaten{#scene-coordinates}

Der Szenenkoordinatenraum wird verwendet, um Größen und Abstände auf den texturierbaren Objektoberflächen festzulegen.

Da es sich bei den meisten Vignetten um reale Szenen mit physischen Objekten handelt, werden die meisten Vignetten in Zoll als Einheiten für den Szenen-Koordinatenraum erstellt. Es können auch andere Einheiten wie mm oder cm verwendet werden. Das Bild-Rendering unterstützt keine Einheitenkonvertierung.

Die folgenden Befehle akzeptieren Werte im Szenen-Koordinatenraum:

* [verpressen=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [Größe=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
