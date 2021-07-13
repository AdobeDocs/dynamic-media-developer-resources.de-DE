---
description: Scharfzeichnen Sie das Bild. Wendet einen einfachen Scharfzeichnungsfilter auf die Ebene oder das endgültige Ansichtsbild an, nachdem die Skalierung abgeschlossen ist (wenn layer=comp).
solution: Experience Manager
title: op_sharpen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 7%

---

# op_sharpen{#op-sharpen}

Scharfzeichnen Sie das Bild. Wendet einen einfachen Scharfzeichnungsfilter auf die Ebene oder das endgültige Ansichtsbild an, nachdem die Skalierung abgeschlossen ist (wenn layer=comp).

`op_sharpen=0|1`

Die Ebenenmaske oder die zusammengesetzte Maske wird ebenfalls scharfgezeichnet.

## Eigenschaften {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Ebenenattribut oder Ansichtsattribut. Gilt für die aktuelle Ebene oder für das endgültige Ansichtsbild, wenn `layer=comp` Wird von Effektebenen ignoriert.

## Standard {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, um keinen Scharfzeichnungseffekt zu erzielen.

## Beispiel {#section-3202122df5db4e14b358ecabfb6d8b85}

Kompensieren Sie die leichte Unschärfe, die durch das Neuberechnen von Bildern verursacht wird. Außerdem erhöhen wir die JPEG-Qualität, um zusätzliche JPEG-Artefakte entlang der scharfgezeichneten Kanten zu vermeiden.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Verwandte Themen {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
