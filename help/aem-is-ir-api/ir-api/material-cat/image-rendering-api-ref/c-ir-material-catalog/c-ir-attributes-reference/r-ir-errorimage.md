---
description: Fehlermeldungsbild. Beim Rendern von Bildern wird normalerweise ein Fehlerstatus mit einer Textmeldung zurückgegeben, wenn ein Fehler auftritt. Attribut ErrorImage ermöglicht die Konfiguration eines Bildes, das im Fehlerfall zurückgegeben werden kann.
seo-description: Fehlermeldungsbild. Beim Rendern von Bildern wird normalerweise ein Fehlerstatus mit einer Textmeldung zurückgegeben, wenn ein Fehler auftritt. Attribut ErrorImage ermöglicht die Konfiguration eines Bildes, das im Fehlerfall zurückgegeben werden kann.
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# ErrorImage *{#errorimage}

Fehlermeldungsbild. Beim Rendern von Bildern wird normalerweise ein Fehlerstatus mit einer Textmeldung zurückgegeben, wenn ein Fehler auftritt. attribute::ErrorImage ermöglicht die Konfiguration eines Bildes, das im Fehlerfall zurückgegeben wird.

Wenn ein Fehler auftritt, versucht der Server zunächst, den Wert von `ImageRendering::attribute::ErrorImage`als einfachen Bilddateipfad zu interpretieren. Wenn die Datei nicht geöffnet werden kann, sendet sie die Attributwerte und Fehlerdetails an Image Serving, das die Prozesse, wie unter `ImageServing::attribute::ErrorImage` beschrieben, durchführt. Wenn Image Serving kein gültiges Antwortbild zurückgibt, werden der standardmäßige HTTP-Fehlerstatus und die Textnachricht an den Client gesendet.

Fehlerbilder werden mit HTTP-Status 200 zurückgegeben.

## Eigenschaften {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Textzeichenfolge. Bei Angabe muss es sich entweder um einen **`ImageServing::catalog::id`**-Wert, einen relativen Pfad (zu **`ImageServing::attribute::RootPath`** oder **`ImageRendering::attribute::RootPath`**) oder einen absoluten Pfad zu einer Bilddatei handeln, auf die der Image-Server zugreifen kann.

## Standard {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Von `default::ErrorImage` geerbt, wenn sie nicht definiert ist. Wenn sie definiert, aber leer ist, ist das Verhalten des Fehlerbilds deaktiviert, auch wenn `default::ErrorImage` definiert ist, und ein HTTP-Fehlerstatus wird zurückgegeben.

## Verwandte Themen {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
