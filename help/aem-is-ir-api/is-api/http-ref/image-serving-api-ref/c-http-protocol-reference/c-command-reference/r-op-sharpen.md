---
description: Scharfzeichnen des Bildes. Wendet einen grundlegenden Scharfzeichnungsfilter auf die Ebene oder auf das endgültige Bild der Ansicht an, wenn layer=comp skaliert wird.
seo-description: Scharfzeichnen des Bildes. Wendet einen grundlegenden Scharfzeichnungsfilter auf die Ebene oder auf das endgültige Bild der Ansicht an, wenn layer=comp skaliert wird.
seo-title: op_sharpen
solution: Experience Manager
title: op_sharpen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1a00c60a-0d5c-4a99-a649-f29ebd710cf3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 7%

---


# op_sharpen{#op-sharpen}

Scharfzeichnen des Bildes. Wendet einen grundlegenden Scharfzeichnungsfilter auf die Ebene oder auf das endgültige Bild der Ansicht an, wenn layer=comp skaliert wird.

`op_sharpen=0|1`

Die Ebenenmaske oder die Composite-Maske wird ebenfalls scharfgezeichnet.

## Eigenschaften {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Ebenenattribut oder Ansicht-Attribut. Gilt für die aktuelle Ebene oder für die letzte Ansicht, wenn `layer=comp`. Von Effektebenen ignoriert.

## Standard {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, um keinen Scharfzeichnungseffekt zu erzielen.

## Beispiel {#section-3202122df5db4e14b358ecabfb6d8b85}

Kompensieren Sie die leichte Unschärfe, die durch das Neuberechnen des Bildes entsteht. Außerdem erhöhen wir die JPEG-Qualität, um zusätzliche JPEG-Artefakte entlang der scharfgezeichneten Kanten zu vermeiden.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Verwandte Themen {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
